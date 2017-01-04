To run docker commands from a consul-template Docker container.

## A use case

We run Haproxy using `docker-compose`. To restart Haproxy when its bind-mounted template changes, consul-template needs access to docker to send the `HUP` signal. This way, we can use the official haproxy Docker image which handles restarts gracefully based a signal.

## Usage

```
docker run nextjournal/consul-template-docker -f....
```
