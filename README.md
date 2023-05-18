# Laravel Google Cloud Buildpacks

# Build
```bash
pack build laravel-app --builder=gcr.io/buildpacks/builder \                           
  --env GOOGLE_COMPOSER_VERSION="2.2.20"  \
  --env GOOGLE_RUNTIME="php"
  
or

gcloud builds submit --pack image={REGION}-docker.pkg.dev/{PROJECT_ID}/{REPO_NAME}/laravel-app
```

# Run
```bash
docker run -it --init --platform linux/amd64 
  -e APP_DEBUG=  \
  -p 8080:8080  \
  laravel-app:latest 
```
