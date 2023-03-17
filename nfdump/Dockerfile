FROM debian:bullseye-backports

RUN apt update && \
    apt install -t bullseye-backports -y \
    nfdump \
    nfdump-sflow \
    procps

WORKDIR /app
COPY entrypoint.sh .
RUN chmod a+x /app/entrypoint.sh

ENTRYPOINT [ "/bin/bash", "/app/entrypoint.sh" ]
