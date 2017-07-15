FROM jenkins
LABEL maintainer="tyr@pettingzoo.co"

USER root

# Install Minio Client
RUN curl -o /usr/bin/mc https://dl.minio.io/client/mc/release/linux-amd64/mc && \
    chmod +x /usr/bin/mc

# Install Go
RUN curl -o /tmp/go1.8.3.linux-amd64.tar.gz https://storage.googleapis.com/golang/go1.8.3.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf /tmp/go1.8.3.linux-amd64.tar.gz && \
    rm -Rf /tmp/go1.8.3.linux-amd64.tar.gz && \
    echo "export PATH=\$PATH:/usr/local/go/bin" >> /etc/profile

USER jenkins
