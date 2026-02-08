<p align="center">

  <a href="####"><img src="http://readme-typing-svg.herokuapp.com?color=cyan&center=true&vCenter=true&multiline=false&lines=`🔰Rahat_Boss🔰`" alt=""></a>

</p>


<a><img src='https://i.imgur.com/LyHic3i.gif'/></a>


<br />

<p align="center">

    <a href="https://github.com/XrahatX/Xrahat">

        <img src="https://i.imgur.com/9pBmbf3.gif" alt="Logo">

    </a>

</p>


<p align="center">

  <!-- GitHub -->

  <a href="https://github.com/XrahatX/Xrahat.git" target="_blank">

    <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"

      width="40"

      height="39"

      style="border-radius:100%; margin-right:50px;"

      alt="GitHub">

  </a>

 <!-- Facebook -->

  <a href="https://www.facebook.com/share/1AWBvSfV1P/" target="_blank">

    <img src="https://upload.wikimedia.org/wikipedia/commons/5/51/Facebook_f_logo_%282019%29.svg"

      width="33"

      height="33"

      style="border-radius:100%;"

      alt="Facebook">

  </a>

</p>


### <br>   ❖ DEPLOY_WORKFLOWS ❖

<a><img       

src='https://i.imgur.com/LyHic3i.gif'/></a>

```
name: Node.js CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [20.x]
        # See supported Node.js release schedule at https://nodejs.org/en/about/releases/

    steps:
    # Step to check out the repository code
    - uses: actions/checkout@v2

    # Step to set up the specified Node.js version
    - name: Use Node.js ${{ matrix.node-version }}
      uses: actions/setup-node@v2
      with:
        node-version: ${{ matrix.node-version }}

    # Step to install dependencies
    - name: Install dependencies
      run: npm install

    # Step to run the bot with the correct port
    - name: Start the bot
      env:
        PORT: 8080
      run: npm start
```

<a><img       

src='https://i.imgur.com/LyHic3i.gif'/></a>


___


### 📋 Table of Contents


· ⚠️ Important Disclaimer


· ✨ Features


· 🚀 Installation Guide


· ⚙️ Configuration


· 📖 Usage Guide


· 🔧 Advanced Setup


· ❓ FAQ


· 🤝 Contributin


· 📄 License


---

## ⚠️ Disclaimer & Credits


This repository is a custom fork of the original miraiv2 framework.


I do NOT claim ownership of the original project.

All original rights and credits go to the original developer:

https://github.com/m1raibot/miraiv2.git


This project is shared strictly for educational and personal use only.


🚫 I am not responsible for any misuse, account bans, platform restrictions,

or violations of rules, policies, or terms of service.

### ✨ Features


Feature Description Status

🤖 Automated Messaging Send automated responses ✅


📁 File Handling Support for various file types ✅


⚡ Fast Performance Optimized Node.js runtime ✅


🔒 Secure AppState authentication ✅


📊 Logging Detailed activity logs ✅


🔧 Customizable Easy to modify and extend ✅


🌐 Multi-platform Works on various systems ✅


---

## 📹 𝗦𝗲𝘁𝘂𝗽 𝗧𝘂𝘁𝗼𝗿𝗶𝗮𝗹

