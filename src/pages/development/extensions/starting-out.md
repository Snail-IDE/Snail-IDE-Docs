---
title: First steps
---

Anything that only works unsandboxed will be noted, but regardless, we will assume you are creating an unsandboxed extension during this tutorial.

## Let's start simple
Let's create the first beginnings of our extension.
Create a new JavaScript file (file extension is `.js`) and place a function that runs on start.

We'll want this function to take an input, a `Scratch` global object that is given to extensions.
This object gives us some tools we'll need for creating blocks.

The cleanest way to do this is like this:

```js
(function(Scratch) {
  'use strict';
  
})(Scratch);
```

We are using a function with `'use strict'` here to prevent any variables we create to enter the global scope.
This will prevent any *weirdness* once other extensions try to create variables or things with the same name.

Next let's create a class for our extension. This will be where most of the code for our extension will be.

This can be done as follows:

```js
(function(Scratch) {
  'use strict';
  class Extension {
  
  }
})(Scratch);
```

We still have 2 more things to add on before we can load this into PenguinMod.
Let's add the code to register this into PenguinMod, so we don't forget later.

```js
(function(Scratch) {
  'use strict';
  class Extension {
  
  }
  Scratch.extensions.register(new Extension());
})(Scratch);
```

This is our first use of the `Scratch` object.
The `extensions` property of the `Scratch` object gives us some small information, and the ability to register our extension.

There are a few more things that the `Scratch.extensions` object has:
```json
{
    "unsandboxed": (boolean),
    "isPenguinMod": (boolean)
}
```

- `unsandboxed` will be true if the extension is run unsandboxed.
- `isPenguinMod` will be true if loaded into the PenguinMod editor, or if it's in a packaged project.