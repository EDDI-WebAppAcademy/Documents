## vue 환경 구성

일단 Vue나 React나 Svelte 같은 최신 기능들은 대부분 ECMA 6 스펙을 따름  
구닥다리로 쓰지 말고 최신형으로 씁시다.  

### nodejs 설치

```make
중간에 뭐가 나올때 그냥 대충 휙휙 넘기거나 끄면 안됩니다.
컴퓨터 포맷해야 하는 최악의 사태가 발생할 수 있습니다.

작업 진행중 중간에 나타나는 에러 메시지를 잘 확인해야 합니다.
에러 메시지에 보면 Packages requiring reboot: <<<----
패키지가 재부팅을 요구합니다 <<< 라는 뜻 ㄷㄷㄷ

https://www.microsoft.com/ko-kr/download/details.aspx?id=48145

1. https://nodejs.org/ko/download/ 에서 자신의 운영체제에 맞게 다운로드한다.
2. 실행
3. Next
4. 라이센스 동의 후 Next
5. Next
6. Next
7. Next
8. nodejs 일부 패키지에 C/C++ 기능이 필요한 것들이 있음
   묻지도 따지지도 말고 그냥 필요하면 다 설치하라고 체크하고 Next
9. Install
10. 설치가 꽤 오래 걸릴 수도 있으니 커피나 한 잔 하면 좋다.
11. node -v 로 nodejs 설치 여부를 체크한다.
12. npm --version 으로 npm 설치 여부를 체크한다.
```

### Vue.js 설치

```make
1. npm install -g @vue/cli
2. 오류나면 npm audit fix
3. MAC에선 권한(permission) 없다고 하면 관리자 모드로 sudo 줘서 실행한다.
```

### vue 프로젝트 생성

```make
1. 적당한 위치를 잡는다(HTML/CSS, JavaScript에선 javascript 폴더로 잡음)
2. vue create frontend
   frontend라는 이름으로 프로젝트가 만들어짐
3.  옵션 설정을 해야함

? Please pick a preset:
  Default ([Vue 2] babel, eslint)
  Default (Vue 3) ([Vue 3] babel, eslint)
> Manually select features

? Check the features needed for your project:
 (*) Choose Vue version
 (*) Babel
 ( ) TypeScript
 ( ) Progressive Web App (PWA) Support
 (*) Router
>(*) Vuex
 ( ) CSS Pre-processors
 (*) Linter / Formatter
 ( ) Unit Testing
 ( ) E2E Testing
 
? Choose a version of Vue.js that you want to start the project with 2.x

? Use history mode for router? (Requires proper server setup for index fallback in production) Yes

? Pick a linter / formatter config: (Use arrow keys)
> ESLint with error prevention only
  ESLint + Airbnb config
  ESLint + Standard config
  ESLint + Prettier
  
? Pick additional lint features: (Press <space> to select, <a> to toggle all, <i> to invert selection)
>(*) Lint on save
 ( ) Lint and fix on commit
 
? Where do you prefer placing config for Babel, ESLint, etc.?
  In dedicated config files
> In package.json

? 다음 질문엔 그냥 앤터치면 된다.

그럼 뭔가 프로젝트 설정하기 위해 많은 작업이 일어난다.
```

### vue 프로젝트 구동

```make
cd frontend
npm run serve
```

## materialize 설정

```make
npm install materialize-css@next --save-dev
npm install material-design-icons --save-dev
```

## Vuetify

```make
vue add vuetify
```

## CoverFlow

```make
npm add vue-coverflow
```

## Vue Awesome Swiper

```make
npm install vue-awesome-swiper --save-dev

// 버그나는 경우(버전을 낮춰서 활용)
npm install swiper@5.3.7 --save-dev
```

## Vue Img LightBox

```make
npm install @morioh/v-lightbox --save-dev
```

## 부속 라이브러리

```make
npm install axios --save-dev

npm install materialize-css@next --save-dev
npm install material-design-icons --save-dev

vue add vuetify

<------------------ Vuetify 설치도중 메시지 시작 --------------------->
 WARN  There are uncommitted changes in the current repository, it's recommended to commit or stash them first.
? Still proceed? Yes

📦  Installing vue-cli-plugin-vuetify...

+ vue-cli-plugin-vuetify@2.4.7
updated 1 package and audited 1343 packages in 5.869s

94 packages are looking for funding
  run `npm fund` for details

found 17 vulnerabilities (2 low, 11 moderate, 4 high)
  run `npm audit fix` to fix them, or `npm audit` for details
✔  Successfully installed plugin: vue-cli-plugin-vuetify

? Choose a preset: Default (recommended)

🚀  Invoking generator for vue-cli-plugin-vuetify...
📦  Installing additional dependencies...

added 14 packages from 9 contributors and audited 1357 packages in 6.511s

98 packages are looking for funding
  run `npm fund` for details

found 17 vulnerabilities (2 low, 11 moderate, 4 high)
  run `npm audit fix` to fix them, or `npm audit` for details
⚓  Running completion hooks...

✔  Successfully invoked generator for plugin: vue-cli-plugin-vuetify
 vuetify  Discord community: https://community.vuetifyjs.com
 vuetify  Github: https://github.com/vuetifyjs/vuetify
 vuetify  Support Vuetify: https://github.com/sponsors/johnleider
 <------------------ Vuetify 설치도중 메시지 종료 --------------------->
 
npm add vue-coverflow
npm install vue-awesome-swiper --save-dev
npm install swiper@5.3.7 --save-dev
 
npm install @mdi/font --save-dev

npm install --save vue-cookies --save-dev
```
