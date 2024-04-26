Build Docker container that can access Docker Daemon of the host.
Can be used to spawn sibling container or children container.

Example command:

```sh
docker run -v /var/run/docker.sock:/var/run/docker.sock \
-itd <docker-image-name>
```

To run children spawner, use privileged mode instead of mounting volume.


```sh
docker run --privileged -itd <docker-image-name>
```