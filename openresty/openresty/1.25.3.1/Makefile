# This file is generated by the template.

REGISTRY?=lcr.loongnix.cn
ORGANIZATION?=openresty
REPOSITORY?=openresty
VERSION?=1.25.3.1

IMAGE=$(REGISTRY)/$(ORGANIZATION)/$(REPOSITORY):$(VERSION)

default: image

image:
	docker build \
		--build-arg http_proxy=$(https_proxy) \
		--build-arg https_proxy=$(https_proxy) \
		-t $(IMAGE) \
		-t $(IMAGE)-buster \
		.

push:
	docker push $(IMAGE)
	docker push $(IMAGE)-buster
