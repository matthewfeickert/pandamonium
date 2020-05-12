ARG BASE_IMAGE=python:3.8-slim
# hadolint ignore=DL3006
FROM ${BASE_IMAGE} as base

FROM base
COPY ./panda* /usr/local/pandamonium/

WORKDIR /home/data
ENV HOME /home
RUN cp /root/.bashrc "${HOME}"/ && \
    echo '\nexport PATH=$PATH:/usr/local/pandamonium' >> "${HOME}"/.bashrc

ENTRYPOINT ["/bin/bash", "-l", "-c"]
CMD ["/bin/bash"]
