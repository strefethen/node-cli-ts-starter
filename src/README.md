Setting up a Node TypeScript CLI starter app.

    $ npm init
    $ tsc --init
    $ mkdir src
    $ mkdir build

Edit the tsconfig.json file:

    // Edit tsconfig.json and adjust the following:
    {
        "compilerOptions": {
            "target": "es6",
            "lib": ["esnext"],
            "allowJs": true,
            "checkJs": true,
            "sourceMap": true,
            "outDir": "./build",

            /* Module Resolution Options */
            "moduleResolution": "node",
            "types": ["node"],

            "watch": true
        },
        "include": [
            "src"
        ],
        "exclude": [
            "node_modules",
            "**/*.spec/ts"
        ]
    }

In VSCode:

Setup the TypeScript compiler to watch for source modifications:

* Select Terminal | Run Build Task... select "tsc: watch - tsconfig.json"
* Click the Debugger icon
    * Click the gear icon next to the debugger dropdown
    * Select Node.js
* Edit launch.json
    * Change "program" to point to: "${workspaceFolder}/build/App.js",
* Create a new file and save it as App.js



Continue setting up the project:

    $ npm install --save-dev @types/node

