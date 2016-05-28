
Light set-up for ecmascript6 dev

        mkdir proj
        cd proj
        npm init
        npm install babel-cli babel-preset-es2015 --save-dev
        mkdir src
        touch src/index.js


Your `package.json` file should contain the following `main` and `script` declarations:


        {
          "main": "src/index.js",
          "scripts": {
            "build": "babel src/ --presets babel-preset-es2015 --out-dir dist",
            "start": "npm run build && node dist/index.js"
          },
        }

This makes your `npm run build` use babel to transpile the code in the `src` dir into the `dist` dir.

`npm start` calls build, then runs the transpiled code in `dist/index.js`.


