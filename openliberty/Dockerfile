FROM adoptopenjdk/openjdk12-openj9:jdk-12.0.1_12_openj9-0.14.1-alpine-slim
LABEL maintainer="Jose Amadeo Martin Diaz Diaz"

ENV RELEASE 2019-08-25_1901
ENV VERSION 19.0.0.9-cl190920190825-1901

RUN apk add curl

RUN curl https://public.dhe.ibm.com/ibmdl/export/pub/software/openliberty/runtime/nightly/${RELEASE}/openliberty-all-${VERSION}.zip -L -o openliberty.zip \
    && unzip openliberty.zip -d /opt \
    && rm openliberty.zip

ENV INSTALL_DIR /opt/wlp/
ENV CONFIG_DIR /opt/wlp/usr/servers/defaultServer/
ENV DEPLOYMENT_DIR /opt/wlp/usr/servers/defaultServer/dropins/

COPY server.xml ${CONFIG_DIR}configDropins/defaults/

CMD ["/opt/wlp/bin/server", "run", "defaultServer"]



