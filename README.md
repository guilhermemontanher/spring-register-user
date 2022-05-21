# spring-register-user
A demo application that saves a user on Postgres database and send a e-mail verification to confirm de registration

Install mail-dev on docker

```
$ docker pull maildev/maildev
$ docker run -p 1080:1080 -p 1025:1025 maildev/maildev
```

### /registration
```
curl --location --request POST 'localhost:8080/api/v1/registration' \
--header 'Content-Type: application/json' \
--data-raw '{
    "firstName": "Name",
    "lastName": "Lastname",
    "email": "mail@gmail.com",
    "password": "password"
}'
```

### /registration/confirm?token=$TOKEN
```
curl --location --request GET 'localhost:8080/api/v1/registration/confirm?token=$TOKEN' \
--header 'Content-Type: application/json' 
```
