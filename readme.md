# [DRAFT] ServiceNow SDK Project 

This project is a test to see how I can develop for **ServiceNow** using **VS Code** instead of working directly in the **ServiceNow** web interface. The main goal is to try out **Claude Code** as an AI partner to see how much it can help me write and build applications faster.

This application is developed using the **ServiceNow SDK**, **VS Code**, and **Claude Code**. It utilizes **React** with **Fluent UI** (ready-to-use building blocks, like buttons, lists, etc) for the frontend and TypeScript for server-side logic.

## Prerequisites

* **[Node.js](https://nodejs.org/en/download)**: Version v20.x.x or higher is required.

* **ServiceNow SDK**: Install the SDK globally so the `now-sdk` CLI is available from any directory. 

Can be installed via: 
```bash
npm install -g @servicenow/sdk
```

Verify version (expected output: 4.4.0 or later): 
```bash
now-sdk --version
```

* **Claude Code**: Requires a Claude Pro, Max, or Team subscription. When installed locally, it can be installed via: 

```bash
npm install -g @anthropic-ai/claude-code
```

* **ServiceNow PDI (Personal Developer Instance)**: Can be ordered for free on [https://developer.servicenow.com/](https://developer.servicenow.com/).

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/youraccount/your-project-name.git
cd your-project-name
```

### 2. Install Dependencies
```bash
npm install
```

To check version: 
```bash
npm --version
```

### 3. Authentication
To connect the project to your ServiceNow Personal Developer Instance (PDI). The PDI example https://**dev123456**.service-now.com/, and it must be active (ensure you are logged in to the developer portal):
```bash
now-sdk auth --add dev123456 --type oauth
```
Follow the prompts in your browser to complete the OAuth authentication process. Copy the code provided in the browser. 

Please note: When pasting the code into the terminal, the characters will not be visible. Paste it once and press Enter. 

### 4. Claude Code "sndev" Skill Setup 
A "skill" is a knowledge file that teaches Claude Code (AI) about the ServiceNow SDK and Fluent API. Follow these steps to install it:

1. Create the skills directory: 
```bash
mkdir -p ~/.claude/skills/sndev
```
2. Download and copy the skill file: 
```bash


### 5. Development with Claude Code
To initialize the AI assistant:
```bash
claude
```

## Deployment

To deploy your local code changes to the connected ServiceNow instance, execute the following command:
```bash
now-sdk deploy
```

## Project Structure
* **src/fluent/**: Contains metadata and server-side logic defined in TypeScript.
* **src/client/**: Contains React components and Fluent UI assets for the user interface.
* **now.config.json**: Configuration settings for the ServiceNow instance connection.


