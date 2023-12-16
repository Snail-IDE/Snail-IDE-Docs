---
title: Arguments and their Types
---

:::note
Anything that only works unsandboxed will be noted, but regardless, we will assume you are creating an unsandboxed extension during this tutorial.
:::

So far we have created a regular command block, reporter block, and a boolean block.  
But none of these blocks actually allow us to put other blocks inside, or even really do anything useful.

Why don't we take a look at **handling block arguments**?

## How do we add an input to a block?
First we need to start by adding an `arguments` object to a block.  
Let's use our console logging block for this.

