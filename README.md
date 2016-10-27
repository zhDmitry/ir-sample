# [Starter Pack](https://starter-pack.603.nu)

[Bitbucket Pipelines status](https://bitbucket.org/jch254/starter-pack/addon/pipelines/home)

## Overview

Starter Pack combines React, Redux and Redux-saga with Auth0's Lock as a starting point for modern
web apps with solid authentication. Why reinvent the wheel? The app utilises Rebass and Reflexbox to
keep things looking decent. I built this as a way to quickly prototype new ideas.

The app contains a 'locked down' Books page which requires a user to log in/sign up before content
will be visible. The data is read from a local JSON file as this is a only demonstration/starting
point. In the real world data would be fetched from external APIs (see externalApiService.js).
Protected routes in the external APIs should check validity of the JWT token and return unauthorised
if invalid. The app should then prompt the user to log in again. This is the perfect companion for
AWS Lambda/API Gateway-driven Node.js microservices. Separate those concerns!

![Main](https://img.jch254.com/Main.png)

![Modal](https://img.jch254.com/Login.png)

![Recommended](https://img.jch254.com/Books.png)

## Tools Used

* [React](https://github.com/facebook/react)
* [Redux](https://github.com/reactjs/redux) (ft. various middleware)
* [Redux Saga](https://github.com/yelouafi/redux-saga)
* [Auth0 Lock](https://github.com/auth0/lock)
* [React Router](https://github.com/reactjs/react-router)
* [Rebass](https://github.com/jxnblk/rebass)
* [Reflexbox](https://github.com/jxnblk/reflexbox)
* [Webpack](https://github.com/webpack/webpack)
* [Node.js](https://github.com/nodejs/node)

**SPOTIFY_CLIENT_ID, SPOTIFY_SCOPES and SPOTIFY_CALLBACK_URI environment variable must be set before `yarn run` commands below.**

E.g. `SPOTIFY_CLIENT_ID=YOUR_CLIENT_ID SPOTIFY_SCOPES="user-top-read playlist-modify-private" SPOTIFY_CALLBACK_URI="http://localhost:3001/spotifylogincallback" yarn run dev`

## Running locally

1. Sign up and create a new [Auth0 app](https://auth0.com)
1. Add http://localhost:3001 as an Allowed Origin (CORS) for your newly created app (don't forget to press save)
1. Run the following commands in the app's root directory then open http://localhost:3001

```
yarn install
yarn run dev
```

## Building the production version
1. Run the following commands in the app's root directory then check the /dist folder

```
npm install
npm run build
```

## Deployment/Infrastructure

Refer to the [/infrastructure](../master/infrastructure) directory.
