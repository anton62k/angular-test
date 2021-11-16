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
