.POSIX:

TAG = homelab-tools
PROJECT_DIR = ${shell pwd}/..

default: build run

build:
	@docker build . --tag ${TAG}

run:
	@docker run \
		--rm \
		--interactive \
		--tty \
		--network host \
		--volume "${PROJECT_DIR}:${PROJECT_DIR}" \
		--volume "/var/run/docker.sock:/var/run/docker.sock" \
		--workdir "${PROJECT_DIR}" \
		${TAG}
