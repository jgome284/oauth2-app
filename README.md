# OAuth2 on GitHub

## About

This project provides a basic web app to authenticate users via an OAuth2 strategy on GitHub.

## Prerequisites

### Container Engine

The easiest way to get started is by leveraging the dev container in this repo. You will need a Container Engine like Docker installed and running. For Docker, the easiest way to start the container engine is via Docker Desktop.

### Visual Studio Code

The dev container provided is set up for use on Visual Studio Code. Have it installed along with the [remote development pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) to enable the IDE's DevContainers functionality.

## Getting started

Open VS Code in a directory of your choice. With the terminal, clone this repository via `git clone https://github.com/jgome284/oauth2-app`.

Make sure you have your container engine running. Open your local copy of the project on VS Code and start the development container by running Dev Containers: Rebuild and Reopen In Container in the command palette. It can be accessed with the keyboard shortcut `ctrl + shift + P` on your keyboard.

When the Dev Container launches, install project dependencies via npm by executing the following command.

> npm install

If successful, a node_modules folder should appear in your directory. 

You will also need to register the app on GitHub for OAuth2 Authentication. To do so, reference [the following instructions](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app). Name the app whatever you want. Fill out the Homepage URL and Authorization Callback URL with the following: 

- **Homepage URL:** http://localhost:3000
- **Authorization Callback URL:** http://localhost:3000/auth/github/callback

With the app registered, you will receive a Client ID. Generate a Client Secret and make sure you copy it to your clipboard. Add both the Client ID and Client Secret variables to a .env file at the root of your directory as follows.

```.env
GITHUB_CLIENT_ID=<YOUR CLIENT ID>
GITHUB_CLIENT_SECRET=<YOUR CLIENT SECRET>
```

To start the webapp run the following command.

> npm start

Then, lanch the webapp on localhost:3000 and test the GitHub OAuth 2 authentication strategy! ... Yay! (ﾉ◕ヮ◕)ﾉ*:･ﾟ🎊!
