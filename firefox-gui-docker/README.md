# Running Firefox GUI Program in Docker Container

### Linux: 
```
docker run --rm -ti --net=host -e DISPLAY=:0 mtabishk/firefox:v1.0.0
```

### macOS: 
```
docker run --rm -ti -e DISPLAY=docker.for.mac.host.internal:0 mtabishk/firefox:v1.0.0
```

### Windows: 
```
docker run --rm -ti -e DISPLAY=host.docker.internal:0 mtabishk/firefox:v1.0.0
```
