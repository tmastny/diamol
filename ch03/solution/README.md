Copy file over (like last time) or

```bash
docker run -it diamol/ch03-lab
```

Edit the file (no nano or vim, I used echo).

Then commit your change:
```bash
docker container commit 37e81bd32bbf lab-change:v1
```
