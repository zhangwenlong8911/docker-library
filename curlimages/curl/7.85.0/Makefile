# This file is generated by the template.

REGISTRY?=lcr.loongnix.cn
ORGANIZATION?=curlimages
REPOSITORY?=curl
TAG?=7.85.0

IMAGE=$(REGISTRY)/$(ORGANIZATION)/$(REPOSITORY):$(TAG)

default: image

image: source replace build


source: clear
	wget https://github.com/curl/curl/archive/refs/tags/curl-7_85_0.tar.gz
	tar -xzf curl-7_85_0.tar.gz
	mv curl-curl-7_85_0 curl
	rm -rf curl-7_85_0.tar.gz

TARGET_FILE_PATH:=curl/lib
TARGET_FILE:=easy_lock.h

replace:
	rm $(TARGET_FILE_PATH)/$(TARGET_FILE) 
	cp $(TARGET_FILE) $(TARGET_FILE_PATH)/	

build:
	docker build --no-cache \
		-t $(IMAGE) \
		.

push:
	docker push $(IMAGE)

clear:
	rm -rf curl
