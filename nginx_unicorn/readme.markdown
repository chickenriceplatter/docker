production rails container using nginx and unicorn
===

1. make sure you have ```gem 'unicorn'``` in your Gemfile
2. replace your database.yml with the database.yml in this directory.
3. copy unicorn.rb into the config directory of your rails project.
4. add ```default```, ```Dockerfile```, ```entrypoint.sh``` and ```nginx.conf``` to the root of your rails project.
5. cd into the root of your rails project.
6. run ```docker build -t nginx_unicorn .```
7. run ```docker run -P --name db -d -t postgres:latest```
8. run ```docker run -d -p 80:80 --link db:postgres nginx_unicorn```
9. go to your boot2docker ip address and you should see your application up and running.
