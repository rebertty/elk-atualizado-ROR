ARG ELK_VERSION

FROM docker.elastic.co/kibana/kibana:${ELK_VERSION}

#Cópia e instalação de plugin ReadOnlyRest no Kibana. Após instalação será efetuada a aplicação do patch.
COPY ./config/readonlyrest_kbn_free-1.35.0_es7.15.0.zip /usr/share/kibana/readonlyrest_kbn_free-1.35.0_es7.15.0.zip
RUN bin/kibana-plugin install file:///usr/share/kibana/readonlyrest_kbn_free-1.35.0_es7.15.0.zip
RUN node/bin/node plugins/readonlyrestkbn/ror-tools.js patch

