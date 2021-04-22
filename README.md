# GPT-2/3 Tokenizer

GPT-2/3 byte pair encoder/decoder/tokenizer based on [@latitudegames/GPT-3-Encoder](https://github.com/latitudegames/GPT-3-Encoder) that works in the browser and Deno.

See also: [JS byte pair encoder for OpenAI's CLIP model](https://github.com/josephrocca/clip-bpe-js).

```js
import {encode, decode} from "https://deno.land/x/gpt_2_3_tokenizer@v0.0.1/mod.js";
let text = "hello world";
console.log(encode(text)); // [18798, 995]
console.log(decode(encode(text))); // "hello world"
```

# License

The [original code is MIT Licensed](https://github.com/latitudegames/GPT-3-Encoder/blob/master/LICENSE) and so are any changes made by this repo.
