Build Docker container that can access Docker Daemon of the host.
Can be used to spawn sibling container or children container.

Run example:

```sh
docker run -v /var/run/docker.sock:/var/run/docker.sock \
-itd <docker-image-name>
```

To run children spawner, use previlege mode instead of mounting volume.