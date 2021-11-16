# PbiTest

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.0.2.

## Eslint, prettier setup

```
ng add @angular-eslint/schematics@next
npm install --save-dev --save-exact prettier
npm install --save-dev eslint-config-prettier
```

### Update `.eslintrc.json`

```
"plugins": ["prettier"]
```

```
"rules": {
  "prettier/prettier": "error"
},
```

Overrides:

https://github.com/angular-eslint/angular-eslint#notes-for-eslint-plugin-prettier-users

```
// NOTE: WE ARE NOT APPLYING PRETTIER IN THIS OVERRIDE, ONLY @ANGULAR-ESLINT/TEMPLATE
{
  "files": ["*.html"],
  "extends": ["plugin:@angular-eslint/template/recommended"],
  "rules": {}
},
// NOTE: WE ARE NOT APPLYING @ANGULAR-ESLINT/TEMPLATE IN THIS OVERRIDE, ONLY PRETTIER
{
  "files": ["*.html"],
  "excludedFiles": ["*inline-template-*.component.html"],
  "extends": ["plugin:prettier/recommended"],
  "rules": {
    // NOTE: WE ARE OVERRIDING THE DEFAULT CONFIG TO ALWAYS SET THE PARSER TO ANGULAR (SEE BELOW)
    "prettier/prettier": ["error", { "parser": "angular" }]
  }
}
```

## Css, icons, fonts

Just update index.html

```
<link
  href="//code.ionicframework.com/ionicons/2.0.1/css/ionicons.min.css"
  rel="stylesheet"
  type="text/css"
/>
<link
  href="//fonts.googleapis.com/css?family=Titillium+Web:700|Source+Serif+Pro:400,700|Merriweather+Sans:400,700|Source+Sans+Pro:400,300,600,700,300italic,400italic,600italic,700italic"
  rel="stylesheet"
  type="text/css"
/>

<link rel="stylesheet" href="//demo.productionready.io/main.css" />
```
