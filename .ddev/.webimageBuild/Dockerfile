
#ddev-generated - Do not modify this file; your modifications will be overwritten.

### DDEV-injected base Dockerfile contents
ARG BASE_IMAGE="scratch"
FROM $BASE_IMAGE
SHELL ["/bin/bash", "-c"]

ARG TARGETPLATFORM
ARG TARGETARCH
ARG TARGETOS
ARG username
ARG uid
ARG gid
ARG DDEV_PHP_VERSION
ARG DDEV_DATABASE
RUN (groupadd --gid $gid "$username" || groupadd "$username" || true) && (useradd  -l -m -s "/bin/bash" --gid "$username" --comment '' --uid $uid "$username" || useradd  -l -m -s "/bin/bash" --gid "$username" --comment '' "$username" || useradd  -l -m -s "/bin/bash" --gid "$gid" --comment '' "$username" || useradd -l -m -s "/bin/bash" --comment '' $username )

### DDEV-injected extra content

RUN mkdir -p /home/$username && chown $username /home/$username && chmod 600 /home/$username/.pgpass
ENV NVM_DIR=/home/$username/.nvm
RUN corepack enable

### Drupal 11+ requires a minimum sqlite3 version (3.45 currently)
ARG SQLITE_VERSION=3.45.1
RUN log-stderr.sh bash -c "mkdir -p /tmp/sqlite3 && \
wget -O /tmp/sqlite3/sqlite3.deb https://snapshot.debian.org/archive/debian/20240203T152533Z/pool/main/s/sqlite3/sqlite3_${SQLITE_VERSION}-1_${TARGETPLATFORM##linux/}.deb && \
wget -O /tmp/sqlite3/libsqlite3.deb https://snapshot.debian.org/archive/debian/20240203T152533Z/pool/main/s/sqlite3/libsqlite3-0_${SQLITE_VERSION}-1_${TARGETPLATFORM##linux/}.deb && \
apt-get install -y /tmp/sqlite3/*.deb && \
rm -rf /tmp/sqlite3" || true
			
RUN mariadb-client-install.sh || true


### DDEV-injected composer update
RUN export XDEBUG_MODE=off; composer self-update --stable || composer self-update --stable || true; composer self-update --2 || log-stderr.sh composer self-update --2 || true

### DDEV-injected folders permission fix
RUN chmod 777 /run/php /var/log
