ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}
COPY ./config/readonlyrest-1.35.0_es7.15.0.zip /usr/share/elasticsearch/readonlyrest-1.35.0_es7.15.0.zip
RUN bin/elasticsearch-plugin install --batch file:///usr/share/elasticsearch/readonlyrest-1.35.0_es7.15.0.zip
# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
