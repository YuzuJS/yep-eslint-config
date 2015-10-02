## Installation
* Make sure you have [eslint installed](https://github.com/eslint/eslint) as a dev dependency.
* Install the latest @yuzu/yep-eslint-config as a devDependency.
* In your top level package.json add the following under 'scripts':
    `"lint": "eslint -c ./node_modules/@yuzu/yep-eslint-config/.eslintrc ."`
* Call `npm run lint` from the command line to run.

##Troubleshooting
##### Help! I'm getting an error about not having a react plugin or babel plugin installed.
This probably means that something went wrong with npm when installing your peer dependencies. Most likely inside your `node_modules/@yuzu` you have another `node_modules` folder that contains our eslint plugins and our config can't find it. There are two possible ways to fix this.

The first is to delete your `node_modules` folder from your yep-app component and `npm install` again from that component's top level directory to see if NPM can't sort itself out.

If that doesn't work, the alternative is to physically move the plugins to whatever the top most node_modules folder of your application is.

```
@yuzu/my-component
-lib
-node_modules
    -eslint
    -chai
    -@yuzu
        -yep-eslint-config
        -node_modules (this folder shouldn't exist)
            -babel-eslint (move me!)
            -eslint-plugin-react (move me!)
    -(move babel-eslint and eslint-plugin-react to this level)
-index.js
-package.json
```
##### Help! I'm getting an error that says `'eslint' is not recognized as an internal or external command, operable program or batch file. ` but I totally have eslint installed!
This may mean that for some reason you're missing your eslint bin file (potentially because the generator didn't install it properly). To resolve this problem simply type `npm install eslint` in your command line and hit enter and you should be good to go.

## ESLint React Rules Currently On:
* [Enforce boolean attributes notation in JSX](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-boolean-value.md)
* [Curly Spacing](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-curly-spacing.md)
* [Indent Props](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-indent-props.md)
* [No Duplicate Props](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-no-duplicate-props.md)
* [Disallow undeclared variables](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-no-undef.md)
* [Prevent usage of unknown DOM property](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/no-unknown-property.md)
* [Prevent extra closing tags for components without children (self-closing-comp)](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/self-closing-comp.md)
* [Prevent missing parentheses around multiline JSX](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/wrap-multilines.md)
* [Prevent React to be incorrectly marked as unused](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-uses-react.md)
* [Prevent variables used in JSX to be incorrectly marked as unused](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-uses-vars.md )
* [Prevent missing React when using JSX](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/react-in-jsx-scope.md)
