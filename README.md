<p float="left">
  <img src="https://github.com/user-attachments/assets/f8e79fd4-cca4-45b8-a034-d27bf2c49f90" width="400" />
  <img src="https://github.com/user-attachments/assets/20eb5523-7b62-41a2-ba31-432f656e50b3" width="400" />
</p>

# ♟️ ChessBySesilu

Real-time online chess, built from scratch without frameworks. Create a private match, share the code with a friend and play.

**Live:** [chessbysesilu.com](https://www.chessbysesilu.com)

## How it fits together

```
browser (vanilla JS client)  ⇄  wss://chessbysesilu.com/ws/  ⇄  Nginx  ⇄  Node.js WebSocket server  ⇄  MySQL / MongoDB
```

| Folder | What's inside |
|---|---|
| [`client/`](client) | Vanilla HTML/CSS/JS client: board, game logic, sounds and piece artwork |
| [`server/`](server) | Node.js WebSocket server (`ws`): lobby and match codes, real-time move relay, draws/resign, saving games |

Self-hosted on **AWS EC2** behind an **Nginx** reverse proxy with TLS.

## Tech stack

- **Client:** HTML, CSS, vanilla JavaScript
- **Server:** Node.js, `ws`, `mysql2`, `mongodb`, `dotenv`
- **Data:** MySQL (Amazon RDS), MongoDB
- **Infra:** AWS EC2, Nginx

## Running the server locally

```bash
cd server
npm install ws mysql2 mongodb dotenv
cp .env.example .env   # fill in your database settings
node ws_chess_2.js
```

The client is static: serve `client/` with any web server and point the WebSocket URL in `chess_vani_WS.js` at your server.

---

This repo merges the former `chess_game` (client) and `ws_server_chess` (server) repositories, keeping their full commit history.
