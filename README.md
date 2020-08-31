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
    "paths": {
      "@assets/*": [
        "./src/assets/*"
      ],
      "@components/*": [
        "./src/components/*"
      ],
      "@styles/styles/*": [
        "./src/styles/*"
      ],
      "@layout/*": [
        "./src/layout/*"
      ]
    },
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
