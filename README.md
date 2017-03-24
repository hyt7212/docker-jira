JIRA 7.2.7 for docker 汉化版
===
+ jira7.2.7
+ mysql <= 5.6

```yml
version: '2'
services:
  jira:
    image: hyt7212/jira:7.2.7
    ports:
      - 8080:8080
    restart: always
  mysql5.6:
      restart: always
      image: mysql:5.6
      ports:
        - "3307:3306"
      volumes:
        - ./mysql:/var/lib/mysql
        - ./mysql/my.cnf:/etc/mysql/my.cnf
      environment:
        MYSQL_ROOT_PASSWORD: 123456
```