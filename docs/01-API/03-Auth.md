# Authentication

---

> ## Sign up

Using `POST` at `/api/v1/auth/signup`

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

After that, we must validate the account using a captcha `POST` request at `/api/v1/auth/sendCaptchaCode`

---

> ## Send captcha

```js
// body
{
    "email": "example@gmail.com",
}
```

This will send a code to the given email, to confirm it, we send another requests to `The same URL` but this time we must provide the **code** property:

> ## Confirm Capatcha

```js
// body
{
    "email": "example@gmail.com",
    "code": abcdef
}
```

---

> ## Login

Using `POST` at `/api/v1/auth/login`

```js
// body
{
  "email": "example@gmail.com",
  "password": "pass1234", // Current password
  "remember": true, // Return an expire date with the cookie
}
```

---

> ## Forgot password

Using `POST` at `/api/v1/auth/forgotPassword`

```js
// body
{
  "email": "example@gmail.com",
}
```

:::tip Note
These 3 requests returns a token, save it for other uses.
:::

Using `PATCH` at `/api/v1/auth/resetPassword/<token>`

```js
// body
{
    "password": "HarderPassword123123!@#$", // New password
    "passwordConfirm": "HarderPassword123123!@#$"
}
```

---

> ## Change password

Using `PATCH` at `/api/v1/auth/updateMyPassword`

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

---

> ## Update info

Using `PATCH` at `/api/v1/auth/changeAccountData`

:::note
Adjust the `ALLOW_USER_TO_EDIT` array in [config.env](/docs/API/Config) **if you want**
:::

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

---

> ## Delete account

Using `DELETE` at `/api/v1/auth/deleteMyAccount`

```js
// headers
{
  Authorization: "Bearer <TOKEN>";
}
```

_Last updated on August 15, 2024 by Aymen_
