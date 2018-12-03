# Envoy Example

## Testing Envoy Simple Example

```bash
docker pull envoyproxy/envoy:latest
docker run --rm -d -p 10000:10000 envoyproxy/envoy:latest
curl -v localhost:10000
```

Building the envoy docker container:
```bash
docker build -t envoy-example:v1 .
```

Running the envoy docker container:
```bash
docker run -d --name envoy-example-v1 -p 9901:9901 -p 10000:10000 envoy-example:v1
```

Test it:
```bash
curl -v localhost:10000
```
