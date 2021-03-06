## eslint 的规范
> 这个是自定义的eslint用的规范
---
## 使用
```bash
npm install --save-dev eslint-config-ro
```
## 然后在你自己的eslint的配置文件上引入
```javascript
"extends": [
    "ro"
]
```
---
## 依赖
```javascript
"dependencies": {
    "babel-eslint": "^10.0.1",
    "eslint": "^7.1.0",
    "eslint-plugin-react": "^7.20.0"
  }
```
---
## 完整的规则如下
```javascript
{
    "parser": "babel-eslint",
    "env": {
        "node": true,
        "es6": true,
        "browser": true
    },
    "extends": [
        "eslint:recommended",
        "plugin:react/recommended"
    ],
    "parserOptions": {
        "ecmaFeatures": {
            "jsx": true
        },
        "ecmaVersion": 11,
        "sourceType": "module"
    },
    "plugins": [
        "react"
    ],
    "rules": {
        "react/prop-types": "off",
        "react/no-typos": "error",
        "no-console": "off",
        "no-prototype-builtins": "off",
        "semi": ["error", "never"],
        "indent": [ "error", 2 ],
        "quotes": ["error", "single"],
        "block-spacing": "error",
        "space-before-blocks": "error",
        "object-curly-spacing": ["error", "always"],
        "no-duplicate-imports": "error",
        "no-var": "error",
        "require-await": "error", // 禁止使用不带 await 表达式的 async 函数
        "computed-property-spacing": "error",
        "lines-between-class-members": "error", // 强制类成员之间出现空 s
        "key-spacing": "error", // 强制在对象字面量的属性中键和值之间使用一致的间距 s
        "no-nested-ternary": "error", // 禁用嵌套的三元表达式
        "no-multiple-empty-lines": ["error", { "max": 1, "maxBOF": 1 }], // 禁止出现多行空行 s max 1行 文件末尾1行 s
        "space-before-function-paren": "error", // 强制在 function的左括号之前使用一致的空格 s
        "arrow-spacing": "error", // 强制箭头函数的箭头前后使用一致的空格 s
        "rest-spread-spacing": "error", // 强制剩余和扩展运算符及其表达式之间有空格 s
        "no-unneeded-ternary": "error", // 禁止可以在有更简单的可替代的表达式时使用三元操作符 s
        "eqeqeq": "error", // 要求使用 === 和 !==
        "space-infix-ops": "error", // 要求操作符周围有空格 s
        "switch-colon-spacing": "error", // 强制在 switch 的冒号左右有空格 s
        "no-multi-spaces": "error", // 禁止使用多个空格 s
        "array-bracket-spacing": "error", // 强制数组方括号中使用一致的空格 s
        "comma-spacing": "error", // 强制在逗号后使用一致的空格 s
        "space-unary-ops": "error", // 强制在一元操作符前后使用一致的空格 s
        "eol-last": "error", // 在文件末尾多一行
        "lines-around-comment": ["error", {"beforeLineComment": true}] // 行注释前面需要空行
    }
}
```
## license
MIT
