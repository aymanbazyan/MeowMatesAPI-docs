# Configure Enviormnet

---

> First you must get the required strings from:-

1. MongoDB.
1. Gmail apps.

You can create the **config.env** here:

- MeowMatesAPI folder
  - config.env

<!-- | Header 1 | Header 2 |
| -------- | -------- |
| Row 1    | Data     | -->

```javascript
NODE_ENV=development
PORT=3000

DATABASE=mongodb+srv://<YOUR NAME>:<PASSWORD>@<CLUSTER NAME>.<ID>.mongodb.net/<COLLECTION NAME>
DATABASE_LOCAL=mongodb://localhost:27017/<COLLECTION NAME>

USER_NAME_MAX_LENGTH=15
USER_NAME_MIN_LENGTH=3

USER_PASS_MIN_LENGTH=8
USER_PASS_MAX_LENGTH=60
USER_PASS_SALT=12
USER_RESET_PASS_EXPIRE=600000
USER_DEFAULT_PICTURE='https://i.imgur.com/iNzohYg_d.webp?maxwidth=760&fidelity=grand'

JWT_SECRET=<LONG PASSWORD>
JWT_EXPIRES_IN=30d
JWT_COOKIE_EXPIRES_IN=30

EMAIL_MAIL=<YOUR MAIL>
EMAIL_PASSWORD=<YOUR EMAIL PASSWORD>
```

:::danger
Nobody should see this file.
:::

_Last updated on August 8, 2024 by Aymen_
