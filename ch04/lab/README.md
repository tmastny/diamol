# Step 1

```bash
docker image build -t lab4_1 .
docker image ls | grep lab4_1
> 736 mb 
```

Run and test:
```bash
docker container run -d -p 802:80 lab4_1                       
```
Visit at `http://localhost:802/`.

Add environment variable:
```bash
docker container run -d -p 802:80 -e USER=timmastny lab4_1 
```

# Step 2

Multistage Dockerfile, copying binary into `diamol/base`:
```bash
docker image build -t lab4_2 .
docker image ls | grep lab4_2
> 25.9mb
```

Moved `COPY index.html .` to the bottom of the file,
so every other step can be cached.
