## Docker-Nginx-Ubuntu12.04

Nginx docker container recipe.

### Dependencies

* [dockerfile/ubuntu](http://dockerfile.github.io/#/ubuntu)


### Installation

Install [Docker](https://gist.github.com/koudaiii/10282062#file-docker_install).
   [for mac](https://gist.github.com/koudaiii/10224422)

### Usage
In Host Machine

    $ git clone https://github.com/koudaiii/docker_nginx_ubuntu.git

Change username to your own

    $ vim ~/docker_nginx_ubuntu/nginx.conf

Change app to your app
   
    $ vim ~/docker_nginx_ubuntu/default

Change dockerfile to your Document_ROOT

    $ vim ~/docker_nginx_ubuntu/Dockerfile

Docker run

    $ docker build -t user/nginx . 

#### Attach persistent/shared directories

    $ docker run -d -p 80 -p 22 -v /var/log/nginx:/var/log/nginx user/nginx

Open `http://<host>` to see the welcome page.
