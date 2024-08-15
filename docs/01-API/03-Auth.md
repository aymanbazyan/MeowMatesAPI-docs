# Authentication

---

> ## Sign up

using `POST` at /api/v1/auth/signup

```js
// body
{
  "displayName": "Aymen",
  "email": "example@gmail.com",
  "password": "pass1234", // New password
  "passwordConfirm": "pass1234"
}
// This account is not valid yet
```

after that, we must validate the account using a captcha `POST` request at /api/v1/auth/sendCaptchaCode

> ## Send captcha

```js
// body
{
    "email": "example@gmail.com",
}

```

this will send a code to the given email, to confirm it, we send another requests to the same URL but this time we must provide the **code** property:

```js
// body
{
    "email": "example@gmail.com",
    "code": 1234
}

```

> ## Login

using `POST` at /api/v1/auth/login

```js
// body
{
  "email": "example@gmail.com",
  "password": "pass1234", // Current password
  "remember": true, // Return an expire date with the cookie
}
```

> ## Forgot password

using `POST` at /api/v1/auth/forgotPassword

```js
// body
{
  "email": "example@gmail.com",
}
```

:::tip Note
These 3 requests returns a token, save it for other uses.
:::

using `PATCH` at /api/v1/auth/resetPassword/;token

```js
// body
{
    "password": "HarderPassword123123!@#$", // New password
    "passwordConfirm": "HarderPassword123123!@#$"
}
```

> ## Change password

using `PATCH` at /api/v1/auth/updateMyPassword

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

> ## Update info

using `PATCH` at /api/v1/auth/changeAccountData

```js
// body
{
    "displayName": "My new name",
    "bio":"hello there"
}

// headers
{
  Authorization: "Bearer <TOKEN>";
}
```

> ## Delete account

using `DELETE` at /api/v1/auth/deleteMyAccount

```js
// headers
{
  Authorization: "Bearer <TOKEN>";
}
```

_Last updated on August 15, 2024 by Aymen_
