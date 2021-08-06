![](https://img.shields.io/badge/Microverse-blueviolet)

# Leaderboard

> App written in JavaScript to submit scores, and to view scores of different players

The objective of this App is to submit scores and grab others from the list of online scores using an API


## Built With

- HTML & CSS
- JavaScript
- VSCode
- Webpack
- Async/Await
- Working with APIs.
- Babel

## Setup

- Get the link of the repository 
- Clone it as `git@github.com:IjayAbby/leaderboard-api.git`

## Info

- For this exercise, a previous game named "Matchmaking Stickman" was created in Insomnia
- This process yielded the id of `0kY85yL0KhloRBs8Qkjq` which was hardcoded in the code

## API Information

- This application uses the [Leaderboard API service](https://www.notion.so/Leaderboard-API-service-24c0c3c116974ac49488d4eb0267ade3) provided by Microverse

- The base URL is `https://us-central1-js-capstone-backend.cloudfunctions.net/api/`

- It has basically 2 endpoints, `/games/` (to create games) and `/games/:id/scores/` (To create and get scores)

- To create a game, send a POST action to the base URL + `/games/` with the name of the game:

```
{
  "name": "This is the name of the new game" 
}
```

- The result will be something like: 
``` 
{
	"result": "Game with ID: Zl4d7IVkemOTTVg2fUdz added."
}
``` 

- To create a new score, send a POST action to the base URL + `/games/:id/scores/` (where id is the previous id of the created game) and the score and user name:

```
{
  "user": "User 1"
  "score": 1000 
}
```

- To get a list of all scores for a specific game, send a GET action to the base URL + `/games/:id/scores/`:

- The response will be something like:

```
{
  "result": [
    {
      "user": "John Doe",
      "score": 42
    },
    {
      "user": "Peter Parker",
      "score": 35
    },
    {
      "user": "Wonder Woman",
      "score": 50
    }
  ]
}
``` 

## Usage

- Run `npm install` on a Terminal to install the modules
- Run `npm run build` on a Terminal to build the assets using webpack
- Run `npm run start` on a Terminal to start the server and look at the result in `localhost:8080`

## Author

👤 **Ijay Abby**

- GitHub: [@IjayAbby](https://github.com/IjayAbby)
- Twitter: [@Ijay_js](https://twitter.com/Ijay_js)
- LinkedIn: [Abigael Nyangasi](https://www.linkedin.com/in/ijayabby4/)


## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

- Microverse
- Webpack Documentation
- MDN Documentation.