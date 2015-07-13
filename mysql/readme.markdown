mysql in docker
===

command to create a mysql container
---

  ```bash
  docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:tag

  # make port 3306 available
  docker run -p 3306:3306 --name mysql_container -e MYSQL_ROOT_PASSWORD=somepassword -d mysql:5.5
  ```

connect to containerized mysql using sequel pro
---
![sequel pro instructions](./docker_sequel_pro.png)
