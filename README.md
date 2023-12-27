# User Management API

This project is a User Management API built with Node.js and MongoDB. It allows for user registration, login, and management of a user's favourite items and history.

## API Reference

#### Register a new user

```
  POST /api/user/register
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userName` | `string` | **Required**. The username of the new user |
| `password` | `string` | **Required**. The password of the new user |
| `password2` | `string` | **Required**. Confirmation of the password |

#### Login a user

```
  POST /api/user/login
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `userName` | `string` | **Required**. The username of the user |
| `password` | `string` | **Required**. The password of the user |

#### Get a user's favourites

```
  GET /api/user/favourites
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of user to fetch favourites |

#### Add a favourite for a user

```
  PUT /api/user/favourites/:id
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of user to add favourite |
| `favId`   | `string` | **Required**. Id of favourite to add |

#### Remove a favourite for a user

```
  DELETE /api/user/favourites/:id
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of user to remove favourite |
| `favId`   | `string` | **Required**. Id of favourite to remove |

#### Get a user's history

```
  GET /api/user/history
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of user to fetch history |

#### Add a history for a user

```
  PUT /api/user/history/:id
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of user to add history |
| `historyId`   | `string` | **Required**. Id of history to add |

#### Remove a history for a user

```
  DELETE /api/user/history/:id
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of user to remove history |
| `historyId`   | `string` | **Required**. Id of history to remove |

## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`MONGO_URL`
`JWT_SECRET`

## Run Locally

Clone the project

```
  git clone https://github.com/benakram4/user-api.git
```

Install dependencies

```
  npm install
```

Start the server

```
  npm run start
```
