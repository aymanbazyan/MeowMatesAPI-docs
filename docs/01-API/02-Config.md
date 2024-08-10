# Configure Enviormnet

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
NODE_ENV = development
PORT = 3000

DATABASE = mongodb+srv://<YOUR NAME>:<PASSWORD>@<CLUSTER NAME>.<ID>.mongodb.net/<COLLECTION NAME>
DATABASE_LOCAL = mongodb://localhost:27017/<COLLECTION NAME>
DATABASE_USERNAME = <DATABASE USERNAME>
DATABASE_PASSWORD = <YOUR PASSWORD>

JWT_SECRET = <LONG PASSWORD>
JWT_EXPIRES_IN = 30d
JWT_COOKIE_EXPIRES_IN = 30

EMAIL_MAIL = <YOUR MAIL>
EMAIL_PASSWORD = <YOUR EMAIL PASSWORD>
```

:::danger
Nobody should see this file.
:::

_Last updated on August 8, 2024 by Aymen_
