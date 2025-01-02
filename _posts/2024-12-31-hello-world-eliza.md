---
title:  "Eliza: Hello World"
date:   2024-12-31 15:28:00 -0000
categories: ai agent framework
---

# Create your first Eliza Agent  
> Assumption: you already have git, node, and pnpm installed  
> For **git**: [Find instructions to install git](https://github.com/git-guides/install-git)<br/>
> For **node**: [Visit the Node.js website](https://nodejs.org) and download the appropriate installer for your operating system. Once downloaded, run the installer and follow the on-screen instructions. After a successful installation, you’ll have access to the node and npm command in your terminal or command prompt.
> For **pnpm**: In a terminal, run the command `npm install -g pnpm`

---
Used the following versions when writing this blog  
node - v23.2.0  
npm - 10.9.0  
pnpm - 9.12.3  

---

<br/>  
*Open a command line terminal and run the following commands*

# Clone the Eliza Starter Repository
```shell
git clone https://github.com/elizaOS/eliza-starter.git
```

# Change directory to the cloned repository
```shell 
cd eliza-starter
```

# Create an environment file
```shell
cp .env.example .env
```

# Add direct client and ollama model to character file
1. open /src/character.ts file
2. change  
~~//clients: [],~~
```
clients: [Clients.DIRECT],
```
3. change  
~~//modelProvider: ModelProviderName.OPENAI,~~
```
modelProvider: ModelProviderName.OLLAMA,
```

![character.ts](/assets/images/default_eliza_env_settings.png)

# Install the node modules required by the Eliza agent 
```shell
pnpm i
```

# Start the default Eliza agent
```shell
pnpm start
```

# Chat with you Eliza agent
- Type after the "You:" prompt  
*Note The first time, your computer will download a small ollama model*
![agent terminal](/assets/images/eliza_hello_world_terminal.png)
<br/><br/>

---
This completes your hello world Eliza introduction   
Congratulations you have successful run your first Ai Agent 

