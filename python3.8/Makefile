.PHONY: build publish run test

build:
	sudo docker build . -t python:3.8-ubuntu 
	sudo docker image tag python:3.8-ubuntu  tonghs/python:3.8-ubuntu 

publish:
	sudo docker push tonghs/python -a
