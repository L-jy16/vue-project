# vue를 이용한 포트폴리오 사이트 만들기

Vue.js는 현대적인 웹 애플리케이션을 만들기 위한 JavaScript 프레임워크 중 하나에요. 사용자 인터페이스를 만들기 위한 라이브러리로, 데이터 바인딩과 컴포넌트 기반 아키텍처를 중심으로 한다고 볼 수 있어요.

데이터 바인딩은 화면에 표시되는 내용과 데이터 모델 간의 동기화를 자동으로 처리해줍니다. 이것은 개발자가 DOM 조작에 직접 신경 쓰지 않고도 애플리케이션의 상태를 쉽게 관리할 수 있게 해줘요.

컴포넌트 기반 아키텍처는 애플리케이션을 작은 독립적인 조각으로 나누어 개발하고 유지보수하기 쉽게 만들어줘요. 각 컴포넌트는 자체적인 상태와 뷰를 갖고 있으며, 이러한 컴포넌트들을 조합하여 전체 애플리케이션을 구성합니다.

Vue.js는 다른 프레임워크나 라이브러리와 쉽게 통합되며, 점진적으로 프로젝트에 도입하기에도 좋아요. 또한 문서가 잘 정리되어 있어 학습이 비교적 쉬운 편입니다.

## 셋팅
1. `npm init vue@latest`
2. 설정 내용
Vue.js - The Progressive JavaScript Framework<br/><br/>

√ Project name: ... vue-project<br/>
√ Add TypeScript? ... <span style="color.#0000FF">No</span> / Yes<br/>
√ Add JSX Support? ... No / <span style="color.#0000FF">Yes</span><br/>
√ Add Vue Router for Single Page Application development? ... No / <span style="color.#0000FF">Yes</span><br/>
√ Add Pinia for state management? ... <span style="color.#0000FF">No</span> / Yes<br/>
√ Add ESLint for code quality? ... No / <span style="color.#0000FF">Yes</span><br/>
√ Add Prettier for code formatting? ... No / <span style="color.#0000FF">Yes</span><br/><br/>

Scaffolding project in C:\Users\line\Desktop\WEBS0106\vue-project...<br/><br/>

Done. Now run:<br/><br/>

  npm install<br/>
  npm run format<br/>
  npm run dev<br/>

3. 해당 폴더로 이동 `cd vue-project`
4. npm 설치 `npm install`
5. npm format `npm run format`
6. 실행하기 `npm run dev`

## 설치
1. gsap 설치 : `npm install gsap`
2. sass 설치 : `npm install sass`
3. lenis 설치 : `npm install @studio-freight/lenis`