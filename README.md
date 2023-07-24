# Localstack docker compose
Launch Localstack to simulate AWS services. See https://docs.localstack.cloud/get-started/#docker-compose
and https://docs.localstack.cloud/localstack/configuration/ for more details.

- The lambdas service require host docker socket to be mounted. The docker compose file attempts to
mount `/var/run/docker.sock` path to the container. This can be overridden using environment variable
`DOCKER_HOST_PATH`.
- Create the `.env` file with following, for example, if using colima on a Mac system.
~~~
DOCKER_HOST_PATH="/Users/user/.colima/default/docker.sock"
~~~
