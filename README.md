# Flask Pipenv Example

Flask application using Pipenv and Docker.

## Running locally

Set up Python environment:

```shell
$ pipenv install
```

To create a virtual environment you just execute the `$ pipenv shell`.

Run a development server:

```shell
$ FLASK_APP=helloworld flask run
```

## Docker image

Build the docker image:

```shell
$ docker build -t flask-pipenv-helloworld .
```

Run the Docker Container:

```shell
$ docker run -p 8000:8000 flask-pipenv-helloworld
```

You can find the container runtime details as shown below:

```shell
$ docker ps
CONTAINER ID        IMAGE                             COMMAND                  CREATED             STATUS              PORTS                      NAMES
80af0bce64c7        flask-pipenv-helloworld           "gunicorn -b0.0.0.0:…"   1 second ago        Up Less than a second   0.0.0.0:8000->8000/tcp     silly_goldstine
```

## Running the tests

Install the prerequisites:

```shell
$ pipenv install --dev
```

Runs tests:

```shell
$ pipenv run python -m pytest
```