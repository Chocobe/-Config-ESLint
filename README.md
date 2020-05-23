# FrontEnd
FrontEnd 정리

## 🐫 ESLint / Prettier 설정

>경로: /root/.eslintrc.js

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
