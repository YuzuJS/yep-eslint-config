# Installation
* Make sure you have [eslint installed](https://github.com/eslint/eslint).
* Install the latest @yuzu/yep-eslint-config.
* In your top level package.json add the following under 'scripts':
    `"lint": "eslint -c ./node_modules/@yuzu/yep-eslint-config/.eslintrc ."`
* Call `npm run lint` from the command line to run.

# ESLint React Rules Currently On:
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
