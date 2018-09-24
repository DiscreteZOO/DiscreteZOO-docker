# Dockerfile for binder
# Reference: https://mybinder.readthedocs.io/en/latest/dockerfile.html#preparing-your-dockerfile

# Temporary work around: the first 8.2 image that was pushed to dockerhub was incompatible
FROM sagemath/sagemath@sha256:e933509b105f36b9b7de892af847ade7753e058c5d9e0c0f280f591b85ad996d
# FROM sagemath/sagemath:8.2

USER root
RUN    apt-get update -qq \
    && apt-get install -y git wget make \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

USER sage
RUN sage -i bliss gap_packages database_gap
RUN sage -pip install psycopg2
RUN git clone --recursive https://github.com/DiscreteZOO/DiscreteZOO-sage.git ${HOME}/DiscreteZOO-sage
RUN ln -s ${HOME}/DiscreteZOO-sage/discretezoo ${HOME}/sage/local/lib/python2.7/site-packages/discretezoo
RUN mkdir ${HOME}/.discretezoo
RUN wget http://discretezoo.xyz/discretezoo.db -O ${HOME}/.discretezoo/discretezoo.db -q
