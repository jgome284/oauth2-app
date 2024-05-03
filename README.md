# OAuth2 with GitHub 🔓

## About

This project provides a basic web app that authenticates users via an OAuth2 strategy on GitHub.

## Prerequisites

### Container Engine

The easiest way to get started is by leveraging the dev container in this repo. You will need a Container Engine like Docker installed and running. For Docker, the easiest way to start the container engine is via Docker Desktop.

### Visual Studio Code

The dev container provided is set up for use on Visual Studio Code. Have it installed along with the [remote development pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) to enable the IDE's DevContainers functionality.

## Getting started

With the terminal, clone this repository via `git clone https://github.com/jgome284/oauth2-app` in a directory of your choice. 

Make sure you have your container engine running. Open your local copy of the project on VS Code and start the development container by running Dev Containers: Rebuild and Reopen In Container in the command palette. It can be accessed with the keyboard shortcut `ctrl + shift + P` on your keyboard.

When the Dev Container launches, install project dependencies via npm by executing the following command.

> npm install

If successful, a node_modules folder should appear in your directory. 

You will also need to register the app on GitHub for OAuth2 Authentication. To do so, reference [the following instructions](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app). Name the app whatever you want. Fill out the Homepage URL and Authorization Callback URL as follows: 

- **Homepage URL:** http://localhost:3000
- **Authorization Callback URL:** http://localhost:3000/auth/github/callback

With the app registered, you will receive a Client ID. Generate a Client Secret and make sure you copy it to your clipboard. Add the Client ID and Client Secret variables to a `.env` file at the root of your directory as follows.

```.env
GITHUB_CLIENT_ID=<YOUR CLIENT ID>
GITHUB_CLIENT_SECRET=<YOUR CLIENT SECRET>
```

To start the web app run the following command.

> npm start

Then, launch the web app on localhost:3000 and sign in through GitHub to test our OAuth 2 authentication strategy! ... Yay! (ﾉ◕ヮ◕)ﾉ*:･ﾟ🎊!
