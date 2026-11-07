# Chats Web

React client for a real-time, one-to-one chat app. It pairs with [chats-backend](https://github.com/anishumar/chats-backend), a Node.js, Express, and MongoDB API.

## Features

- Registration, login, and profile management with Firebase Authentication
- Protected routes, with auth state shared through React Context
- Live messaging and online status over Socket.IO
- User search and chat rooms
- Emoji picker and a light/dark theme toggle

## Tech stack

React, React Router, Tailwind CSS, Headless UI, Axios, Socket.IO Client, Firebase

## Project structure

```
src/
  components/
    accounts/   Register, Login, Profile, Logout
    chat/       ChatRoom, ChatForm, Message, AllUsers, SearchUsers
    layouts/    ChatLayout, Header, ThemeToggler, ErrorMessage
  contexts/     AuthContext
  services/     ChatService (REST and socket calls)
  utils/        WithPrivateRoute, GenerateAvatar
```

## Running locally

Start [chats-backend](https://github.com/anishumar/chats-backend) first, then:

```bash
cp .env.example .env     # add your Firebase web app config
npm install
npm start
```

The app runs at http://localhost:3000. The backend address is set in `src/services/ChatService.js`.
