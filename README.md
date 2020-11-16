# Confusables

Deno compatible version ported from https://github.com/gc/confusables

This library allows you to easily remove confusables from a string, into normal english characters.

Try it out: https://confusables.netlify.com/

## Usage

### Removing confusables

```ts
import remove from 'confusables';

remove('Ἢἕļľᦞ ш٥ṟｌᑰ! Hello World!'); // => Hello World! Hello World!
remove('Iлｔèｒｎåｔïｏｎɑｌíƶａｔïǫԉ'); // => Internationalization
```

### Injecting random confusables

```ts
import { obfuscate } from 'confusables';

obfuscate('Hello World!'); // => Ḣé𝑙ŀ𝟶 Ꮤᴑ𝖗łᏧ
obfuscate('Internationalization'); // => ᶦṅᵗᧉ𝘳𝓃ȧťί𝙾ቢค𝞲ἱƶ𝜶ナἰøŉ
```

### List of supported confusable characters

```ts
import { characters } from 'confusables';

console.log(characters);
```

## What are confusables?

> Confusable characters are those that may be confused with others (in some common UI fonts), such as the Latin letter "o" and the Greek letter omicron "ο". Fonts make a difference: for example, the Hebrew character "ס" looks confusingly similar to "o" in some fonts (such as Arial Hebrew), but not in others.

> [Source](https://unicode.org/cldr/utility/confusables.jsp)
