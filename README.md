# StringsDemoRoot

## Prequesites
[docker](https://docs.docker.com/get-docker/) & [docker-compose](https://docs.docker.com/compose/install/) must be installed

## Installation
```sh
mkdir -p $GOPATH/src/github.com/xakepp35
cd $GOPATH/src/github.com/xakepp35
git clone https://github.com/xakepp35/StringRandomizerDemo
git clone https://github.com/xakepp35/StringEncryptorDemo
git clone https://github.com/xakepp35/StringsDemoRoot
cd StringsDemoRoot
docker-compose build
docker-compose up
```
This would build & start 2 microservices
On some environment you'll have to use `sudo` with `docker-compose` commands (unless your user is not added to group docker)

## Usage
1) Open browser
2) Type `localhost:6002/20` where `20` is number of wanted strings, press enter
It would: 
 - Generate 20 random strings of length 10-30 characters
 - Send them to encryptor microservice via websocket
 - Await for sha-256 response from encryptor worker pool
 - Output them as raw text in browser

All env configuration is stored in `StringsDemoRoot/docker-compose.yml` file
Good luck ;-D