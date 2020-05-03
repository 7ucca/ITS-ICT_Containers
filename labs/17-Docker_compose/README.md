# Docker Compose

Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration.

## Prerequisites

Having installed:

- [Docker](https://docs.docker.com/docker-for-windows/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)


## Instance a multi container application with Docker Compose

Start containers

```console
$ docker-compose -f docker-compose.yml up -d
Recreating 13dockercompose_db_1 ... done
Recreating 13dockercompose_wordpress_1 ... done
```

If you point your browser to http://\<DOCKER HOST\>:8000/ you should see the WordPress installation page.

Go ahead installing WordPress, you will see that MySQL container has been created too.

## Remove containers

Finally, remove the containers

```console
$ docker-compose -f docker-compose.yml down -v
Removing network 13dockercompose_default
Removing volume 13dockercompose_db_data
```