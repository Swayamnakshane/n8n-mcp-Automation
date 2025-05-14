#  AI Automation with n8n, Docker CLI, and mCP – Step-by-Step Guide

Hey everyone! 🚀
In this post, you’ll learn how to *install n8n using Docker CLI* (no Docker Desktop required) and take your automation skills to the next level using *mCP (Model Context Protocol)*.

Imagine your AI being able to connect with any tool or API automatically – no complicated code, no headaches. That’s what mCP does – it makes automation 10x easier and smarter.

---

## 🔧 What You’ll Learn

✅ Install n8n for free using Docker CLI
✅ Set up mCP in n8n to unlock AI superpowers
✅ Let AI dynamically choose and execute tools
✅ Automate web searches and scraping
✅ Bonus: Learn a powerful trick even experts miss!

---

## 🚀 Step 1: Install Docker CLI

If you haven’t already, [install Docker Engine](https://docs.docker.com/engine/install/) on your system:

* Linux: Follow your distro’s instructions
* macOS & Windows: Install Docker Desktop, then use CLI commands (Docker Desktop still required on these platforms for the engine)

To verify Docker is working:

bash
docker --version


---

## 🐳 Step 2: Run n8n Container Using Docker CLI

### 1. Create a local folder for storing n8n data

bash
mkdir -p ~/n8n-data


### 2. Run n8n container with required settings

bash
docker run -it --name n8n-container \
  -p 5678:5678 \
  -v ~/n8n-data:/home/node/.n8n \
  -e N8N_ENABLE_COMMUNITY_NODES=true \
  n8nio/n8n


*Explanation:*

* -it: Run interactively
* --name: Name your container
* -p 5678:5678: Map local port 5678 to container
* -v: Mount volume for data persistence
* -e: Set environment variable to enable community nodes
* n8nio/n8n: Official n8n Docker image

Once the container starts, open your browser and go to:

------------------------------------------------------------------------------------------------------------------------------------------------------------
"C:\Users\swaya\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 212600.png"
------------------------------------------------------------------------------------------------------------------------------------------------------------

http://localhost:5678 (aws ip address)


You should see the n8n signup page!

------------------------------------------------------------------------------------------------------------------------------------------------------------
"C:\Users\swaya\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 212319.png"
------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🧠 Step 3: Create a New Account and Start Your Workflow

1. Sign up with your email and password
2. Click to create a new workflow
3. You’re now inside n8n and ready to build!

---

## 🧩 Step 4: Install mCP Nodes in n8n

1. Go to *Settings → Community Nodes*
2. Search for n8n-nodes-mcp
3. Click *Install*
4. Wait for installation to finish

Now you can use mCP in your automations!

---

## 🛠 Step 5: Create Your First AI Agent Workflow

### Add Nodes:

* *Chat Trigger Node* – To start on user input
* *AI Agent Node* – Set up with OpenAI (add your API key)
* *Simple Memory Node* – Helps maintain conversation history

Now let’s bring in the mCP power!

---

## 🔌 Step 6: Connect mCP with n8n

### Add mCP Client Node:

1. Action: List Tools
2. Set up credentials using Brave API
3. use this repository to setup brave using api: https://github.com/Swayamnakshane/servers.git
4. Use CLI or browser to get your API key from [Brave Search](https://search.brave.com/)

bash
# This is an example of mCP setup inside n8n via node config
# Fill in API key and Brave server name in node settings


Test the node. It should show available tools from the Brave mCP server (like search, details, etc.)

---

## 🤖 Step 7: Let the AI Use Those Tools

1. Add a new mCP node to *Execute Tool*
2. Choose a tool like “search”
3. Let AI define parameters automatically
4. Add a *System Message* like:

   > "You are a helpful assistant using Brave search to answer questions."

Make sure all nodes are connected correctly.

---

## 🧪 Step 8: Run and Test!

Open the chat input and ask:

> “Find a nearby coffee shop.”

The workflow will:

* Capture your question
* AI will decide to use Brave Search
* Get the result
* Format and show it back to you

Magic. 💫

---

## 🎉 Conclusion

By using Docker CLI + n8n + mCP, you’ve created an AI system that can *use real tools, make decisions, and fetch live data* — all with *zero code*.


connect with me :
linkedin: Swayamnakshane4
_____________________________________________________________________________________________________________________________________________________________

"C:\Users\swaya\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 212600.png"

_____________________________________________________________________________________________________________________________________________________________

"C:\Users\swaya\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 212319.png"

______________________________________________________________________________________________________________________________________________________________










