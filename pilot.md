## Intro

- [Gabriel Cardona](https://twitter.com/cgcardona)
- [Bitcoin.com Developer Services](https://developer.bitcoin.com)

## Prerequisites

- Basic web development
- Comfortable at the command line
- Basic git workflow
- [Atom Text Editor](http://atom.io/)
- [iTerm3 Terminal](https://www.iterm2.com/version3.html)
- [NodeJS LTS](https://nodejs.org/en/)

## Setup

1.  Install Atom
2.  Install iTerm
3.  Install NodeJS
    - `node -v`
    - `npm -v`
4.  [https://www.npmjs.com/](https://www.npmjs.com/)

## Steps

Install BITBOX SDK

```
npm install bitbox-sdk --global
bitbox -v
```

Create new react scaffold

```
bitbox new myReactApp --scaffold react
cd myReactApp
npm install && npm start
```

Create new nodeJS scaffold

```
bitbox new myNodeApp --scaffold node
cd myNodeApp
npm install && npm start
```

Show `bitbox.js` and open console

```
bitbox console
bitbox console --environment production
```

Convert cash address to legacy address

```js
BITBOX.Address.toLegacyAddress(
  "bitcoincash:qzm47qz5ue99y9yl4aca7jnz7dwgdenl85jkfx3znl"
);
// 1HiaTupadqQN66Tvgt7QSE5Wg13BUy25eN
```

Get details about address

```js
(async () => {
  try {
    let details = await BITBOX.Address.details([
      "1BFHGm4HzqgXXyNX8n7DsQno5DAC4iLMRA"
    ]);
    console.log(details);
  } catch (error) {
    console.error(error);
  }
})();
```

### Resources

- [Semantic Versioning](https://semver.org/)
- [BITBOX SDK docs](https://developer.bitcoin.com/bitbox/)
- [BITBOX SDK source code](https://github.com/Bitcoin-com/bitbox-sdk)
