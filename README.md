# 🐫 ESLint / Prettier 설정

> 경로: /root/.eslintrc.js

```javascript
  rules: {
    "no-console": "off",

    "prettier/prettier": [
      "error",
      {
        singleQuote: false,
        semi: true,
        useTabs: false,
        tabWidth: 2,
        trailingComma: "all",
        printWidth: 100,
        bracketSpacing: true,
        arrowParens: "avoid",
      },
    ],
  },
```

<br/>

위 설정으로 자동수정 또는 표시가 안될경우, ESLint 버전을 "v5.x" 로 변경

> 경로: /root/package.json

```json
  "eslint": "^5.16.0",
  "eslint-loader": "^3.0.2",
  "eslint-plugin-vue": "^5.2.3",
```



<br/><br/><hr/>


# 🐫 Typescript/ESLint

> 경로: /root/package.json

```javascript
{
  "devDependencies": {
    "@typescript-eslint/eslint-plugin": "^2.26.0",
    "@typescript-eslint/parser": "^2.26.0",
  }
}
```

<br/><br/>


> 경로: /root/.eslintrc.js

```javascript
  module.exports = {
    root: true,
    env: {
      node: true
    },
    extends: [
      "plugin:vue/essential",
      "eslint:recommended",
      "@vue/typescript/recommended",  // 추가
      "@vue/prettier",
      "@vue/prettier/@typescript-eslint"  // 추가
    ],

    // 추가
    plugins: [
      "@typescript-eslint",
    ],

    // 추가
    parserOptions: {
      parser: "@typescript-eslint/parser",
      ecmaVersion: 2020
    },
    
    // 기존
    rules: {
      "no-console": process.env.NODE_ENV === "production" ? "warn" : "off",
      "no-debugger": process.env.NODE_ENV === "production" ? "warn" : "off"
      
      "prettier/prettier": [
        "error",
        {
          singleQuote: false,
          semi: true,
          useTabs: true,
          tabWidth: 2,
          trailingComma: 'all',
          printWidth: 150,
          bracketSpacing: true,
          arrowParens: 'avoid',
        },
      ],
    },
    
    overrides: [
      {
        files: [
          "**/__tests__/*.{j,t}s?(x)",
          "**/tests/unit/**/*.spec.{j,t}s?(x)"
        ],
        env: {
          jest: true
        }
      }
    ]
  };
```
