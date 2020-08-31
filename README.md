### Documentação para iniciar o front-end da aplicação.


#### Iniciondo projeto React com Typescript
~~~bash
npx create-react-app name-project --templete typescript

cd ./name-project

yarn upgrade

or

npm update
~~~


#### Variável de ambiente .env
~~~bash
yarn add dotenv && yarn add -dev @types/dotenv

or

npm install dotenv && npm install --save-dev @types/dotenv
~~~
.env
~~~env
SKIP_PREFLIGHT_CHECK = true
~~~


#### Starting git and commond initial git
~~~bash
git add --all

git commit -m 'commentary'

git push origin master -> já devera ter vinculado seu repositório com git.
~~~


#### .ditorconfig configuration
~~~editorconfig
root = true

[*]
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
end_of_line = lf
~~~


#### Vscode settings.json configuration
settings.json
~~~js
{
  "editor.codeActionsOnSave": {
    "source.fixAll": true,
    "source.fixAll.eslint": true
  }
}
~~~

#### Configurantion Typescript
~~~js
{
  "compilerOptions": {
    "target": "es5",
    "lib": [
      "dom",
      "dom.iterable",
      "esnext"
    ],
    "allowJs": true,
    "skipLibCheck": true,
    "esModuleInterop": true,
    "allowSyntheticDefaultImports": true,
    "strict": false,
    "forceConsistentCasingInFileNames": true,
    "module": "esnext",
    "moduleResolution": "node",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "noEmit": true,
    "jsx": "react",
    "sourceMap": true,
    "outDir": "./build",
    "rootDir": "./src",
    "baseUrl": ".",
    "experimentalDecorators": true,
    "emitDecoratorMetadata": true
  },
  "include": [
    "src"
  ],
  "exclude": [
    "node_modules"
  ]
}

~~~


#### Install Prettier and configuration
~~~bash
yarn add --dev prettier

or

npm install --save-dev prettier
~~~
#### Configuration .prettierrc.js
~~~js
module.exports = {
  semi: true,
  trailingComma: 'all',
  singleQuote: true,
  printWidth: 80,
  tabWidth: 2,
}
~~~


#### Install Eslint and configuration
~~~bash
yarn add --dev eslint

yarn eslint --init

yarn add -D @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint-plugin-prettier eslint-config-prettier eslint-config-react eslint-plugin-react

or

npm install --save-dev eslint

npm run eslint --init

npm install --save-dev @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint-plugin-prettier eslint-config-prettier eslint-config-react eslint-plugin-react
~~~
#### Eslint configuration
~~~js
module.exports = {
module.exports = {
  env: {
    browser: true,
    es6: true,
    node: true,
  },
  extends: [
    'eslint:recommended',
    'plugin:react/recommended',
    'plugin:@typescript-eslint/recommended',
    'plugin:@typescript-eslint/eslint-recommended',
    'plugin:prettier/recommended',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parser: '@typescript-eslint/parser',
  parserOptions: {
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 12,
    sourceType: 'module',
  },
  plugins: ['react', '@typescript-eslint'],
  rules: {},
  settings: {
    react: {
      createClass: 'createReactClass', // Regex for Component Factory to use,
      // default to "createReactClass"
      pragma: 'React', // Pragma to use, default to "React"
      fragment: 'React.Fragment', // Fragment to use, default to "React.Fragment"
      version: 'detect', // React version. "detect" automatically picks the version you have installed.
      // You can also use `16.0`, `16.3`, etc, if you want to override the detected value.
      // default to latest and warns if missing
      // It will default to "detect" in the future
      flowVersion: '0.53', // Flow version
    },
    propWrapperFunctions: [
      // The names of any function used to wrap propTypes, e.g. `forbidExtraProps`. If this isn't set, any propTypes wrapped in a function will be skipped.
      'forbidExtraProps',
      { property: 'freeze', object: 'Object' },
      { property: 'myFavoriteWrapper' },
    ],
    linkComponents: [
      // Components used as alternatives to <a> for linking, eg. <Link to={ url } />
      'Hyperlink',
      { name: 'Link', linkAttribute: 'to' },
    ],
  },
};

~~~
