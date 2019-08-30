# GoBarber-Node

## How to run

#### Since this project is using sucrase to work with import / export default syntax, running node src/server.js will not work, so:

- yarn sucrase-node src/server.js
- Or with Nodemon: yarn dev (that will use sucrase-node)

#### Database:

- Postgresql with docker
- docker run --name postgres -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres to get the Postgres image and set up
- Open a command prompt and run "docker ps" to check if the container is running (named postgres)
- Download a visual interface to see the data in Postgres (I like https://electronjs.org/apps/postbird)
- To stop the container, just run: "docker stop postgres"
- To run again the container, just run : "docker start postgres"

## Setup

#### EsLint / Prettier:

- The file .eslintrc.js has some configurations using AirBnB style and prettier
- The Line-break mode is configured for Windows
- The file .prettierrc is needed because eslint and prettier conflicts in some cases (for example single quote)
- To avoid opening one by one .js files and saving to let eslint fix with the rules, just run the command: "yarn eslint --fix src --ext .js"