<h1 align="center">
  <b>docker-php-intro-project</b>
</h1>
<p>This is an introduction project to working with PHP and Docker. The image that is being used for PHP is the 8.2 version. The image also contains the APACHE Web Server.</p>



# Instructions
### Build Docker Image:
```bash
docker build -t php-docker-intro .
```

### Start the Container:
```bash
docker run -d -p 12500:80 --name php-docker-container php-docker-intro
```

### Stop the Container:
```bash
docker stop php-docker-container
```

### Delete the Container:
```bash
docker rm php-docker-container
```

# Deploying images to Docker Hub (First you have to log in to Docker Hub)

```bash
docker tag php-docker-intro <your_dockerhub_username>/php-docker-intro:latest

docker push <your_dockerhub_username>/php-docker-intro:latest
```