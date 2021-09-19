# How to get our app running?

## Client only
you can run the app in a client only mode.
The client sends requests to a "fake server" that returns random data.

```
cd sofi-client
npm start
```
in separate tab
```
npm run start:fakeserver
```
## Running against local server
you need to run the server locally. By default server uses sqlite as db. look at `env.ts` on how to persist data, or connect with mysql.

env var can be placed in `.env`.


```
cd sofi-client
npm run start:realauth
```
in separate tab
```
cd sofi-server
npm start
```
## Running local client but using server from staging
- if you are trying to fix a bug, this might be useful, but it's not a replacement for tests. you still need to write tests.


(needs more testing to make sure it works)
change `proxy` in package.json to point to staging url .

```
cd sofi-client
npm run start:realauth
```


