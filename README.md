# 할 일 앱 만들기

## 리액트 프로젝트 세팅

- npm으로 설치 한 경우 yarn add 대신에 npm i
- `npx create-react-app ./`
- `yarn create react-app ./`
- `yarn add normalize.css`
- `yarn add sass`
- `yarn add classnames react-icons`

## ESLint, prettier 설정

- ./.prettierrc.json 폴더 만든 후 아래 내용 붙여넣기

```json
{
  "singleQuote": false,
  "semi": true,
  "useTabs": false,
  "tabWidth": 2,
  "trailingComma": "all",
  "printWidth": 80,
  "arrowParens": "avoid",
  "endOfLine": "auto"
}
```

- `yarn add eslint --dev`
- `yarn eslint --init` 모두 yes, 마지막만 yarn으로 설정

- ESLint와 Prettier 연결하여 ESLint 설정
- `yarn add eslint-config-prettier --save-dev`

- ./.eslintrc.js 내용 수정 prettieer 추가

```js
    "extends": [
        "eslint:recommended",
        "plugin:react/recommended",
        "prettier"
    ],
```

```js
    rules: {
    "react/react-in-jsx-scope": "off",
    "react/prop-types": "off",
    "no-unused-vars": "off",
    },
```
## index.css 수정
```css
    * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    outline-style: none;
    }
    ul,
    li {
    list-style: none;
    }
    a {
    color: #000000;
    text-decoration: none;
    }
    img {
    vertical-align: middle;
    border: 0;
    }
    html {
    font-size: 16px;
    }
    body {
    font-family: "Pretendard-Regular", sans-serif;
    font-size: 1rem;
    line-height: 1.25;
    letter-spacing: -0.23px;
    word-break: keep-all;
    color: #000000;
    }
```