default: image

image:
	docker build \
		--build-arg http_proxy=$(http_proxy) \
		--build-arg https_proxy=$(https_proxy) \
		-t lcr.loongnix.cn/library/redis:7.0.4 \
		-t lcr.loongnix.cn/library/redis:7.0.4-trixie \
		.

push:
	docker push lcr.loongnix.cn/library/redis:7.0.4
	docker push lcr.loongnix.cn/library/redis:7.0.4-trixie
