# docker-manager
React/Python/Django dashboard manager for docker

## Configure Docker API (for Docker Daemon)

Follow instructions in the link below to configure Docker Daemon on Ubuntu:
https://www.ivankrizsan.se/2016/05/18/enabling-docker-remote-api-on-ubuntu-16-04/

## Configure ```settings.py``` 

Change the following lines to reflect your Docker API configuration:

```
DOCKER_API_PROTOCOL = 'http'
DOCKER_API_IP = '192.168.99.101'
DOCKER_API_PORT = 2375
```

## Finish configuration

Run the following commands to finish the configurarion:

```
(env) > python ./manage.py makemigrations
(env) > python ./manage.py migrate
(env) > python ./manage.py collectstatic
```

## Run Django server

Finally run the server:

```
(env) > python manage.py runserver
```

## Install and run React project

Open another terminal window.

Enter the react project directory:

```
> cd react-dashboard
```

NPM install the react app:

```
> npm install
```

Start react app:

```
> npm start
```

And navigate to web address:

```
http://localhost:3000/
```