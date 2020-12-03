ARG FROM_REPO=jrafanie
ARG FROM_TAG=fasterer-liveness

FROM ${FROM_REPO}/manageiq-base:${FROM_TAG}
MAINTAINER ManageIQ https://manageiq.org

LABEL name="manageiq-orchestrator" \
      summary="ManageIQ Orchestrator Image"

COPY container-assets/entrypoint /usr/local/bin

RUN source /etc/default/evm && /usr/bin/generate_rpm_manifest.sh

CMD ["entrypoint"]