[![Watch Tutorial](https://img.youtube.com/vi/QiQG__QRpoM/hqdefault.jpg)](https://youtu.be/QiQG__QRpoM?si=dTFDVRzAGQtmO7EE)

Click thumbnail to watch full tutorial.

### 🚀 Installation Guide


Prerequisites


· Node.js (v16 or higher)

· Git

· Facebook Developer Account (for testing)


Step-by-Step Installation


```bash

# 1. Clone the repository

git clone https://github.com/XrahatX/Xrahat.git


# 2. Navigate to project directory

cd Xrahat


# 3. Install dependencies

npm install


# 4. Install additional packages if needed

npm install chalk fs-extra axios

```

---

⚙️ Configuration

1. AppState Setup

```javascript

// Create appstate.json in root directory

{

  "cookies": [

    // Your Facebook cookies here (for educational purposes only)

  ]

}

```

1. Environment Variables

Create a .env file:

```env

PORT=3000

NODE_ENV=development

PREFIX=!

ADMIN_ID=your_facebook_id

AUTO_REPLY=true

```

1. Bot Configuration

Edit config.json:

```json

{

  "autoReply": true,

  "listenEvents": true,

  "selfListen": false,

  "online": true,

  "markRead": true,

  "logMessageEvents": false

}

```

---

📖 Usage Guide

Starting the Bot

```bash

# Development mode

npm run dev


# Production mode

npm start


# With debugging

DEBUG=* node Xrahat.js

```

Basic Commands

```

!help - Show all commands

!info - Bot information

!ping - Check bot status

!admin - Admin commands

!uptime - Check bot uptime

!version - Show bot version

```

File Structure

```

Xrahat/

├── Xrahat.js          # Main bot file

├── package.json       # Dependencies

├── config.json        # Configuration

├── appstate.json      # Authentication

├── commands/          # Command modules

├── events/            # Event handlers

├── utils/             # Utility functions

├── plugins/           # Additional plugins

└── README.md          # Documentation

```

Docker Deployment

```dockerfile

FROM node:18-alpine

WORKDIR /app

COPY package*.json ./

RUN npm ci --only=production

COPY . .

EXPOSE 3000

CMD ["node", "Xrahat.js"]

```

PM2 Process Manager

```bash

# Install PM2 globally

npm install -g pm2


# Start bot with PM2

pm2 start Xrahat.js --name "rahat-bot"


# Save process list

pm2 save


# Set up startup script

pm2 startup


# Monitor logs

pm2 logs rahat-bot

```

---

❓ FAQ

Q1: Is this bot safe to use?

A: Only in controlled, educational environments. Never use on production accounts.

Q2: Will my account get banned?

A: Using automation tools violates Facebook's ToS. Use at your own risk with test accounts only.

Q3: How to get appstate?

A: Use browser developer tools to extract cookies from a Facebook session (for educational purposes only).

Q4: Can I add custom commands?

A: Yes! Create new files in the commands/ directory following existing patterns.

Q5: Error: Cannot find module

A: Run npm install to ensure all dependencies are installed.

Q6: How to update the bot?

A: Pull latest changes and run npm install again.

---

🤝 Contributing

We welcome ethical contributions for educational purposes:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

Contribution Guidelines

· Add clear comments

· Update documentation

· Follow existing code style

· Include tests if applicable

· Respect privacy and security

---

<!-- LICENSE -->
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file.

---

🔗 Important Links

Resource Link

📚 Documentation GitHub Wiki

🐛 Issue Tracker GitHub Issues

💬 Discussion Facebook Group

📢 Updates Follow on GitHub

---

🌟 Support & Community

Connect with Developer

· Facebook: Rahat Islam

· GitHub: @XrahatX

Special Thanks🩵🩵🩵

· Rx Abdullah - For guidance and support

· Open Source Community - For inspiration

· All Contributors - For educational improvements

<p align="center">

  <img src="https://i.imgur.com/LyHic3i.gif" width="50">

  <br>

<em>Happy Coding! 🚀</em>

</p>

```


---


### 📦 package.json


```json

{

  "name": "xrahat",

  "version": "1.0.0",

  "description": "Facebook Messenger Bot for educational purposes",

  "main": "Xrahat.js",

  "scripts": {

    "start": "node Xrahat.js",

    "dev": "nodemon Xrahat.js",

    "test": "echo \"Error: no test specified\" && exit 1"

  },

  "keywords": [

    "messenger",

    "bot",

    "facebook",

    "automation",

    "educational"

  ],

  "author": "Rahat Islam",

  "license": "MIT",

  "dependencies": {

    "axios": "^1.6.0",

    "chalk": "^4.1.2",

    "facebook-chat-api": "github:Schmavery/facebook-chat-api",

    "fs-extra": "^11.1.1",

    "moment": "^2.29.4",

    "node-cron": "^3.0.3"

  },

  "devDependencies": {

    "nodemon": "^3.0.1"

  }

}

```

---

⚙️ config.json

```json

{

  "language": "en",

    "keyActive": "",

    "DeveloperMode": false,

    "autoCreateDB": true,

    "notiGroup": true,

    "NOTIFICATION": true,

    "allowInbox": false,

    "autoClean": true,

    "commandDisabled": 

        "sim.js"

}

```

---

🚫 .gitignore

```

node_modules/

appstate.json

.env

*.log

.DS_Store

npm-debug.log*

yarn-debug.log*

yarn-error.log*

.vscode/

.idea/

```

---

📜 LICENSE

```

MIT License


Copyright (c) 2026 XrahatX


Permission is hereby granted, free of charge, to any person obtaining a copy

of this software and associated documentation files (the "Software"), to deal

in the Software without restriction, including without limitation the rights

to use, copy, modify, merge, publish, distribute, sublicense, and/or sell

copies of the Software, and to permit persons to whom the Software is

furnished to do so, subject to the following conditions:


The above copyright notice and this permission notice shall be included in all

copies or substantial portions of the Software.


THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR

IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,

FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE

AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER

LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,

OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE

SOFTWARE.

```

💡 How to Use These Files:

1. Create a new GitHub repository
2. Copy each section above separately
3. Create corresponding files in your repository
4. Paste the content into each file
5. Commit and push to GitHub

Files to create:

· README.md (copy the main README content)

· package.json

· config.json

· .gitignore

· LICENSE

· .github/workflows/main.yml

Note: Remember to replace placeholder links and IDs with your actual information.

👇👋original fork👋👇

<a><img

src='https://i.imgur.com/LyHic3i.gif'/></a>

<p align="center">

  <a href="https://github.com/XrahatX/Xrahat.git" target="_blank">

 </a>

</p>

<p align="center">

  <img src="https://i.imgur.com/LyHic3i.gif" width="100%">

</p>

<h3 align="center">

<code>🔰 Educational Tool Only - Use Responsibly 🔰</code>

</h3>

<div align="center">

📊 Repository Stats

https://img.shields.io/github/stars/XrahatX/Xrahat?style=for-the-badge

https://img.shields.io/github/forks/XrahatX/Xrahat?style=for-the-badge

https://img.shields.io/github/issues/XrahatX/Xrahat?style=for-the-badge

https://img.shields.io/github/license/XrahatX/Xrahat?style=for-the-badge

</div>