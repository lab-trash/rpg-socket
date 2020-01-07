# Blacksmith Project: RPG - Socket

This is a small node server handling a list of players / game.

Receiving a notice of connection to a game from player (Client), node server will send a message to a Mercure server.

Client should emit on websocket, and listen on Mercure to get the list of connected players.

## Why ?

Mercure is currently not able to provide a list of connected clients on a topic. This is a workaround.

## How to use it:
- Client MUST connect Player on `ws://localhost:3000` _(remember to put the right url here)_.

- Client MUST provide a `gameId` in the query.

_Example:_
```
const socket = io.connect('ws://localhost:3000', { query: `gameId=${gameId}` });
```

- Client MUST provide an object as Player. (An id and a name is good)