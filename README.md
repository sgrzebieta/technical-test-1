# Multistage Build Dockerfile Example

This is a technical test to demonstrate how to optimize a standard Dockerfile into a Multistage Dockerfile

## About

This is a simple go http server which will expose 3 different endpoints

- `/` will return a Hello a greeting.
- `/go` will return a Go proverb.
- `/opt` will return an optimization truth.


## Building
To build this image run the following docker command

```bash
docker build . -t <tag-name>
```

## Testing
To run the image execute the following docker command

```bash
docker run -p 80:8000 <tag-name>
```

To test the 3 endpoint run the following curl commands

```
curl http://localhost/
Hello, world.

curl http://localhost/go
Don't communicate by sharing memory, share memory by communicating.

curl http://localhost/opt
If a program is too slow, it must have a loop.
```
