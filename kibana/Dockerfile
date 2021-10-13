ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/kibana/kibana:${ELK_VERSION}
COPY ./config/readonlyrest_kbn_free-1.35.0_es7.15.0.zip /usr/share/kibana/readonlyrest_kbn_free-1.35.0_es7.15.0.zip
RUN bin/kibana-plugin install file:///usr/share/kibana/readonlyrest_kbn_free-1.35.0_es7.15.0.zip
RUN node/bin/node plugins/readonlyrestkbn/ror-tools.js patch
# Add your kibana plugins setup here
# Example: RUN kibana-plugin install <name|url>
