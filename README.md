# MongoDB - ExpressJS - Svelte (Smelte) - NodeJS

https://github.com/Matttweb/MESN

https://github.com/matyunya/smelte

https://smeltejs.com/components/cards

https://npm.runkit.com/smelte

https://www.npmjs.com/package/smelte

The project basically consists of allowing you to create an account in which you will store different products of what you want which will have name, price per unit and an image, you also have the option to create an order that has different products in different quantities, when creating the order also creates a pdf file with all the data including the date and time of creation.. This is a very basic practical example to get started in the world of web development with frameworks.

You can watch the full youtube tutorial on how to make this practical example step by step [here](https://www.youtube.com/playlist?list=PL3f738vgxpbgIJ_XqrDZCZde3s_d5siN5)

> mesn-be

This folder contains all the backend of the project but also in its public folder it has all the frontend that is generated when you run `$ npm run build` in a vue project, this makes you can see the whole project when you run the `$ npm run dev` script

> mesn-fe

This folder contains the whole frontend of the project made with Svelte and has a connection to our api through axios which is in the `pevn-be` folder so make sure that when you run the `$ npm run dev` script you first start the api by running `$ npm run dev` from the `mesn-be` folder.

Please do not forget this

```
npm install
```

## Backend works

```java
cd mesn-be
npm run dev
```

Output

```java
> mesn-be@1.0.0 dev
> nodemon src/ --exec babel-node

[nodemon] 2.0.7
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting `babel-node src/`
Server on port 3000
Database is connected
```

## Frontend does not compile

```java
cd mesn-fe
npm run dev
```

```java
> svelte-app@1.0.0 dev
> rollup -c -w

rollup v2.46.0
bundles src/main.js → public/build/bundle.js...
(!) Plugin svelte: A11y: A form label must be associated with a control.
node_modules/smelte/src/components/Checkbox/Label.svelte
20: </script>
21:
22: <label
    ^
23:   aria-hidden="true"
24:   {...$$props}
node_modules/smelte/src/components/Slider/Slider.svelte
52: </script>
53:
54: <label>{label}</label>
    ^
55: <input
56:   use:applyColor
node_modules/smelte/src/components/TextField/Label.svelte
71: </style>
72:
73: <label class="{lClasses} {$$props.class}" {...props}>
    ^
74:   <slot />
75: </label>
node_modules/smelte/src/components/Switch/Switch.svelte
67:     </Ripple>
68:   </div>
69:   <label aria-hidden="true" class={l}>
      ^
70:     {label}
71:   </label>
(!) Plugin svelte: "queue" is declared in a module script and will not be reactive
node_modules/smelte/src/components/Snackbar/Snackbar.svelte
58:
59:   $: if (value) {
60:     queue.update(u => [...u, toggler]);
        ^
61:   }
62:
(!) Plugin svelte: "running" is declared in a module script and will not be reactive
node_modules/smelte/src/components/Snackbar/Snackbar.svelte
61:   }
62:
63:   $: if (!running && value && $queue.length) {
              ^
64:     $queue.shift()();
65:   }
[!] Error: Unexpected token (Note that you need @rollup/plugin-json to import JSON files)
node_modules/axios/package.json (2:8)
1: {
2:   "name": "axios",
           ^
3:   "version": "0.21.4",
4:   "description": "Promise based HTTP client for the browser and node.js",
Error: Unexpected token (Note that you need @rollup/plugin-json to import JSON files)
    at error (/mnt/volume_nyc1_01/svelte-express-mongoDB-Node/mesn-fe/node_modules/rollup/dist/shared/rollup.js:5305:30)
    at Module.error (/mnt/volume_nyc1_01/svelte-express-mongoDB-Node/mesn-fe/node_modules/rollup/dist/shared/rollup.js:9750:16)
    at Module.tryParse (/mnt/volume_nyc1_01/svelte-express-mongoDB-Node/mesn-fe/node_modules/rollup/dist/shared/rollup.js:10156:25)
    at Module.setSource (/mnt/volume_nyc1_01/svelte-express-mongoDB-Node/mesn-fe/node_modules/rollup/dist/shared/rollup.js:10057:24)
    at ModuleLoader.addModuleSource (/mnt/volume_nyc1_01/svelte-express-mongoDB-Node/mesn-fe/node_modules/rollup/dist/shared/rollup.js:18402:20)
    at ModuleLoader.fetchModule (/mnt/volume_nyc1_01/svelte-express-mongoDB-Node/mesn-fe/node_modules/rollup/dist/shared/rollup.js:18458:9)
    at async Promise.all (index 0)
    at ModuleLoader.fetchStaticDependencies (/mnt/volume_nyc1_01/svelte-express-mongoDB-Node/mesn-fe/node_modules/rollup/dist/shared/rollup.js:18484:34)
    at async Promise.all (index 0)
    at ModuleLoader.fetchModule (/mnt/volume_nyc1_01/svelte-express-mongoDB-Node/mesn-fe/node_modules/rollup/dist/shared/rollup.js:18460:9)
```

## Views

### SignUp

![SignUp](https://user-images.githubusercontent.com/67696829/103473397-f5742f80-4d65-11eb-8df3-f8809447bc46.png)

### SignIn

![SignIn](https://user-images.githubusercontent.com/67696829/103473416-294f5500-4d66-11eb-8bea-e3280bf2c0cd.png)

### Products

![Products](https://user-images.githubusercontent.com/67696829/103473536-b0e99380-4d67-11eb-81a9-15f491a94704.png)

### Make an order

![making-order](https://user-images.githubusercontent.com/67696829/103473571-30776280-4d68-11eb-8ede-119dd2fe5589.png)

### Orders

![order](https://user-images.githubusercontent.com/67696829/103473656-fe1a3500-4d68-11eb-99e8-6062d616ab7f.png)

### Order details

![order-details](https://user-images.githubusercontent.com/67696829/103473676-3883d200-4d69-11eb-8ffe-3a536a017f51.png)
