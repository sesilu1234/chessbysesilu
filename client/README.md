
<p float="left">
  <img src="../docs/lobby.png" width="400" alt="ChessBySesilu lobby: create or join a game" />
  <img src="../docs/game.png" width="400" alt="A game in progress" />
</p>



# ♟️ WS Server Chess

A lightweight **WebSocket chess server** built in Node.js.  
It manages real-time communication between players, validates moves, and keeps game state synchronized without relying on external frameworks.  
Includes a minimal **HTML/CSS/JS client** to play and test games.

---

## 🚀 Features
- Real-time **WebSocket** connections for two-player games.  
- **Game state management**: tracks board position, turns, and results.  
- **Move validation** to ensure legal chess moves.  
- Minimal **frontend client** (HTML, CSS, JS) included for testing.  
- Optional **persistent storage in AWS (Amazon RDS)** for storing moves or finished games.
- **Game flow options**:
  - Offer/accept **draws**  
  - **Resign** a game  
  - **Save game** to database (AWS RDS) and **resume later**  

---

## 🛠️ Tech Stack
- **Node.js** – server runtime  
- **WebSocket (ws)** – client-server communication  
- **Chess.js** (optional) – for move legality validation  
- **Amazon RDS (PostgreSQL/MySQL)** – managed SQL database in AWS  
- **HTML, CSS, JavaScript** – simple browser client  

---

## 📂 Project Structure
