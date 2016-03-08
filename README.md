# Basic Seed (00)
## Based on [Rob Wormald](https://gist.github.com/robwormald/429e01c6d802767441ec)
<pre><code>
$ npm init -y
$ npm install --save-dev jspm
$ jspm init   // 7 x OK + typescript
$ jspm install ts angular2 zone.js reflect-metadata
 
@edit system.config:
    System.config({
        "baseURL": "/",
        "defaultJSExtensions": true,
        "transpiler": "typescript",
        "typescriptOptions":{
            "module":"commonjs",
            "emitDecoratorMetadata": true
        }, 
        "packages": {
            "app": {
                "main": "app",
                "defaultExtension": "ts" 
            }
        },    
        ...
        "paths": {
            "github:*": "jspm_packages/github/*",
            "npm:*": "jspm_packages/npm/*",
            
            //this lets us use app/ for our package as a sort of virtual directory
            "app": "src"
        },
        ...
    });    

@create file structure and files
    index.html 
    /src
        app.html
        app.ts
        /components or /app ??
      
@edit index.html
@edit app.ts
@edit app.html
</code></pre>
* run code with live-server