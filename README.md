# Raw Node.js Project Setup Guide Info

## Node Version Check
Ensure you have Node.js installed. You can check the version using:
```sh
node -v
```

---

## New Project Setup using npm

### 1. Initialize the Project
```sh
mkdir raw-node-api-project
cd raw-node-api-project
npm init -y
```

### 2. Install Dependencies
```sh
npm install dotenv
npm install --save-dev nodemon
npm install react  # Install if needed
```

### 3. Install ESLint & Prettier for Code Formatting
```sh
npm install --save-dev eslint prettier
npm install --save-dev eslint-config-airbnb-base eslint-plugin-import
npm install --save-dev eslint-config-prettier eslint-plugin-prettier
```

### 4. Update package.json
Manually edit `package.json` and update the scripts:
```json
"scripts": {
  "start": "node index.js",
  "dev": "nodemon index.js",
  "test": "echo \"Error: no test specified\" && exit 1"
},
"keywords": ["node", "api", "server", "raw-node"],
"author": "Your Name <your.email@example.com>",
"description": "A simple raw Node.js API project"
```

### 5. Create `.eslintrc.json` and add the following configuration:
```json
{
  "extends": ["prettier", "airbnb-base"],
  "parserOptions": {
    "ecmaVersion": 12
  },
  "env": {
    "commonjs": true,
    "node": true
  },
  "rules": {
    "no-console": 0,
    "indent": 0,
    "linebreak-style": 0,
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
  },
  "plugins": ["prettier"]
}
```

### 6. Create `index.js`

### 7. Run the Project
```sh
npm run dev
```

---

## New Project Setup using yarn

### 1. Initialize the Project
```sh
mkdir raw-node-api-project
cd raw-node-api-project
yarn init -y
```

### 2. Install Dependencies
```sh
yarn add dotenv
yarn add --dev nodemon
yarn add react  # Install if needed
```

### 3. Install ESLint & Prettier for Code Formatting
```sh
yarn add -D eslint prettier
yarn add -D eslint-config-airbnb-base eslint-plugin-import
yarn add -D eslint-config-prettier eslint-plugin-prettier
```

### 4. Update `package.json`
```sh
yarn set-script start "node index.js"
yarn set-script dev "nodemon index.js"
yarn set-script test "echo \"Error: no test specified\" && exit 1"

yarn config set description "A simple raw Node.js API project"
yarn config set author "Your Name <your.email@example.com>"
yarn config set keywords "node, api, server, raw-node"
```

### 5. Create `.eslintrc.json` and add the following configuration:
```json
{
  "extends": ["prettier", "airbnb-base"],
  "parserOptions": {
    "ecmaVersion": 12
  },
  "env": {
    "commonjs": true,
    "node": true
  },
  "rules": {
    "no-console": 0,
    "indent": 0,
    "linebreak-style": 0,
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
  },
  "plugins": ["prettier"]
}
```

### 6. Create `index.js`

### 7. Run the Project
```sh
yarn dev
```

