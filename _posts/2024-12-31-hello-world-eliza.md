---
layout: post
title:  "Eliza: Hello World"
date:   2024-12-31 15:28:00 -0000
categories: ai agent framework
---

# Create your first Eliza Agent<br/>
> Assumption: you already have git, node, and pnpm installed<br/>
> For **git**: [Find instructions to install git](https://github.com/git-guides/install-git)<br/>
> For **node**: [Visit the Node.js website](https://nodejs.org) and download the appropriate installer for your operating system. Once downloaded, run the installer and follow the on-screen instructions. After a successful installation, you’ll have access to the node and npm command in your terminal or command prompt.
> For **pnpm**: In a terminal, run the command `npm install -g pnpm`

* Open a command line terminal and run the following commands

# Clone the Eliza Starter Repository
`git clone https://github.com/elizaOS/eliza-starter.git`

# Change directory to the cloned repository
`cd eliza-starter`

# Create an environment file
`cp .env.example .env`

# Add direct client to environment file
1. open .env file
2. change<br/>
~~//clients: [],~~
```
clients: [Clients.DIRECT],
```
3. change<br/>
~~//modelProvider: ModelProviderName.OPENAI,~~
```
modelProvider: ModelProviderName.OLLAMA,
```

![character.ts](/assets/images/default_eliza_env_settings.png)

# Install the node modules required by the Eliza agent 
`pnpm i`

# Start the default Eliza agent
`pnpm start`

# Chat with you Eliza agent
- Type after the "You:" prompt <br/>
*Note The first time, your computer will download a small ollama model*
![agent terminal](/assets/images/eliza_hello_world_terminal.png)
<br/><br/>

---
This completes your hello world Eliza introduction<br/> 
Congratulations you have successful run your first Ai Agent 

