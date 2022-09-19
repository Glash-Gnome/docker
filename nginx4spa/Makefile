#

all: build create start exec stop rm rmi

compose:
	@set -x; \
	USER_ID=$(shell id -u) \
	GROUP_ID=$(shell id -g) \
	docker-compose build
	@set -x; docker-compose up
	@set -x; docker-compose down

build:
	@set -x; \
	docker build \
	  --file ./Dockerfile \
	  --tag spa-image \
	  --build-arg USER_ID=$(shell id -u) \
	  --build-arg GROUP_ID=$(shell id -g) \
	  .

create:
	@set -x; \
	docker container create \
	  --name spa-container_1 \
	  spa-image:latest

start:
	@set -x; docker container start spa-container_1

exec:
	@set -x; docker container exec spa-container_1 ash

stop:
	@set -x; docker container stop spa-container_1

rm:
	@set -x; docker container rm spa-container_1

rmi:
	@set -x; docker image rm spa-image
