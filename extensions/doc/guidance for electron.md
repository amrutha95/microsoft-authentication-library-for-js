In case you are developing an Electron application and want to use this extension for caching tokens, you may run into an error that looks like the following:
```The module C:\...\dpapi.node' was compiled against a different Node.js version using NODE_MODULE_VERSION 85. This version of Node.js requires NODE_MODULE_VERSION 80...```

To resolve this error, follow these steps: 
* Install electron-rebuild with the command: ```npm i -D electron-rebuild```
* Remove the file ```packages-lock.json```
* Run ```npm i``` to install non-installed modules
* And finally run ./node_modules/.bin/electron-rebuild

