FROM python:2.7-alpine

RUN apk add git g++
# g++ required to build Brotli

WORKDIR /opt/crs
RUN git clone https://github.com/coreruleset/coreruleset.git /opt/crs
RUN git checkout v3.3/master && ln -s /opt/crs/tests/regression /opt/ftw/crs-tests

RUN cd tests/regression && pip install -r requirements.txt

CMD [/bin/bash]
