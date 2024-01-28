---
title: ChatGPT
---

| :zap:        This is a modified version of the WorkingTurboGPT Docs   |
|-----------------------------------------|

## Harness the power of ChatGPT-3.5 in your projects! 
*Extension originally made by LOLEMO then forked by Anonymous_cat1.*

## API Note
APIs go up and down every once in a while, so if you get error responses, you should be able to find more reverse proxies here on the internet.
The API used in LOLEMO's version is dead, so I've updated it to use https://reverse.mubi.tech/v1/chat/completions by default, although you can update it using the "Set Reverse Proxy API URL" block.

Ratelimits are inevitable however, you can get around them with a VPN/Proxy or just waiting a few hours.

## Installation
To use this extension in Snail IDE go to the extension menu and add the PenguinGPT extension.
    
## How to use
If you find that using the extension only reports errors, use this block to update the API URL. (You can find ChatGPT reverse proxies by looking them up)

![Set Reverse Proxy API URL](https://snail-ide.js.org/SnailGPT/img/block_10_2_2023-4_59_51 PM.svg)

Additionally, You can use this reporter to check if the API you are using is alive. 

![Check API](https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_28_51 PM.svg)

To simply send a prompt to ChatGPT without any context (chat history), use this reporter:

![Send Prompt](https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_28_56 PM.svg)

If you want to use prompts with history (GPT remembers previous messages) you will have to create a chatbot! you can use these blocks to manage (create, delete, and reset) chatbots.

![Manage Chatbots](https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_19 PM.svg)

Also, you can use this block to change the behavior of the chatbot:

![Change Chatbot Behavior](https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_02 PM.svg)

Then, use this reporter to interact with the one you have created:

![Interact with Chatbot](https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_39_30 PM.svg)

If you want to get a predefined jailbreak or prompt, you can use this block:

![Get Predefined Prompt](https://snail-ide.js.org/SnailGPT/img/block_11_19_2023-3_14_26 PM.svg)

Now, if you want to export chats, use these blocks:

![Export Chats](https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_37 PM.svg)

![Export Chats 2](https://snail-ide.js.org/SnailGPT/img/block_11_19_2023-3_17_42 PM.svg)

If you want to import chats, use these blocks:

![Import Chats](https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_40 PM.svg)

If you want to get all active chats as an array, use this block:

![Get Active Chats](https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_43 PM.svg)

You can even generate images with PenguinGPT!

![Generate Images](/img/docimages/block_1_27_2024-10_42_18 PM.svg)
