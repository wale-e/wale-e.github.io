---
layout: post
title:  "Rig: Hello World"
date:   2025-01-01 13:20:00 -0000
categories: ai agent framework
---

# Assumptions<br/>
> You already have git, cargo, and rust installed<br/>
> For **git**: [Find instructions here](https://github.com/git-guides/install-git)<br/>
> For **rust and cargo**: [Find instructions here](https://www.rust-lang.org/tools/install)

**Check out my GitHub repository for the source code [Rig Hello World](https://github.com/wale-e/rig_hello_world)**  

*Open a command line terminal and run the following commands*

# Install Rust
*If you haven't installed Rust yet, install it using rustup*  
`curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`

# Create a new Rust project
`cargo new rig_hello_world`

# Change to the newly created project directory
`cd rig_hello_world`

# Add rig-core, tokio, and anyhow dependency to Project
```
cargo add rig-core
cargo add tokio --features full
cargo add anyhow
```

# Download and install Ollama for your OS
[Ollama Website](https://ollama.com/)

# Pull down the llama3.2:1b model
`
ollama run llama3.2:1b
`

# Confirm Ollama is running in a browser
[Open Local Ollama](http://localhost:11434/)
- if running, should see a respone "Ollama is running"

# Replace the content of src/main.rs with below
```
/// This example requires that you have the [`ollama`](https://ollama.com) server running locally.
use rig::{completion::Prompt, providers};

#[tokio::main]
async fn main() -> Result<(), anyhow::Error> {
    // Create an OpenAI client with a custom base url, a local ollama endpoint
    // The API Key is unnecessary for most local endpoints
    let client = providers::openai::Client::from_url("ollama", "http://localhost:11434/v1");

    // Create agent with a single context prompt
    let comedian_agent = client
        .agent("llama3.2:1b")
        .preamble("You are a comedian here to entertain the user using humour and jokes.")
        .build();



    // Prompt the agent and print the response
    let response = comedian_agent.prompt("Entertain me!").await?;
    println!("{}", response);

    Ok(())
}
```

# Run the Rig agent
`cargo run`  

* Output should be a joke from the llama model

---
This completes your hello world Rig introduction<br/> 
Congratulations you have successful run your first Rig Ai Agent 

