# lab solution attempt

## File Mount

First, let's figure out how to run the todo app with a local file:
```bash
docker container run --mount type=bind,source=$(pwd)/data,target=/data -d -p 8012:80 diamol/ch06-todo-list
```
Pretty easy translation to [docker-compose](https://docs.docker.com/compose/compose-file/#volumes).

## Application Restart

Next, how do make the application restart if the machine reboots or engine restart.
Turns out, all you need is a simple [restart key](https://docs.docker.com/compose/compose-file/#restart) on the image.

## Test

Finally, app should listen on port 80 for test (tbh I don't know what this means atm).



