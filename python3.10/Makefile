.PHONY: build publish run test


build:
	sudo docker build . -t python:3.10-ubuntu 

build-amd64: build
	sudo docker image tag python:3.10-ubuntu  tonghs/python:3.10-ubuntu-amd64

build-m1: build
	sudo docker image tag python:3.10-ubuntu  tonghs/python:3.10-ubuntu-m1 

create-manifest:
	docker manifest create tonghs/python:3.10-ubuntu tonghs/python:3.10-ubuntu-amd64 tonghs/python:3.10-ubuntu-m1

push-manifest:
	docker manifest push tonghs/python:3.10-ubuntu

publish:
	sudo docker push tonghs/python -a
