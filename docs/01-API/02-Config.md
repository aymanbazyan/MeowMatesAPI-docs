# Configure Enviormnet

---

> ## Enviorment

First you must get the required strings from:-

1. MongoDB.
2. Gmail apps.

You can create the **config.env** here:

- MeowMatesAPI folder
  - config.env

<!-- | Header 1 | Header 2 |
| -------- | -------- |
| Row 1    | Data     | -->

```javascript
NODE_ENV=development // or production
PORT=3000

// Your app's localhost and prod link
ALLOWED_URLS=["http://localhost:5173", "https://meow-mates.vercel.app"]

// From MongoDB
DATABASE=mongodb+srv://<YOUR NAME>:<PASSWORD>@<CLUSTER NAME>.<ID>.mongodb.net/<PROJECT NAME>
DATABASE_LOCAL=mongodb://localhost:27017/<PROJECT NAME>

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

// From email app settings
EMAIL_MAIL=<YOUR MAIL>
EMAIL_PASS=<YOUR EMAIL PASSWORD>

// searching for users by name
DEFAULT_PAGE=1
DEFAULT_PAGE_SIZE=10
MAX_SEARCH_TYPOS=1

// Other than password
ALLOW_USER_TO_EDIT=["displayName", "email", "photoURL", "bio"]

GET_REQUEST_LIMIT=30

MAX_NUM_OF_FILES_ON_UPLOAD=5
```

:::danger
Nobody should see this file.
:::

---

> ## Search index

And also you must add these options for displayName in [Search Index](https://www.mongodb.com/docs/atlas/atlas-search/tutorial/create-index/) of the users collection:

```javascript
{
  "mappings": {
    "dynamic": false,
    "fields": {
      "displayName": {
        "type": "autocomplete"
      }
    }
  }
}
```

_Last updated on October 23, 2024 by Aymen_
