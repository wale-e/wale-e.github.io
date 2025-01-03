---
title:  "CrewAi: Hello World"
date:   2025-01-03 09:14:00 -0000
categories: ai agent framework
---

# Create a Senior Data Researcher and Reporting Analyst agent for any Topic
---    
[CrewAi](https://github.com/crewAIInc/crewAI) requires **Python** version >=3.10 <3.13 installed on your system.  
Using **Homebrew** for package management on macOS (Please use something similar for your OS if not macOS)  
Using **Ollama** as provider for llama3.1 model

# Download and install Ollama for your OS
[Ollama Website](https://ollama.com/)

# Pull down the llama3.1 model
```shell
ollama run llama3.1
```

# Confirm Ollama is running in a browser
[Open Local Ollama](http://localhost:11434/)
- if running, should see a respone "Ollama is running"

# Install Python version 3.12
```shell
brew install python@3.12
```

# Install pipx
```shell
brew install pipx
```

# Ensure pipx is in your PATH
```shell
pipx ensurepath
```

# Install CrewAi using pipx
```shell
# tell pipx to use Python version 3.12
pipx install crewai --python /opt/homebrew/bin/python3.12
```

# Create your project
```shell
# crewai create crew <project_name>
crewai create crew crewai_hello_world
```

# Choose ollama as your provider (Option: 5)

# Choose llama3.1 as your model (Option: 1)

# Change to project directory
```shell
cd crewai_hello_world
```

# Create a virtual environment
```shell
python3 -m venv venv
```

# Activate the virtual environment
```shell
source venv/bin/activate
```

# Modify src/crewai_hello_world/main.py to update topic for your agents and tasks.
```python
# replace every occurence of the topic "AI LLMs" (3 in total)
'topic': 'AI LLMs'
# with
'topic': 'AI Agents'
```
# Modify src/crewai_hello_world/config/tasks.yaml to update the year.
```yaml
# replace 
2024
# with
2025
```

# Install CrewAi in virtual environment
```shell
pip install crewai
```
# Run Your Crew
```shell
crewai run
```

# Output I got below
![data reseacher](/assets/images/crewai_data_researcher.png)
![report_analyst](/assets/images/crewai_report_analyst.png)
