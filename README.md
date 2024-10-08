# Chat Room Application

Welcome to the **Real-Time Chat Room Application**! This application features a backend built with Go (utilizing WebSocket for real-time communication) and a frontend developed in React, providing an engaging user interface.
![image](https://github.com/nixysoft/go-chat/blob/main/Capture.PNG)
## Project Structure

```bash
.
├── real-time-chat/    # Go (Golang) WebSocket server (backend)
├── chatroom/          # React frontend for the chat room
└── README.md          # Project documentation
```
## Prerequisites
Before getting started, please ensure you have the following installed on your machine:

 - Go: Version 1.16 or higher.
 - Node.js: Version 14 or higher is recommended, along with npm.

## Setting Up the Go Backend (real-time-chat)
The Go backend functions as a WebSocket server that facilitates real-time communication.

### Steps to Run the Backend:

1. **Open your terminal and navigate to the real-time-chat/ directory**:
```bash
cd real-time-chat/
```
2. **Install any necessary dependencies:**:
```bash
go mod tidy
```
3. **Start the server**:
```bash
go run main.go
```
4. **To cross-compile the binary for a different platform, you can use the following commands**:
```bash
GOOS=windows GOARCH=amd64 go build -o chatroom.exe main.go # For Windows
GOOS=linux GOARCH=amd64 go build -o chatroom main.go # For Linux
```
Your backend WebSocket server will now be running at ws://localhost:8080/ws.

### Backend File Structure
```bash
real-time-chat/
├── main.go           # Entry point for the WebSocket server
├── handlers.go       # Contains WebSocket handlers (e.g., HandleConnections, HandleMessages)
├── go.mod            # Go module file
└── go.sum            # Go dependency file
```

### Endpoints
/ws: The WebSocket connection endpoint for handling real-time chat messages.

## Setting Up the React Frontend (chatroom)
The React frontend serves as the user interface for the chat room.

### Steps to Run the Frontend
1. **In a new terminal, navigate to the chatroom/ directory**:
```bash
cd chatroom/
```
2. **Install the necessary dependencies**:
```bash
npm install
```
3. **Launch the development server**:
```bash
npm start
```
The frontend will be available at http://localhost:3000.

## Frontend File Structure
```bash
chatroom/
├── public/
│   └── index.html    # Main HTML file for the React app
├── src/
│   ├── components/   # Contains React components (ChatRoom, etc.)
│   ├── App.tsx       # Main app component
│   ├── index.tsx     # Entry point for the React app
│   └── styles.css    # Custom styles for the chat room
├── package.json      # NPM package file
└── tsconfig.json     # TypeScript configuration file
```

## Key Features
- Real-time messaging using WebSockets.
- Emoji support using the emoji-mart library.
- Responsive chatroom layout.

## Running Both Frontend and Backend

1. **Start the Go server: Open a terminal and navigate to the backend folder**:
```bash
cd real-time-chat/
go run main.go
```

2. **Start the React frontend: In a separate terminal, navigate to the frontend folder**:
```bash
cd chatroom/
npm start
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
