# FROM uphy/novnc-alpine
FROM ddddv1/nonvcj
#FROM j2
RUN \
    apk add --no-cache curl openjdk8-jre bash \
    && curl -L https://archive.apache.org/dist/jmeter/binaries/apache-jmeter-5.4.1.tgz >  /tmp/jmeter.tgz \
    && mkdir -p /opt \
    && tar -xvf /tmp/jmeter.tgz -C /opt \
    && rm /tmp/jmeter.tgz \
    && cd /etc/supervisor/conf.d \
    && echo '[program:jmeter]' >> supervisord.conf \
    && echo 'command=/opt/apache-jmeter-5.4.1/bin/./jmeter' >> supervisord.conf \
    && echo 'autorestart=true' >> supervisord.conf