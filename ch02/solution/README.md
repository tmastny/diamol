Start the server container (will be a different id)
```bash
docker container start b50335bf34ce
```

Copy `index.html` into the path. The existing one will be replaced:
```bash
docker cp index.html b50335bf34ce:/usr/local/apache2/htdocs
```
