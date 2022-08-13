# Game Stats API

A public API to fetch information about an online game server. This API has over 295+ games server's information including player list and much more!

## API Calling
Our main API endpoint is: **`https://gamestats.tk`**

*Please use the endpoint as a prefix of all API URLs.*

---
- ### Fetching Server Status


```http
GET /api/stats?game=<GAME_NAME_ID>&ip=<YOUR_SERVER_IP>&port=<YOUR_SERVER_PORT>
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `game` | `string` | **Required**. ID of the game of the server. [gamestats.tk/games](https://gamestats.tk/games "Game ID List") for the list of IDs |
| `ip` | `string` | **Required**. IP of the server |
| `port` | `number` | **Optional**. Port of the server |

---
- ### Fetching Server Player List

```http
GET /api/players?game=<GAME_NAME_ID>&ip=<YOUR_SERVER_IP>&port=<YOUR_SERVER_PORT>
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `game` | `string` | **Required**. ID of the game of the server. [gamestats.tk/games](https://gamestats.tk/games "Game ID List") for the list of IDs |
| `ip` | `string` | **Required**. IP of the server |
| `port` | `number` | **Optional**. Port of the server |

## Responses
Game Stats will return raw json as a response for every request you send.

## Status Codes

Gophish returns the following status codes in its API:

| Status Code | Description |
| :--- | :--- |
| 202 | `OK` |
| 404 | `NOT FOUND OR ERROR` |
