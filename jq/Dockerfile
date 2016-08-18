FROM alpine
RUN apk update && apk add build-base
ADD https://github.com/stedolan/jq/releases/download/jq-1.5/jq-1.5.tar.gz .
RUN zcat jq-1.5.tar.gz | tar xvf - && cd jq-1.5 && ./configure && make && make install
ENTRYPOINT ["jq"]
