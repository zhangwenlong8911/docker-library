default: image

image:
	docker build \
		--build-arg http_proxy=$(http_proxy) \
		--build-arg https_proxy=$(https_proxy) \
		-t lcr.loongnix.cn/library/redis:8.0.2-alpine \
		-t lcr.loongnix.cn/library/redis:8.0.2-alpine3.21 \
		.

push:
	docker push lcr.loongnix.cn/library/redis:8.0.2-alpine
	docker push lcr.loongnix.cn/library/redis:8.0.2-alpine3.21
