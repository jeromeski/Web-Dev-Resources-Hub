To run the command `NODE_OPTIONS=--max-old-space-size=4096 next build` directly without using `cross-env`, you can set the environment variable `NODE_OPTIONS` directly in your terminal. Here's how you can do it for different operating systems:

**For Windows (using PowerShell):**
```powershell
$env:NODE_OPTIONS="--max-old-space-size=4096"
next build
```

**For Linux or macOS:**
```bash
export NODE_OPTIONS=--max-old-space-size=4096
next build
```

After setting the `NODE_OPTIONS` environment variable, you can proceed with the `next build` command, and it should work with the specified maximum old space size.

Source: Conversation with Bing, 5/4/2024
(1) 'NODE_OPTIONS' is not recognized as an internal or external command .... https://stackoverflow.com/questions/67993622/node-options-is-not-recognized-as-an-internal-or-external-command-still-an-i.
(2) Node.js — How to read environment variables from Node.js. https://nodejs.org/en/learn/command-line/how-to-read-environment-variables-from-nodejs.
(3) node.js - How to use the NODE_OPTIONS environment variable to set the .... https://stackoverflow.com/questions/56742334/how-to-use-the-node-options-environment-variable-to-set-the-max-old-space-size-g.
(4) Environment variables in Node.js. The Right way! - DEV Community. https://dev.to/numtostr/environment-variables-in-node-js-the-right-way-15ad.