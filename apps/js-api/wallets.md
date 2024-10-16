---
title: Dag4.js Wallets
sidebar_label: Interacting with Wallets
slug: /dag4-wallets
hide_table_of_contents: false
---

## Interacting with Wallets
A wallet consists of a private key, a public key, and an address. You can create a new private key like this. 
```js
const pk = dag4.keyStore.generatePrivateKey();
```

### Login with a PK
Before accessing methods on dag4.account specific to a wallet, you'll need to log in with a private key or seed phrase.
```js
dag4.account.loginPrivateKey(pk);
```

### Login with a seed phrase
If you already have a pneumonic phrase generated by a web wallet or somewhere else you can log in with that as well.
```js
dag4.account.loginSeedPhrase('disco foxtrot calm appleseed trinity organ putter waldorf ordinary shatter green portion');
```

### Check DAG address
```js
const address = dag4.account.address;
```

### Get wallet public key
```js
dag4.account.publicKey;
```