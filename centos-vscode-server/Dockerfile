FROM centos:centos8

# Code server install script
RUN curl -fsSL https://code-server.dev/install.sh | sh

# Clean up files
RUN rm -rf /root/.cache/code-server/*

EXPOSE 8080
# Copy Config
RUN mkdir -p /.config/code-server
RUN mkdir /.local
COPY config.yaml /.config/code-server/
RUN chmod -R 777 /.config
RUN chmod -R 777 /.local

USER 185

CMD ["/usr/bin/code-server"]