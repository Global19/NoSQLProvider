# NoSQLProvider [![Build Status](https://travis-ci.org/Microsoft/NoSQLProvider.svg?branch=master)](https://travis-ci.org/Microsoft/NoSQLProvider)
We developed NoSQLProvider after needing a simplified interface to NoSQL-style object storage/retrieval that worked not only across all browsers, but also for native app development (initially Cordova-based, later moving to React Native.)  Across the browsers, this required unifying WebSQL and IndexedDB, with the nuances of all the different IndexedDB issues (on IE, mostly, with not properly supporting compound keys and multi-entry indexes, and Safari having basically completely broken keyspace support.)  On native platforms and NodeJS, we fully wrap several different SQLite-based providers, depending on the platform.  We also have built a fully in-memory database provider that has no persistence but supports fully transactional semantics, for a fallback in situations where you don't want persistence (ephemeral logins, etc.)


At this point, known feature work is complete and we are mostly just fixing bugs on the platform moving forward.  If you have feature requests, feel free to file them, just make sure that you have behavior determined across all providers as part of your request, since all features need to be able to work across all the different providers.

# Examples
The only current full example is available as part of the ReactXP samples, the [TodoList](https://github.com/Microsoft/reactxp/tree/master/samples/TodoList) sample app.  If you pick up NoSQLProvider and use it in your open source application, please let us know so we can add more example links here!

# Providers/Platforms/Support

We will soon list all of the providers available out of the box here, and list what platforms they can be used on, with any nuances of that platform.

# Usage

Coming soon.

## Compiling
### Source
```bash
yarn install
yarn build
```
### Tests
```bash
yarn install
yarn webtest
```

## Testing
1. Compile tests
1. Open test.html in browser
1. You can add `?grep=foo` to the URL to run only tests containing 'foo' in the name
