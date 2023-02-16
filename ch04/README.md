Built a networked set of APIs:

```bash
docker container run --name iotd -d -p 800:80 --network nat image-of-the-day
docker container run --name accesslog -d -p 801:80 --network nat access-log
docker container run -d -p 802:80 --network nat image-gallery
```

The first two apps are hosted on the docker virtual network at:
```
http://iotd/image
http://accesslog/access-log
```

The root domain is the name the container and the path
is managed by the application code in Java and JS respectively.

The `go` app calls these APIs and posts the image to the net.

