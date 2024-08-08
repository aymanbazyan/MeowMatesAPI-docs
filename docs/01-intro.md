---
sidebar_position: 1
slug: /
---

# Tutorial Intro

Let's discover **MeowMates in less than 5 minutes**.

## Getting Started

Get started by **opening any code editor**.

Or **download postman** from **[here](https://www.postman.com/)**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 18.0 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Get the API project

Download a new folder project using **git**.

The package will automatically be added to your project after you run the command:

```bash
git clone https://github.com/aymanbazyan/MeowMatesAPI.git
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

This command also installs all necessary dependencies you need to run MeowMatesAPI.

```bash
npm i
```

## Start the API

Run the development server:

```bash
cd my-folder
npm run start
```

The `cd` command changes the directory you're working with. In order to work with your newly created API folder, you'll need to navigate the terminal there.

The `nodemon server.js` command builds your API locally and serves it through a development server, ready for you to view at http://127.0.0.1:3000/

Open `/api/v1/users` (GET request), to test it out, and edit some lines: the site **reloads automatically** and displays your changes.

_Last updated on August 8, 2024 by Aymen cholobob_
