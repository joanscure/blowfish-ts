# ES6 Blowfish

[Blowfish](<https://en.wikipedia.org/wiki/Blowfish_(cipher)>) encryption library for browsers and Node.js from Dojo Toolkit 1.8.1 

Improved code first version using pure typescript

## Usage

All input data should be a `String`.
Strings support all unicode including emoji ✨.

### Example

```js
import Blowfish, { MODE, TYPE } from 'blowfish';

// third parameter is optional
const encrypted = Blowfish.encrypt("Secret Text", "SECRET",{cipherMode: MODE.ECB, outputType: TYPE.BASE64});

// third parameter is optional
const decrypted = Blowfish.decrypt(encrypted, "SECRET", {cipherMode: MODE.ECB, outputType: TYPE.BASE64}) as string)

console.log(encrypted);
console.log(decrypted);
```

### Block cipher mode of operation

https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation

```js
MODE.ECB; // (default) Electronic Codebook
MODE.CBC; // Cipher Block Chaining
MODE.PCBC; // Propagating Cipher Block Chaining
MODE.CFB; // Cipher Feedback
MODE.OFB; // Output Feedback
MODE.CTR; // Counter
```

### Return type

Which type of data should return method `decode`:

```js
TYPE.BASE64; // (default) Base64 String;
TYPE.HEX; // HexaDecimal String;
TYPE.STRING; // Uint8Array String;
TYPE.RAW; // Uint8Array
```
