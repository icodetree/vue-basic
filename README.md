# vue-basic

## basic setup

-   버전확인

```
vue --version
```

-   vue 설치(window)

```
npm install -g vue
```

-   vue 설치(macOS)

```
sudo npm install -g vue
```

> sudo : 일반 사용자가 루트 권한을 임시로 획득하여 특정 명령을 가능하게 하는 명령어

-   vue/cli 설치 (window)

```
install -g @vue/cli

```

-   vue/cli 설치 (macOS)

```
sudo install -g @vue/cli
```

-   확장프로그램 설치 (스니펫, 하일라이트, 포맷팅 )

```
Vscode @extension  >>  Vetur (Pine Wu)
```

-   Vue 프로젝트 생성
    -   우선 생성할 폴더로 경로를 변경해준다.

```
vue create [폴더명]

// 생성옵션 선택
>> Default ([Vue3] babel, eslint)
   Default ([Vue2] babel, eslint)
   Manually select features
```

-   Vue 프로젝트 생성

```
cd project01
npm run serve

// 8080 을 사용중이면 자동으로 8081로 설정된다.
App running at:
  - Local:   http://localhost:8081/
  - Network: http://192.168.21.151:8081/
```

-   Manually select features 선택시 spacebar 로 선택

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

-   원하는 버전 선택

```
Vue CLI v5.0.8
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Router, Vuex, Linter
? Choose a version of Vue.js that you want to start the project with (Use arrow
keys)
❯ 3.x
  2.x

```

-   라우터 이동시 히스토리 모드 사용유무 선택

```
Vue CLI v5.0.8
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Router, Vuex, Linter
? Choose a version of Vue.js that you want to start the project with 3.x
? Use history mode for router? (Requires proper server setup for index fallback
in production) (Y/n) y

```

-   ESLint 선택 + 코딩컨벤션 선택 (standard)

```
? Pick a linter / formatter config:
  ESLint with error prevention only
  ESLint + Airbnb config
❯ ESLint + Standard config
  ESLint + Prettier

```

-   Lint 옵션 실행 시점 선택 (저장키를 누를때마다 체크)

```
? Pick additional lint features: (Press <space> to select, <a> to toggle all,
<i> to invert selection, and <enter> to proceed)
❯◉ Lint on save
 ◯ Lint and fix on commit

```

-   패키지 별도관리 유무 선택

```
? Where do you prefer placing config for Babel, ESLint, etc.?
  In dedicated config files
❯ In package.json

```

-   즐겨찾기 추가 유무 (지금까지 선택된것을 재등록하지 않게 추가)

```
? Save this as a preset for future projects? (y/N) y

```

-   프리셋 이름 등록

```
? Save preset as: vue-projec

```

- chunk-vendors.js  >> 빌드시 외부플러그인 코드가 들어간다.

## Project setup

```
npm install
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
