# TypeScript React MD Parser

Parses markdown text into HTML text.

This is directly taken from [snarkdown](https://github.com/developit/snarkdown) - I just converted the code from JS to TS.

## How to use
1. Paste the contents from `MDParser.ts` or download the file and add it into your project.
2. Import the MD parser function into your project.
```TS
import { MDParser } from "./mdparser";
```

3. That's it! You simply need to apply it as an attribute to your component, this needs to be set as a **dangerously InnerHTML**.

```TS
import { MDParser } from "./mdparser";

const md = "**this is** amazing!"

export default function Page() {
    return (
        <h1 dangerouslySetInnerHTML={{__html: MDParser(md)}}/>
    )
}

// RESULT: <strong>this is</strong> amazing!
```
