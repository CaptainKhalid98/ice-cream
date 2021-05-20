vv@@ -1,15 +1,16 @@
# Ice Cream Builder - React JS Starter Application
A basic template that consists of the essential elements that are required to start building a React application using [create-react-app](https://github.com/facebook/create-react-app).
## Table of contents
- [Installation](#installation)
  - [Node JS](#node-js)
  - [Create React App](#create-react-app)
- [Editor setup](#editor-setup)
  - [Plugins](#plugins)
  - [Settings](#settings)
  - [Set Line Breaks](#set-line-breaks)
- [Linting & Auto Formatting setup](#linting-and-auto-formatting-setup)

## Installation
@@ -97,6 +98,12 @@ I would also recommend below settings for VS Code. You can edit the VS Code sett
}
```

### Set Line Breaks

Make sure in your VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed). To do that, just click LF/CRLF in bottom right corner of editor, click it and change it to "LF". If you dont do that, you will get errors in my setup.

<img src="public/line-feed.jpg" alt="Line Feed" width="700">

## Linting and auto Formatting Setup

- Open terminal and cd into the project directory
- enter below command
```bash
npx install-peerdeps --dev eslint-config-airbnb@18.1.0
```
- when the above one finishes, enter the below command
```bash
npm install prettier eslint-config-prettier eslint-plugin-prettier
```
- create 2 new files inside the project root folder called '.eslintrc' and '.eslintignore'
- write below lines inside .eslintignore file
```txt
src/serviceWorker.js
src/setupTests.js
public/*
```
- write below lines inside .eslintrc file
```txt
{
    "extends": [
        "react-app",
        "airbnb",
        "airbnb/hooks",
        "eslint:recommended",
        "plugin:jsx-a11y/recommended",
        "prettier",
        "prettier/react"
    ],
    "plugins": [
        "jsx-a11y",
        "prettier"
    ],
    "rules": {
        "no-console": "off",
        "react/state-in-constructor": "off",
        "react/prop-types": "off",
        "jsx-a11y/click-events-have-key-events": "off",
        "react/jsx-filename-extension": [
            1,
            {
                "extensions": [
                    ".js",
                    ".jsx"
                ]
            }
        ],
        "prettier/prettier": [
            "error",
            {
                "trailingComma": "es5",
                "singleQuote": true,
                "printWidth": 100,
                "tabWidth": 4,
                "semi": true
            }
        ]
    }
}
```

whats up khalid
