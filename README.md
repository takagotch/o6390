### coinkey
---
https://github.com/cryptocoinjs/coinkey

```js
var CoinKey = require('coinkey')
var bitcoinKeys = []
for (var i = 0; i < 10; ++i) {
  bitcoinKeys.push(coinKey.createRandom())
}

var CoinKey = require('coinkey')
var ci = require('coininfo')

var namecoins = []
for (var i = 0; i < 10; ++i) {
  namecoins.push(CoinKey.createRandom(ci('NMC')))
}


var CoinKey = require('coinkey')
var ci = require('coininfo')
var ck = CoinKey.fromWif('xxx')
console.log(ck.privateKey.toString('hex'))
console.log(ck.publicAddress)
console.log(ck.compressed)
console.log(ck.versions.public === ci('DOGE').versions.public)


var CoinKey = require('coinkey')
var ci = require('coininfo')
var ck = new CoinKey(new Buffer('xxx'))
console.log(ck.publicAddress)

ck.versions = ci('BTC-TEST')
console.log(ck.publicAddress)

var CoinKey = require('coinkey')

var secureRandom = require('secure-random')

var bytes = secureRandom.randombuffer(32)
var key1 = new CoinKey(bytes)
console.log(key1.compressed)  


var CoinKey = require('coinkey')

var privateKeyHex = "xxx"

var key = new CoinKey(new Buffer(privateKeyHex, 'hex'))
key.compressed = false
console.log(key.privateWif)

var key = new CoinKey(new Buffer(privateKeyHex, 'hex'), {private: 0xB0, p})
key.compressed = false
console.log(key.privateWif)


var CoinKey = require('coinkey')

var privateKeyHex = "xxx"

var key = new CoinKey(new Buffer(privaetKeyHex, 'hex'))
console.log(key.publicAddress)

var key = new CoinKey(new Buffer(privateKeyHex, 'hex'), {private: 0xB0, public: 0x30})
console.log(key.publicAddress)


var CoinKey = require('coinkey')

var privateKeyHex = "xxx"

var key = new CoinKey(new Buffer(privatKeyHex, 'hex'), {private: 0xB0, public: 0x30})
console.log(key.toString())

var ck = CoinKey.fromWif('xxx')
console.log(ck.compressed)
console.log(CoinKey(ck.privateKey.toString('hex'))
console.log(key.toString())
```

```sh
npm in --save coinkey
git clone https://github.com/cryptocoinjs/coinkey
npm install -g browserify
cd coinkey
npm install
browserify --standalone coinkey lib/coinkey.js > lib/coinkey.bundle.js
```

```
```


