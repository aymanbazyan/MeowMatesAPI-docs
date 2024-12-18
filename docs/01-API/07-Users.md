# Users

---

:::warning
You must provide **Authorization: "Bearer "TOKEN"** in **Headers** for each request
:::

---

> ## Get my profile

Using `GET` at `/api/v1/users/me`

---

> ## Get 1 user by ID

Using `GET` at `/api/v1/users/:id`

```javascript
<URL>/api/v1/users/<123456789>
```

---

> ## Search for users by name

Using `POST` at `/api/v1/users/search`

```javascript
// body
{
    "name": "firstname", // put a part of a name
    "page": 2, // default: 1
    "pageSize": 5 // default: 10
}

```

Also you can edit `MAX_SEARCH_TYPOS` in [config.env](/docs/API/Config)

_Last updated on October 23, 2024 by Aymen_
