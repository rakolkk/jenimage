# contanrizeApp
python flask app to docker container image with redis db


to run ex commands

docker build -t newapp:0.1 .
docker images

#make sure --name & --link must be same because it is used in code


docker run --name=redis -d redis

docker run -d -p 5000:5000 --link=redis --name=newapp1 newapp:0.1

curl localhost:5000
