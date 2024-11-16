# Chats

---

:::warning
You must provide **Authorization: "Bearer "TOKEN"** in **Headers** for each request
:::

---

> ## Create a new chat

Using `POST` at `/api/v1/chats/createChat`

```javascript
{
"userId": "<ID>"
}
```

---

> ## Get chats

Using `Get` at `/api/v1/chats/`

You can add params like `/api/v1/chats/?page=1&limit=5`
You can also edit the `GET_REQUEST_LIMIT` limits in [config.env](/docs/API/Config)

---

> ## Get one chat

Using `Get` at `/api/v1/chats/<ID>`

---

_Last updated on November 16, 2024 by Aymen_
