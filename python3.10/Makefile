.PHONY: build publish run test


build:
	sudo docker build . -t python:3.10-ubuntu 

build-amd64: build
	sudo docker image tag python:3.10-ubuntu  tonghs/python:3.10-ubuntu 

build-m1: build
	sudo docker image tag python:3.10-ubuntu  tonghs/python:3.10-ubuntu-m1 

publish:
	sudo docker push tonghs/python -a
