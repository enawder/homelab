.POSIX:

TAG = homelab-tools

default: build run

build:
	@docker build . --tag ${TAG}

run:
	@docker run \
		--rm \
		--interactive \
		--tty \
		--network host \
		--volume "${shell pwd}/..:/home" \
		--workdir "/home" \
		${TAG}
