# [Innonymous](https://innonymous.tk/)

> IMPORTANT NOTE FOR THOSE WHO CHECK OUR WORK IN INNOPOLIS: this readme only for brief view of project. All important information for grading you can find in our docs: https://innonymous.rtfd.io

<img src="docs/src/images/logo.png" align="left" width=100 style="margin: 0px 10px 0px 0px"> Innonymous is mobile-ready open-source light-weight and anonymous chat. Backend in [python FastAPI](https://fastapi.tiangolo.com/), client-side in [ReastJS](https://reactjs.org/), using web-sockets. Persistant storages are postgres and rabbitmq. Backend has anti spam registration using auto-generated CAPTCHA.

<br>

Since we have clear and easy [documentation](https://innonymous.tk/api/docs) (powered by swagger) you can use our backend and create your own client-side application! 

<br>

## Source code

You may notice that this repo does not have any source code. We decided to split backend, frontend and main repo. Here you can find all links:

+ API Server - https://github.com/innonymous/api-server
+ Web Client - https://github.com/innonymous/web-client
+ Compose (this repo) - https://github.com/innonymous/compose

## Screenshots

Demo of project - [here](https://www.loom.com/share/6995e1a95db54426879e03e139dd61d5)

Desktop version:
<p align="center">
<img src="docs/src/images/app_example1.png" width="800px" />
</p>

Mobile version:
<p align="center">
<img src="docs/src/images/app_example2.jpg" width="400px" />
</p>


## Quick start

We alreay pushed Innonymous to production: https://innonymous.tk/ **(We DO NOT accept any responsibility for the content of the site. Anyone and anything can write)**



However you can start your own version of Innonymous! It is as easy as 1-2-3:

1. [Install Docker and Docker Compose](https://docs.docker.com/get-docker/) if you don't have it already
    * On Mac and Windows, Docker comes with Docker Compose
    * On Linux you need to install Docker Engine and Docker Compose separately

2. Configure `.env` file:
```sh
$ cp .env.example .env
```
|env variable|description|example|
|--|--|--|
|AMQP_PASSWORD| RabbitMQ in docker container will use it, so this password only for infrastructure usage. However you should keep it in secret. |mycoolpassword1|
|DATABASE_PASSWORD| Infra password for postgres |mycoolpassword2|
|API_KEY| 32 bytes in hex, can be generated as `openssl rand -hex 32` for backend JWT generation |12345678901234567890123456789012|
|API_PORT| port for api. can be any free port| 8000 |
|WEB_PORT| port of web service (client side app)| 8080|



3. Now start the whole project. You can add `-d` flag to run in daemon mode:

```sh
$ docker pull smthngslv/innonymous-web-client
$ docker pull smthngslv/innonymous-api-server
$ docker-compose up
```

Done! Now go to `localhost:8080` and test your chat!

<hr>
<br>

<center> 

*You can say and write whatever you think, but you should think carefully* 

</center>