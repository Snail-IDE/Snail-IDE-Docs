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

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_2_2023-4_59_51 PM.svg" alt="Set Reverse Proxy API URL" />

Additionally, You can use this reporter to check if the API you are using is alive. 

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_28_51 PM.svg" alt="Check API" />

To simply send a prompt to ChatGPT without any context (chat history), use this reporter:

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_28_56 PM.svg" alt="Send Prompt" />

If you want to use prompts with history (GPT remembers previous messages) you will have to create a chatbot! you can use these blocks to manage (create, delete, and reset) chatbots.

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_19 PM.svg" alt="Manage Chatbots" />

Also, you can use this block to change the behavior of the chatbot:

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_02 PM.svg" alt="Change Chatbot Behavior" />

Then, use this reporter to interact with the one you have created:

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_39_30 PM.svg" alt="Interact with Chatbot" />

If you want to get a predefined jailbreak or prompt, you can use this block:

<img src="https://snail-ide.js.org/SnailGPT/img/block_11_19_2023-3_14_26 PM.svg" alt="Get Predefined Prompt" />

Now, if you want to export chats, use these blocks:

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_37 PM.svg" alt="Export Chats" />
<img src="https://snail-ide.js.org/SnailGPT/img/block_11_19_2023-3_17_42 PM.svg" alt="Export Chats 2" />

If you want to import chats, use these blocks:

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_40 PM.svg" alt="Import Chats" />

If you want to get all active chats as an array, use this block:

<img src="https://snail-ide.js.org/SnailGPT/img/block_10_14_2023-4_29_43 PM.svg" alt="Get Active Chats" />

You can even generate images with PenguinGPT!

<img src="/img/docimages/block_1_27_2024-10_42_18 PM.svg" alt="Generate Images" />