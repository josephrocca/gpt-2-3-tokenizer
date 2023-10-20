**Note**: This repo is for GPT-3 only. Here's some code that should work for gpt-3.5-turbo and gpt-4:
```js
import { AutoTokenizer } from 'https://cdn.jsdelivr.net/npm/@xenova/transformers@2.6.2'
let tokenizer = await AutoTokenizer.from_pretrained("Xenova/gpt-4"); // gpt-3.5-turbo uses same tokenizer as gpt-4 IIUC
let tokens = tokenizer.encode("hello world");
```

---

# GPT-2/3 Tokenizer

GPT-2/3 byte pair encoder/decoder/tokenizer based on [@latitudegames/GPT-3-Encoder](https://github.com/latitudegames/GPT-3-Encoder) that works in the browser and Deno.

See also: [JS byte pair encoder for OpenAI's CLIP model](https://github.com/josephrocca/clip-bpe-js).

```js
import {encode, decode} from "https://deno.land/x/gpt_2_3_tokenizer@v0.0.2/mod.js";
let text = "hello world";
console.log(encode(text)); // [258, 18798, 995]
console.log(decode(encode(text))); // "hello world"
```
or:
```js
let mod = await import("https://deno.land/x/gpt_2_3_tokenizer@v0.0.2/mod.js");
mod.encode("hello world"); // [258, 18798, 995]
```
or to include it as a global variable (as if you were importing it with the old script tag style):
```html
<script type=module>
  import tokenizer from "https://deno.land/x/gpt_2_3_tokenizer@v0.0.2/mod.js";
  window.tokenizer = tokenizer;
</script>
```

# License

The [original code is MIT Licensed](https://github.com/latitudegames/GPT-3-Encoder/blob/master/LICENSE) and so are any changes made by this repo.
