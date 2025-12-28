# 📥 Claude-Code-With-Qwen-For-Free

**To run Claude Code with Qwen for free, you need the following**:
* **Qwen CLI** (installed and authenticated)
* Node.js v18 or uper versions

#  ✅ Check Node.js is Install or Not:

**Open command Propmt and run this command**:

```bash
node --version
```

**If it shows the version of your Node.js then go to next step otherwise click on this link https://nodejs.org/en and install Node.js**

#  ▶️ Step : 1 Open command prompt:

Open Command Prompt: 

* Press the **Windows** key
* Search for **cmd**

# 🛠️ Step : 2 Qwen CLI Installation:  
Install the latest Qwen Code CLI through this command:

```bash
npm install -g @qwen-code/qwen-code@latest
```

Verify the installation is complete or not:

```bash
qwen --version
```

# 🧩 Step : 3 Installation Of Claude Code and Claude Code Router: 
Install Claude Code and Claude Code Router globally Through ThIs Command:

```bash
npm install -g @anthropic-ai/claude-code @musistudio/claude-code-router
```

#  📁 Step : 4 Create Required Folders:
You Have to create 2 folders in this direction: 

**C:\Users\PC_USER**



- Name Of 1 Folder:
```bash
.claude
```
- Name Of 2 Folder:
```bash
.claude-code-router
```

# 📄 Step : 5 Access Your Qwen Token:

Go in this Direction and Find for the file Named **"oauth_creds.json"** Opne this file , Here is your Access Token 

When You Open file you see something like this: 
```json
{
  "access_token": "YOUR_QWEN_ACCESS_TOKEN_HERE",
  "token_type": "Bearer",
  "refresh_token": "YOUR_QWEN_REFRESH_TOKEN_HERE",
  "resource_url": "portal.qwen.ai",
  "expiry_date": 1764876220290
}
```

# 📄 Step : 6 Create a File:

**Open Notepad and paste this:
```bash
{  
  "LOG": true,  
  "LOG_LEVEL": "info",  
  "HOST": "127.0.0.1",  
  "PORT": 3456,  
  "API_TIMEOUT_MS": 600000,  
  "Providers": [  
    {  
      "name": "qwen",  
      "api_base_url": "https://portal.qwen.ai/v1/chat/completions",  
      "api_key": "YOUR_QWEN_ACCESS_TOKEN_HERE",  
      "models": [  
        "qwen3-coder-plus",  
        "qwen3-coder-plus",  
        "qwen3-coder-plus"  
      ]  
    }  
  ],  
  "Router": {  
    "default": "qwen,qwen3-coder-plus",  
    "background": "qwen,qwen3-coder-plus",  
    "think": "qwen,qwen3-coder-plus",  
    "longContext": "qwen,qwen3-coder-plus",  
    "longContextThreshold": 60000,  
    "webSearch": "qwen,qwen3-coder-plus"  
  }  
}
```

### Now you have to replace    "YOUR_QWEN_ACCESS_TOKEN_HERE"     with your actual    "ACCESS_TOKEN"     and save the file in this direction **"C:\Users\PC_USER\\.claude-code-router"** and you "MUST" have to name this file excat as:
```bash
config.json
```

# 🚀 Step : 7 Start Claude Code with Qwen:

**Open Command Propmt and Run this Command**: 
```bash
ccr start
```

**Open New Command Prompt and Run this Command❗Don't Close the Previous Command prompt**
```bash
ccr code
```

**Now Test it's Working or Not by Saying**:
```
hi
```

### Expected: Claude responds with a greeting confirming it's working! ✅ Success!

## 🎉 Congratulations You Successfully Run Claude Code With Qwen 🎉 
