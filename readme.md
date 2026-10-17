# create a new image from exsting project

docker buildx build --platform linux/amd64,linux/arm64 -t nodejs-image-test:v2 . 


docker tag nodejs-image-test:v2 lebondeveloppeur/nodejs-image-test:v2

docker run -d -p 3003:3000 nodejs-image-test:v2

docker push lebondeveloppeur/nodejs-image-test:v2



# use image from docker hub
docker pull mongo:latest
docker run -d -p 5001:27017 mongo:latest