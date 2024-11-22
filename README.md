# My Nodejs Modules

> References:
>> https://docs.npmjs.com/creating-node-js-modules
>> https://medium.com/@oresoftware/node-js-how-to-test-your-new-npm-module-without-publishing-it-every-5-minutes-3b6f8e0491dd
>
> This document was produced during my personal development day at Voneus

This project is intended to demonstrate how to create, publish and add a nodejs dependency to a project.

## Starts a new Project

To starts a new Nodejs project just run ** npm init ** and following the questions.

```
npm init
```

## The Entry Point

Now need to create a javascript file to be the project's entry point, understanding that everything will be executed from it.
just add an index.js on the project root.

New you can write the module inside of the index.js file.

## Testing Locally

So that you can add your module locally, you can install it using the patch for the local repository.

```
npm install /absolute/local/path/to/your/other/package
```

Keep in mind, any change on the module will be necessary reinstall

> How workaround then?

It's simple load the module straight from the module folder

### Instead that

```
const myModule = require('my-node-module').default;
myModule();
```

### Do that

```
const myModule = require('/absolute/local/path/to/your/other/package').default;
myModule();
```

## Publishing

