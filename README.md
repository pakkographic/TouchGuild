---
  TouchGuild is a library that supports TS, JS (cjs and esm) and it was built to let you interface with the Guilded API. It
  has easy & predictable types, some of them are inspired by Discord Eris.

---

# EARLY ACCESS COMING SOON!
If you read this, it means it's still not release, we're publishing the library soon, and probably within' the end of the week. See ya!

# 🌟 Get started

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FlOPMbaW5t7rQZWQ9C6lG%2Fuploads%2F18hrn4NpcdDAZzNo1Ape%2Ftouchguild-banner.png?alt=media&token=7ccb1380-65eb-44d6-b978-d68fe33048f5" alt=""><figcaption></figcaption></figure>

## Get started, it's easy.

You'll need to download Node (npm), sorry yarn users but it's not for now.

### Install the package

```bash
npm install touchguild@latest --save-dev
```

### Basic scripting (ping, pong!)

Let's get started, it'll be easy examples for ya!

For example, we'll create a simple ping pong script, a well known command!

Javascript & Typescript:

```javascript
const TouchGuild = require('TouchGuild') // import for CommonJS
// import TouchGuild from 'TouchGuild' // import for ESM & TS

const Client = new TouchGuild.Client({token: 'insert token here'}) // create client

Client.connect();

Client.on('messageCreate', (message)=> {
    // Detects when a message is created and executes the code here.
    if (message.member.bot == true) return; // ignores bot messages.
    if (message.content == '!ping'){
        // if the message command is !ping, it executes the code here.
        message.createMessage({content: 'pong!'}); // create a message.
    }
});
```
