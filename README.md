# spring-register-user
A demo application that saves a user on Postgres database and send a e-mail verification to confirm de registration


Pre-configs

Install mail-dev on docker

$ docker pull maildev/maildev
$ docker run -p 1080:1080 -p 1025:1025 maildev/maildev
