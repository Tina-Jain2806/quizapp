The project is inspired by the [Kahoot](https://kahoot.com) app. The main functionality of the application is the creation of educational games in the form of quizzes, which then can be solved by several students at the same time in the form of a game. Quizzes can be created with the use of a special wizard that allows you to select the type of question, determine the method of awarding points and answer time for a particular question, and the number of correct answers. During the quiz, the teacher acts as the host who creates a room that students can access using an access code. During the game, students see the scoreboards after each question in real time. Quizzes are divided into public and private. Each logged in user can view the list of public quizzes, add likes and comments to them.

## Installation

Client side

```bash
cd client
npm install
```

Server side

```bash
cd server
npm install
```

## Run the app

You need four terminal instances - one for client app and three for backend servers.

```bash
cd client
npm start
```

```bash
cd server
npm run devStart
```

```bash
cd server
npm run devStartAuth
```

```bash
cd server
npm run devStartSocket
```

## Generate JWT tokens

```bash
ssh-keygen -t rsa -b 4096 -m PEM -f jwtRS256.key
# Don't add passphrase
openssl rsa -in jwtRS256.key -pubout -outform PEM -out jwtRS256.key.pub
cat jwtRS256.key
cat jwtRS256.key.pub
```

## Env configuration

```
DATABASE_URL=string (required)
PORT=3000 (required number)
AUTH_PORT=4000 (required number)
ACCESS_TOKEN_SECRET=string (required string)
REFRESH_TOKEN_SECRET=string (required string)
```

