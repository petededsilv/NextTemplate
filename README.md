﻿# NextTemplate

# NextTemplate

This project was begun by the Inspire Team in April 2023.

## What Is It?

The Template NEXT.js to be used with Vercel to connect to WordPress.


## Docs

- [GIT Guidelines](/docs/GIT_GUIDELINES.md)

## Installation

### Prerequisites

- Install Homebrew
- Install Git
- Install Node v16 (recommended using nvm)
- Clone the repo locally
- Ensure you've the latest of the environment variables saved in `.env` file
  - See `.env.example` for a sample env variables

Once you've met all above prerequisites, install the app with the command below

```
npm install
```

npm install next react react-dom

## Running the app

```
npm run start
```

## Organization

Currently, this codebase is broken down into four sections, **components**, **config**, **pages**, and **sass**.

### Components

Each UI component currently lives in its own folder, and is named _Component.tsx_. An exception is made for tightly coupled components, such as text inputs, text-area inputs, & dropdown inputs, and for pages which all belong to the same form.

Generally, the component's business logic is kept in a separate file, currently called useHooks.ts, whereas the component itself handles its presentation only.

A component's CSS files are also kept here, as are index.ts files which are used for easy exporting(not currently implemented across the board.)

### Config

Currently, we have our Firebase authentication credentials here, and will keep other configuration files here in the future as well.

### Pages

This is empty at the moment, but now that the design of the project has stabilized, we will migrate components that render screens(such as a login page, landing page, merchandise creation form) to this folder, to provide a separation between small UI components and large templates and pages.

### SASS

This is where our compiled CSS lives.

## Tests

### Unit tests

npm run dev
npm run test

### e2e tests

#### cli

npm run test:e2e:run

#### UI

npm run test:e2e

## Customize Reset Password Template on Firebase

Log onto the Console
Follow these steps:
https://firebase.google.com/docs/auth/custom-email-handler#link_to_your_custom_handler_in_your_email_templates

Use the Env full URL to /passwordreset as Action URL
