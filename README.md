<h1 align="center">Notifications Service</h1>

<p align="center">
  <a href="#features">Features</a> &#xa0; | &#xa0;
  <a href="#technologies">Technologies</a> &#xa0; | &#xa0;
  <a href="#requirements">Requirements</a> &#xa0; | &#xa0;
  <a href="#starting">Starting</a> &#xa0; | &#xa0;
  <a href="#license">License</a> &#xa0; | &#xa0;
  <a href="https://www.linkedin.com/in/alissoonluan/" target="_blank">Author</a>
</p>

<br>

## Features ##

:heavy_check_mark: Create notification;\
:heavy_check_mark: List notification recipient by id;\
:heavy_check_mark: Count notifications from recipient id;\
:heavy_check_mark: Get recipient data from notification id;\
:heavy_check_mark: Cancel notification by id;\
:heavy_check_mark: Mark notification as read;\
:heavy_check_mark: Mark notification as unread;

## Technologies ##

The following tools were used in this project:

- [Nest.js](https://nestjs.com/)
- [Jest.js](https://jestjs.io/)
- [Prisma](https://www.prisma.io/)
- [TypeScript](https://www.typescriptlang.org/)


## Requirements ##

Before starting :checkered_flag:, you need to have [Git](https://git-scm.com) and [Node](https://nodejs.org/en/) installed.

## Starting ##

- Access your terminal
- Execute commands bellow:

  ```bash
  # clone project
  $ git clone https://github.com/alissoonluan/notifications-service

  # Access project folder 
  cd notifications-service
  ```

## Commands to use

```bash
# Execute application
$ yarn start

```

## Url application

The server will initialize in the <http://localhost:3000>

</br>
</br>
</br>

## Routes application ##

- Create (POST): <http://localhost:3000/notifications>

```json

{
 "recipientId": "0dc9af21-4915-4908-b8b1-779a7cad9629",
 "content": "Você tem uma nova notificação",
 "category": "social"
}

```

- Count from recipient (GET): <http://localhost:3000/notifications/count/from/0dc9af21-4915-4908-b8b1-779a7cad9629>

```json
{
  "count": 2
}
```

- Get content from recipient (GET): <http://localhost:3000/notifications/from/0dc9af21-4915-4908-b8b1-779a7cad9629>

```json
{
  "notifications": [
    {
      "id": "e44e7c26-8939-4d22-8834-c539ba2d0949",
      "content": "Você tem conta pra pagar",
      "category": "mega",
      "recipientId": "0dc9af21-4915-4908-b8b1-779a7cad9629"
    },
    {
      "id": "e92af443-40fd-4c86-90a2-069a4cd3b9bf",
      "content": "Você tem conta pra pagar",
      "category": "mega",
      "recipientId": "0dc9af21-4915-4908-b8b1-779a7cad9629"
    }
  ]}
```

- Cancel notification (PATCH): <http://localhost:3000/notifications/0dc9af21-4915-4908-b8b1-779a7cad9629/cancel>
- Mark as read notification (PATCH): <http://localhost:3000/notifications/0dc9af21-4915-4908-b8b1-779a7cad9629/read>
- Mark as unread notification (PATCH): <http://localhost:3000/notifications/0dc9af21-4915-4908-b8b1-779a7cad9629/unread>

## License ##

Made with :heart: by <a href="https://github.com/alissoonluan" target="_blank">Alisson Luan</a>

&#xa0;

<a href="#top">Back to top</a>
