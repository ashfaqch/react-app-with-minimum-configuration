# react-app-with-minimum-configuration

In this example I have demonstrated that how to Create a react app with minimum configuration required.

## Steps:

## Create a new folder for the react app:

_Run following commands._

-   `mkdir react-app`
-   `cd react-app`
-   `npm init` (_npm init will ask you a bunch of questions. Just press enter for the defaults._)

## Install dependencies:

_Run following commands._

-   `npm install --save react`
-   `npm install --save react-dom`
-   `npm install --save typescript`
-   `npm install --save-dev @babel/preset-react`
-   `npm install --save-dev @babel/preset-env`
-   `npm install --save-dev parcel-bundler`

## Create .babelrc file:

_Create the .babelrc file. This file tells parcel that we are using ES6 and React._

```
{
    "presets": [
        "@babel/preset-react"
    ]
}
```

## Create tsconfig.json file:

_Create the tsconfig.json file. To define compiler options._

```
{
    "compilerOptions": {
        "jsx": "react"
    }
}
```

## Create index.tsx file:

_Create startup react component._

```
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';

ReactDOM.render(
	<>
		<h1>React App</h1>
		<p>With minimum configuration using Parcel and Typescript.</p>
	</>,
	document.getElementById('root')
);
```

## Create index.html file:

_Copy following code to index.html file._

```
<!DOCTYPE html>
<html>

<head>
    <title>React App</title>
</head>

<body>
    <div id="root"></div>
    <script src="./index.tsx"></script>
</body>

</html>
```

## Create index.css file:

_Copy following code to index.css file._

```
body {
    background-color: #282c34;
    color: #ffffff;
    text-align: center;
}
```

## Add a script entry to package.json scripts:

```
"start": "parcel index.html"
```

## Build & Run

1. Run `npm install` to install packages
2. Run `npm start` and navigate to `http://localhost:1234/` to view app.
