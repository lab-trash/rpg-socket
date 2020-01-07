# Blacksmith Project: RPG - Socket

This is a small node server handling a list of players / game.

## How to use it:
- Client MUST connect Player on `ws://localhost:3000` _(remember to put the right url here)_.

- Client MUST provide a `gameId` in the query.

_Example:_
```
const socket = io.connect('ws://localhost:3000', { query: `gameId=${gameId}` });
```

- Client MUST provide an object as Player. (An id and a name is good)