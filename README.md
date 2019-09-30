## fasion EC

### ・environment

#### ・app_server_fasion_ec

- Ruby 2.5.1
- Rails 5.1.6
- Docker (Ruby:2.5.1)
- MySQL 5.6
- API mode

#### ・front_server_fasion_ec

- Node.js 12.8.0
- Nuxt.js
- Docker（node:12.8.0）

#### AWS Architecture

![fasion-ec-infra-architect](https://user-images.githubusercontent.com/45042275/65850902-b77ea380-e38b-11e9-8c6f-a01193d80952.png)


### ・Set Up

git clone
```
$ git clone https://github.com/THitokuse/fasion_ec_docker-compose.git fasion-ec
$ cd fasion-ec
$ git clone https://github.com/THitokuse/app_server_fasion_ec.git
$ git clone https://github.com/THitokuse/front_server_fasion_ec.git
```

create .env file in app_server_fasion_ec dir
```.env
USER=root
PASSWORD=
HOST=db
```

build docker-compose
```
$ docker-compose build
$ docker-compose up -d
```
