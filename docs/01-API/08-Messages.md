# Messages

---

:::warning
You must provide **Authorization: "Bearer "TOKEN"** in **Headers** for each request
:::

---

> ## Send a new message

Using `POST` at `/api/v1/messages/sendMessage`

```javascript
{
"chatId": "<ID>"
"textContent": "hello"
}
```

You can also send files, **but it must be in a form-data**, for example:

| Key           | Value          |
| ------------- | -------------- |
| "chatId"      | "`<ID>`"       |
| "textContent" | "hello"        |
| files         | **FILES LIST** |

You can also edit the `MAX_NUM_OF_FILES_ON_UPLOAD` limits in [config.env](/docs/API/Config)

---

> ## Get messages

Using `Get` at `/api/v1/messages/?chatId=<ID>`

You can add params like `/api/v1/chats/?page=1&limit=5`
You can also edit the `GET_REQUEST_LIMIT` limits in [config.env](/docs/API/Config)

---

> ## Get one message

Using `Get` at `/api/v1/messages/<MSG_ID>/?chatId=<CHAT_ID>`

---

> ## Watch messages live

Use `"subToMessages"` connection and `"messageUpdate"` event name in [Sockets](/docs/API/Sockets)

---

_Last updated on November 16, 2024 by Aymen_
