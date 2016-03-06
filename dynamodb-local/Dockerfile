# DynamoDB Local

FROM pottava/java:8

MAINTAINER lulichn <daisuke.develop@gmail.com>

RUN set -ex \
	&& apk --no-cache add --virtual curl \
	&& cd /usr/local/ \
	&& curl -OL http://dynamodb-local.s3-website-us-west-2.amazonaws.com/dynamodb_local_latest.tar.gz \
	&& mkdir dynamo \
	&& tar xfz dynamodb_local_latest.tar.gz -C dynamo \
	&& rm -rf dynamodb_local_latest.tar.gz \
	&& apk del curl

WORKDIR /usr/local/dynamo

EXPOSE 8000

ENV DYNAMO_OPT=""

CMD java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar $DYNAMO_OPT
