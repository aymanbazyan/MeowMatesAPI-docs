# Authentication

> ## Sign up using `POST` at /api/v1/auth/signup

```js
// body
{
  "displayName": "مارك الزكارنة",
  "email": "ILoveHatim@gmail.com",
  "password": "pass1234", // New password
  "passwordConfirm": "pass1234"
}
```

> ## Login using `POST` at /api/v1/auth/login

```js
// body
{
  "email": "ILoveHatim@gmail.com",
  "password": "pass1234", // Current password
}
```

:::tip Note
Both these Requests returns a token, save it for later.
:::

> ## Forgot password `POST` at /api/v1/auth/forgotPassword

```js
// body
{
  "email": "ILoveHatim@gmail.com",
}
```

this should send you a reset token

> ## Reset password `PATCH` at /api/v1/auth/resetPassword/;token

```js
// body
{
    "password": "HarderPassword123123!@#$", // New password
    "passwordConfirm": "HarderPassword123123!@#$"
}
```

> ## Change my password `PATCH` at /api/v1/auth/updateMyPassword

```js
// body
{
    "passwordCurrent": "HarderPassword123123!@#$", // Old password
    "password": "pass1234", // New password
    "passwordConfirm": "pass1234" // New password
}

// headers
{
  Authorization: "Bearer <TOKEN>"
}
```

> ## Delete account `DELETE` at /api/v1/auth/deleteMyAccount

```js
// headers
{
  Authorization: "Bearer <TOKEN>";
}
```

_Last updated on August 9, 2024 by Aymen cholobob_