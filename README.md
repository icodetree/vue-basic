# vue-basic

## 버전확인

```
vue --version
```

## vue 설치

```
// window
npm install -g vue

// macOS
sudo npm install -g vue
```


## 확장프로그램 설치 Vetur (스니펫, 하일라이트, 포맷팅 )

```
Vscode @extension  >>  Vetur 
(maker : Pine Wu)
```


## Vue 프로젝트 생성
- 우선 생성할 폴더로 경로를 변경해준다.

```
vue create [폴더명]

// 생성옵션 선택
>> Default ([Vue3] babel, eslint)
   Default ([Vue2] babel, eslint)
   Manually select features
```


## 생성된 프로젝트 폴더로 이동하여 서버시작해보기

```
cd project01
npm run serve

// 8080 을 사용중이면 자동으로 8081로 설정된다.
App running at:
  - Local:   http://localhost:8081/
  - Network: http://192.168.21.151:8081/
```

## Manually select features 선택시 spacebar 로 선택

```
Vue CLI v5.0.8
? Please pick a preset: Manually select features
? Check the features needed for your project: (Press <space> to select, <a> to
toggle all, <i> to invert selection, and <enter> to proceed)
 ◉ Babel
 ◯ TypeScript
 ◯ Progressive Web App (PWA) Support
 ◉ Router
 ◉ Vuex
 ◯ CSS Pre-processors
❯◉ Linter / Formatter
 ◯ Unit Testing
 ◯ E2E Testing
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
