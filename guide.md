Guide for discord.js  
==
##### 모든 것은, VSC(Visual Studio Code) 에디터를 기반으로 작성하였음.


### **1. 세팅**  
---
>> 1. [Node.js](https://nodejs.org, "Go NodeJs") 를 깔아준다.  
```
Node.js 공홈에 방문하도록 한다.
```

>> 2. 원하는 위치에 폴더 하나를 생성하여, 폴더를 VSC로 연다. (단 폴더명이 되도록이면 한글이 되지 않도록 한다.)  
```
Recommend : discordjs
Not Recommend : 디코봇
```
>> 3. CMD나 VSC내장 Terminal을 열어준다. 여기서 cmd를 사용한다면, 콘솔 명령어(cd 등)을 입력해주어서 파일에 접근할 수 있도록 한다.  
```
Windows Cmd : cd [폴더명]
Mac : 동일하다.
```
>> 4. npm init -y (yarn을 사용한다면, yarn init -y 를 입력해준다.)를 cmd에 입력해주어서, 파일 안에 pakage.json 등의 파일이 생성되는 지 확인한다. 
```
???:\[File Name]>이 cmd에 표시되는지 확인하자.

npm : npm init -y
yarn : yarn init -y
```
>> 5. npm install discord.js 혹은 yarn add discord.js를 실행하여, 디스코드 봇 모듈을 다운 받아준다.
>>> 시간이 좀 걸린다. ~~그래봤자 최대 3분이다;;~~
```
npm : npm install discord.js
yarn : yarn add discord.js
```
>> 6. 모듈을 다운 받았으면, linter를 세팅해주자.
```
npm : npm install --save-dev eslint
yarn : yarn add eslint --dev
```
>> 7. ESLint 룰을 설정해주자.
>>> 새로운 파일을 하나 생성하자.
```
.eslintrc.json
```
>>> 다음으로 표시되는 코드를 입력하자.
```json
{ 
	"extends": "eslint:recommended",
	"env": {
		"node": true,
		"es6": true
	},
	"parserOptions": {
		"ecmaVersion": 2021
	},
	"rules": {
        
	}
}
```
>>> 그리고 "rules"라는 곳에 아무것도 없는 것을 확인했다면, 중괄호 사이에 다음 코드를 삽입하도록한다.
``` json
    "arrow-spacing": ["warn", { "before": true, "after": true }],
	"brace-style": ["error", "stroustrup", { "allowSingleLine": true }],
	"comma-dangle": ["error", "always-multiline"],
	"comma-spacing": "error",
	"comma-style": "error",
	"curly": ["error", "multi-line", "consistent"],
	"dot-location": ["error", "property"],
	"handle-callback-err": "off",
	"indent": ["error", "tab"],
	"keyword-spacing": "error",
	"max-nested-callbacks": ["error", { "max": 4 }],
	"max-statements-per-line": ["error", { "max": 2 }],
	"no-console": "off",
	"no-empty-function": "error",
	"no-floating-decimal": "error",
	"no-inline-comments": "error",
	"no-lonely-if": "error",
	"no-multi-spaces": "error",
	"no-multiple-empty-lines": ["error", { "max": 2, "maxEOF": 1, "maxBOF": 0 }],
	"no-shadow": ["error", { "allow": ["err", "resolve", "reject"] }],
	"no-trailing-spaces": ["error"],
	"no-var": "error",
	"object-curly-spacing": ["error", "always"],
	"prefer-const": "error",
	"quotes": ["error", "single"],
	"semi": ["error", "always"],
	"space-before-blocks": "error",
	"space-before-function-paren": ["error", {
		"anonymous": "never",
		"named": "never",
		"asyncArrow": "always"
	}],
	"space-in-parens": "error",
	"space-infix-ops": "error",
	"space-unary-ops": "error",
	"spaced-comment": "error",
	"yoda": "error"
```