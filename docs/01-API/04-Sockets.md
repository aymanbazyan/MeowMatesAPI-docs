# Sockets

---

> ## Purpose

Sockets are used for **live connections with the API**; you can observe changes happening to messages and chats live for example!

---

> ## Javascript

run `npm i socket.io-client` and type:

```javascript
import { io } from "socket.io-client";

function subToSocket(subToName, nameOnUpdate, obj, callbackOnUpdate) {
  const socket = io(API_URL, {
    transports: ["websocket"], // Use WebSocket transport
    withCredentials: true, // Include credentials if needed
  });

  // Emit "subToMessages" with token
  socket.emit(subToName, obj);

  // Listen for incoming changes
  socket.on(nameOnUpdate, (change) => {
    callbackOnUpdate(change);
  });

  return () => {
    socket.off(subToName);
    socket.disconnect();
  };
}
```

Calling the function:

```javascript
const unsub = await subToSocket(
  <CONNECTION>,
  <EVENT_NAME>,
  { token: <TOKEN>, user2Id: <CHAT_ID> },
  (change) => {
    console.log(change)
  }
);
```

---

> ## Possible events and connections

| Connection      | Events for connection |
| --------------- | --------------------- |
| "subToMessages" | "messageUpdate"       |
| "subToChats"    | "chatUpdate"          |

---

_Last updated on November 16, 2024 by Aymen_
