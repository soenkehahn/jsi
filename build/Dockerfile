FROM golang:1.8.5-jessie
RUN apt-get update --yes && apt-get install --yes upx-ucl

ADD ./src/ /root/jsi/src/
ADD ./build/ /root/jsi/build/

WORKDIR /root/jsi
CMD ./build/build.sh && tar cvf dist.tar dist 1>&2 && cat ./dist.tar
