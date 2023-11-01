## **Setting up a TypeScript Project**

* Create a new NPM or NPX project.
* Install TypeScript and ts-node (for compiling) as development dependencies:

```bash
npm i typescript ts-node -D
```

Configure TypeScript in your project:
```bash
tsc --init
```

To run a TypeScript file without compiling, use the following command:
```bash
ts-node <file-name>.ts
```

To compile a TypeScript file to JavaScript, use the following command:
```bash
tsc <file-name>.ts
```
This will create a JavaScript file with the same name as the TypeScript file.

Run the JavaScript file using the Node.js runtime:
```bash
node <file-name>.js 
//OR 
nodemon <file-name>.js
```

**Note:** Install ts-node in development dependencies for running TypeScript files during development.

## **Compiling TypeScript Files to JavaScript**

To compile a TypeScript file to JavaScript, use the following command:

```bash
tsc <file-name>.ts
```
This will create a JavaScript file with the same name as the TypeScript file.

## **Running JavaScript Files**
To run a JavaScript file, use the following command:

```bash
node <file-name>.js 
//OR 
nodemon <file-name>.js
```
