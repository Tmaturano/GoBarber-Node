# GoBarber-Node

## How to run

#### Since this project is using sucrase to work with import / export default syntax, running node src/server.js will not work, so:

- yarn sucrase-node src/server.js
- Or with Nodemon: yarn dev (that will use sucrase-node)
