# Laravel Google Cloud Buildpacks

# Build
```bash
pack build laravel-php --builder=gcr.io/buildpacks/builder \                           
  --env GOOGLE_COMPOSER_VERSION="2.2.20"  \
  --env GOOGLE_RUNTIME="php"
```

# Run
```bash
docker run -it --init --platform linux/amd64 
  -e APP_DEBUG=  \
  -p 8080:8080  \
  laravel-php:latest 
```
