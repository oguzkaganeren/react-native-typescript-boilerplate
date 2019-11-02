# React native typescript boilerplate

## Folder Structure

`src/app/assets`: This directory contains all the assets files (i.e. images, audio files or videos...) used by the application.

`src/app/boot`: This directory contains all the setup files (i.e. expo font, ...) used by the application.

`src/app/components`: This directory contains presentational components, i.e. React components responsible for the UI of the application.

`src/app/config`: This directory contains configuration variables in 3 files:

-`index.dev.tsx` : contains development variables -`index.production.tsx` : contains production variables -`index.staging.tsx` : contains beta tests variables

You need to create `index.tsx` by copying the right file.

### Warning

Each time you need to build, you need to verify if your `index.tsx` is the right one.
For example, during development, before building your app do:

cp App\Config\index.dev.tsx App\Config\index.tsx

In other environment, you must pay attention to change your `index.tsx` with the good one.
Also, make sure you add each configuration variable in each configuration file.

### Usage

import Config from 'App/Config'

let uri = Config.API_URL

`src/app/containers`: This directory contains container components, i.e. React components responsible for the logic of the application.

`src/app/navigators`: This directory contains your main Navigator (AppNavigator.tsx) You can add nested navigators on this folder if you need it.

`src/app/sagas`: Redux Saga is a library that makes application side effects (i.e. asynchronous things like data fetching and impure things like accessing the browser cache) easier to manage.

This directory contains the sagas of the application. Sagas will for example connect to an API to fetch data, perform actions, etc.

`src/app/services`: This directory contains application services, for example services to connect the application to APIs.

`src/app/pages`: This directory contains presentational screen.

`src/app/theme`: This directory contains the base for the application styles.

## Inspired by

[react-native-boilerplate](https://github.com/thecodingmachine/react-native-boilerplate)
