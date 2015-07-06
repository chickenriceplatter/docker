run rails application inside docker container
---

1. replace you database.yml with this database.yml
2. copy the Dockerfile to the root of your rails app
3. copy the docker-compose.yml file to the root of your rails app
4. ```$ docker-compose up```
5. run your migrations ```$ docker-compose run web rake db:migrate```
6. seed your database ```$ docker-compose run web rake db:seed```
5. go to port 3000 of ip show in ```$ boot2docker ip```

#### if your ```docker-compose up``` command stops due to bundle install

1. remove your Gemfile.lock: ```$ rm Gemfile.lock```
2. try ```$ docker-compose up``` again



