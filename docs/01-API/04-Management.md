# Management capabilities

---

:::warning
You must provide **Authorization: "Bearer "TOKEN"** in **Headers** for each request, **AND YOU MUST BE AN ADMIN OR A MOD**
:::

---

> ## Get all users with filter

Using `GET` at `/api/v1/users`

```bash
<URL>/api/v1/users
```

You can also use these options in params:

- filter (key=value)
- sort
- limit
- limit and page

Examples:

```bash
// filter by role:
<URL>/api/v1/users?role=admin
```

```bash
// paginate:
<URL>/api/v1/users?page=1?limit=10
```

---

> ## Delete any user

Using `DELETE` at `/api/v1/users/:ID`

```bash
<URL>/api/v1/users/<ID>
```

---

> ## Edit any user

Using `PATCH` at `/api/v1/users/:ID`

```bash
<URL>/api/v1/users/<ID>
```

---

_Last updated on October 23, 2024 by Aymen_
