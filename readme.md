# Backend Tickitz with Golang

<br>
<br>
<div align="center">
  <img src="https://res.cloudinary.com/doncmmfaa/image/upload/v1705476761/samples/Tickitz_1_qjg2bh.png" alt="Logo" width="340" height="100"/>
</div>
<br>
<br>
This project is about to show you on my performance in developing backend architecture using Golang. It has couple of features and API also several security authorization. It is a website for purchasing cinema tickets with main features including a list of films and their details, ordering cinema tickets based on the desired time and place. There are 2 roles, namely Consumer and Admin. Its has authentication and authorization for several accessible pages based on role.

## Technologies used in this project

- [Gin Gonic](https://pkg.go.dev/github.com/gin-gonic/gin#section-readme) \
  A lightweight and fast web framework for Golang. \

- [JSON Web Token](https://jwt.io/introduction) \
  Provide a secure and compact way to transmit information between parties. \

- [Cloudinary](https://cloudinary.com/documentation) \
  A cloud-based service for managing and optimizing images and videos. \

- [Midtrans](https://docs.midtrans.com/) \
  A payment gateway service that simplifies online transactions. \

## Environment Variables

To run this project, you will need to add the following environment variables to your .env file in your root directory

```bash
  DB_HOST = "YOUR DB_HOST"
  DB_NAME = "YOUR DB_NAME"
  DB_USER = "YOUR DB_USER"
  DB_PASSWORD = "YOUR DB_PASSWORD"
  JWT_KEY = "YOUR JWT_KEY"
  ISSUER = "YOUR ISSUER"
  CLOUDINARY_NAME = "YOUR CLOUDINARY_NAME"
  CLOUDINARY_KEY = "YOUR CLOUDINARY_KEY"
  CLOUDINARY_SECRET = "YOUR CLOUDINARY_SECRET"
  MIDTRANS_ID_MERCHANT = "YOUR MIDTRANS_ID_MERCHANT"
  MIDTRANS_CLIENT_KEY = "YOUR MIDTRANS_CLIENT_KEY"
  MIDTRANS_SERVER_KEY = "YOUR MIDTRANS_SERVER_KEY"
```

## Run Locally

1. Clone the project

```bash
  $ git clone https://github.com/GilangRizaltin/Tickitz-Golang
```

2. Go to the project directory

```bash
  $ cd Tickitz-Golang
```

3. Install dependencies

```bash
  $ go get .
```

4. Start the server

```bash
  $ go run ./cmd/main.go
```

## Running Tests

To run tests, run the following command

```bash
  $ go test .
```

## API Reference

#### Authentication & Authorization

| Method   | Endpoint           | Description                        |
| :------- | :----------------- | :--------------------------------- |
| `POST`   | `"/auth/register"` | register user                      |
| `POST`   | `"/auth/login"`    | get access and identity of user    |
| `DELETE` | `"/auth/logout"`   | delete access and identity of user |

#### Users

| Method  | Endpoint                | Description                     |
| :------ | :---------------------- | :------------------------------ |
| `GET`   | `"/user/profile"`       | Fet user's profile              |
| `POST`  | `"/user/authorization"` | Checking user's authorization   |
| `PATCH` | `"/user"`               | Update users detail and profile |

#### Movie

| Method | Endpoint                      | Description                              |
| :----- | :---------------------------- | :--------------------------------------- |
| `GET`  | `"/movie"`                    | GET all movie                            |
| `GET`  | `"/movie/movie/:movie_id"`    | Get movie details **Required** movie_id  |
| `GET`  | `"/movie/schedule/:movie_id"` | Get movie schedule **Required** movie_id |

#### Orders

| Method | Endpoint                | Description                              |
| :----- | :---------------------- | :--------------------------------------- |
| `GET`  | `"/order"`              | Get orders per users                     |
| `POST` | `"/order"`              | Create transaction order                 |
| `POST` | `"/order/notification"` | Push notification for sucessfull payment |

## Documentation

[Postman Documentation](https://documenter.getpostman.com/view/29696636/2s9Ykn8MDe)

## Related Project

[Front End (React Js)](https://github.com/GilangRizaltin/Tickitz-Frontend-Gilang)

## Collaborator

- [@Ridwan Bahtiar](https://github.com/ridwanbahtiar15)

## Support

For support, email gilangzaltin@gmail.com
