# FrontEnd
FrontEnd 정리

## 🐫 ESLint / Prettier 설정

>경로: /root/.eslintrc.js

```javascript
  rules: {
    "no-console": "off,

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
