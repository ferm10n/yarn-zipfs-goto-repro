# goto-repro

## Steps to reproduce

- open project in vscode (tested with 1.58.2)
- accept allowing the workspace version of typescript to be used
- disable all extensions (optional)
- run `yarn install` and then `yarn dlx @yarnpkg/sdks vscode`
- install extensions for vscode: arcanis.vscode-zipfs@2.3.0 octref.vetur@0.34.1
- open `index.js`, and see that you can ctrl+click `'vue'` to go to definition. this works
- open `page.vue`, and see that you cannot ctrl+click `'vue'` to go to definition. this does not work and produces this error:
```
Unable to open 'index.d.ts': Unable to read file 'c:\Users\John\Downloads\goto-repro\.yarn\cache\vue-npm-2.6.14-3223a78650-542787dc83.zip\node_modules\vue\types\index.d.ts' (Error: Unable to resolve non-existing file 'c:\Users\John\Downloads\goto-repro\.yarn\cache\vue-npm-2.6.14-3223a78650-542787dc83.zip\node_modules\vue\types\index.d.ts').
```