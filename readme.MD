# Create react components for NPM

###Step 1

Start an npm package:

```
npm start
```

### Step 2

Create the following folders in the main project folder:

```
build up
source
Test
```

### Step 3

Install the following packages as development dependencies:

```
npm i -D rollup rollup-plugin-copy rollup-plugin-terser @rollup/plugin-babel @babel/cli @babel/core @babel/preset-env @babel/preset-react
```

### Step 4

Create a react application inside the test folder:

```
Try npx create-react-app
```

### Step 5

Create your component in the src folder and then we will proceed to link it with the react application created inside the **test** folder to be able to see the correct development of the component.

```javascript
import React from "react";

const MyComponent = () => {
    return <>This es my component</>;
};

export default MyComponent;
```

### Step 6

Link your component with the react application that is in the test folder. Note that if you install any packages in the test react app, you will have to go through the linking process again.

To link the component in the root folder we add the component to the global scope:

```
npm link
```

Then we enter the test folder and link it

```
cd test
npm link component-name
```

Note that the **_component_name_** is the name that the component has in the **package.json**

### Step 7

In a terminal window in the root folder of the component, run the webpack watch script, so that as we modify the component, it is updated in the **build** folder.

```
npm start
```

In another terminal window, in the **test** folder, run the react app and add your component to **src/App.js** to start editing it.

```
cd test
npm start
```

### Step 8

Once the component is finished, we can publish it to npm. Please note that you must correctly configure both the **package.json** as well as the .gitignore and .npmignore files.
