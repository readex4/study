# YEOBOYA Javascript Fullstack Orientation



## 소개
* (주)여보야 스마트사업부 웹개발자 교육을 위한 OT입니다.
* OT를 통해 과거부터 현재까지의 웹흐름을 알아보고 Javascript Fullstack에 대한 커리큘럼 계획들을 확인합니다.

## 웹흐름 핵심 키워드
<details><summary>SSR (Server Side Rendering)</summary>
  <p>
    
  * `db` + `SSR(php,jsp,asp)` + `script` + `css`
    
    * 과거부터 현재까지 많은 웹사이트들은 페이지를 이동할 때마다 서버에 페이지에 대한 요청을 하는 방식을 사용
    * 서버에서 렌더링을 마치고, Data가 결합된 HTML파일을 내려주는 방식
    * 페이지를 이동할 때마다 서버에 요청하여 페이지를 받아야 하기 때문에, 받아오는 시간동안 깜빡거리는 현상이 나타남
      
  </p>  
</details>   
<details><summary>jQuery [Ajax]</summary>
  <p>
    
  * `db` + `SSR(php,jsp,asp)` + `jQuery` + `css`
    * Write Less, Do More (적게 작성하고, 많은 것을 하자)
    * 웹사이트에 JavaScript를 쉽게 활용할 수 있도록 도와주는 Javascript Library
   
  * `Ajax`
    * Asynchronous Javascript And XML
    * XML에 기반으로 하여 서버와의 통신을 비동기 방식으로 연결함으로써 시스템 자원의 불필요한 시간낭비를 줄이고, JS 대화형 웹 Application을 구현한 기술
    
  </p>
</details>

<details><summary>SPA (Single Page Application)</summary>
  <p>

  * `db` + `SSR(php,jsp,asp)` + `Vue` or `React` + `css`
    * 하나의 웹페이지로만 이루어진 사이트
    * 기본적으로는 `CSR` 목표
    * 장점
      * 사용자 친화적
      * 초기 렌더링 후 데이터만 받아오기 때문에, 상대적으로 서버 요청이 적음
      * Virtual Dom
      * 프론트 엔드와 백엔드 분리로 개발업무 분업화 및 협업이 용이
      * 개발이 상대적으로 효율적
    * 단점
      * 첫페이지 로딩속도가 느리다.
      * 첫페이지 로딩속도가 느리다..
      * 첫페이지 로딩속도가 느리다... 
      * `SEO` 문제  
    * SPA의 단점들을 해결위한 방법
      * 첫페이지는 SSR로 처리
      * 각 컨텐츠별로 라우팅되는 페이지를 SSR로 처리    
    
    <details><summary>CSR</summary>
      <p>

      * Client Side Rendering
      * 최초 요청시 HTML, CSS, Javascript 등 각종 리소스를 받아온다. 
      * 이후에는 서버에 데이터만 요청하고, Javascript로 뷰를 컨트롤 한다.
      * 초기 요청 때 SSR 보다 많은 리소스를 요청하기 때문에, 렌더링은 속도는 SSR이 더 빠르다.
      * 하지만 이후 다른 페이지로의 이동시에는 SSR 보다 빠른 페이지 전환 속도와 더 나은 사용자 경험을 제공한다.   
        
      </p>
    </details>       
    <details><summary>SEO</summary>
      <p>

      * Search Engine Optimization
      * CSR방식으로는 검색엔진에서 검색이 불가능 (구글제외)   
      </p>
    </details>       
    <details><summary>Vue.js</summary>
      <p>

      * 웹 개발을 단순화하고 정리하기 위해 개발된 Javascript Frontend Framework
      * 기존 웹개발자들을 위한 느낌이 강하다.
      * 점진적으로 채택 가능한 구조를 갖추고 있다.
      * 선언형 렌더링과 컴포넌트 구성에 초점을 두고 있다.
      * Single File Component
        
        웹의 뷰(view)를 구성하는 요소인 HTML, CSS, JavaScript 코드를 .vue 확장자를 가진 하나의 파일에 모두 정의하는 방식
        
        관리의 생산성을 높이고, 협업을 수월하게 한다는 장점
      * Html 기반 Template 구문
        
        개발한 프론트엔드 파일을 사용자가 볼 수 있도록 브라우저 화면에 렌더링하는 과정에 Template이란 문법을 사용
        
        이 Template을 구성하는 문법이 Html 기반으로 이뤄져 있어 배우기 쉽다.
      </p>
    </details>       
    <details><summary>React.js</summary>
      <p>

      * 웹 개발을 단순화하고 정리하기 위해 개발된 Javascript Frontend Framework
      * JSX 기반 Component
        
        JSX 코드로 Component를 작성하고 Component의 상태(State)를 변화시키지 않고 관리
        
        변화가 일어나면 Virtual DOM에 렌더링을 하고 기존의 DOM과 비교하여 변화가 일어난 곳만 업데이트
      </p>
    </details>       
    <details><summary>Vue.js 와 React.js 공통점</summary>
      <p>

      * 웹 UI를 작은 Component 단위로 구성 
        
        Component는 다른 프로젝트에서도 재사용할 수 있고, 컴포넌트 캡슐화와 확장이 가능해 개발이 유연해지는 장점이 있다.
      * Virtual DOM 방식을 통해 성능을 향상
        
        Virtual DOM은 실제 DOM 변화를 최소화 시켜주는 역할

        브라우저는 HTML 파일을 스크린에 보여주기 위해 DOM 노드 트리 생성 -> 렌더트리 생성 -> 레이아웃 -> 페인팅 과정을 통해 표현
        
        DOM 노드는 HTML의 각 엘리먼트와 연관되어 있기 때문에 HTML 파일에 30개의 변화가 생기면 DOM 노드가 변경되고 그 이후의 과정역시 30회 반복됨
        
        작은 변화에도 매우 복잡한 과정들이 다시 실행되기 때문에 DOM 변화가 잦을 경우 성능이 저하
        
        Virtual DOM은 뷰에 변화가 있다면, 그 변화가 실제 DOM에 적용되기 전에 Virtual DOM에 적용시키고 최종 결과만 실제 DOM에 전달
        
        따라서 30개의 변화가 있다면 Virtual DOM은 변화된 부분만 가려내어 실제 DOM에 전달하고 실제 DOM은 그 변화를 1회로 인식하여 단 한번의 렌더링 과정만 진행
      </p>
    </details>       
 
  </p>
</details>
<details><summary>Node.js</summary>
  <p>
    
  * Backend를 제어하고 처리가 가능한 Javascript Framework
  * 세션서버 또는 패킷서버등 다른용도로도 사용이 가능
  * 웹뿐만 아니라 IoT서비스같은 인베디드 시스템에도 이용이 
  * 장점
    * 비동기처리방식으로 결과값을 기다리지 않고 보다 다양한 요청을 처리할 수 있다.
    * 이벤트 루프를 기반으로하여 급격한 부하의 증가도 견딜 수 있다.
    * 대량의 요청을 동시에 효율적으로 처리 할 수 있다.
    * `Node.js`를 기반으로 한 다양한 라이브러리들이 존재  (`Express`, `Prettier`, `ESLint` 등등)
    * `npm` or `yarn`을 이용한 의존성 처리 및 관리의 용의
    <br>
    <details><summary>Express.js</summary>
      <p>
        
      * Node.js의 대표적인 웹서버 Framework
      </p>
    </details>    
    <details><summary>Prettier.js</summary>
      <p>
        
      * 코드 편집기에 직접 설치할 수있는 뛰어난 코드 포맷터
      * 협업시 모든 개발자가 동일한 코딩스타일을 만들도록 해준다.
      </p>
    </details>    
    <details><summary>ESLint.js</summary>
      <p>
        
      * 존재하지 않거나 사용되지 않는 변수, 이중 선언, 잘못된 코드 구성, 구문 오류 체크해준다.
      * AirBnb와 같은 기존 개발 스타일을 사용하거나 자신만의 규칙을 지정할 수 있다.
      </p>
    </details>    
    <details><summary>Npm</summary>
      <p>

      * Node Packaged Manager
      * Node.js에서 사용하는 패키지 관리자 툴
      * 온라인 데이터베이스로 이루어져 있으며 클라이언트를 통해 접근
      </p>
    </details>    
    <details><summary>Yarn</summary>
      <p>

      * FaceBook에서 개발한 자바스크립트의 새로운 패키지 매니저
      * npm보다 더욱 빠르게 패키지를 인스톨하는 방법과 의존성 관리를 다양한 디바이스에서 일관성 있게 할 수 있다.
      </p>
    </details>

  </p>
</details>

<details><summary>Javascript Fullstack</summary>
  <p>
    
  * `db` + `Nuxt` or `Next` + `css`  
  * `db` + `Express` + `Nuxt` or `Next` + `css`    
    
    * SSR with Hydration 기법
    * middleware 기능을 통한 `api`를 통해 `CRUD`를 처리
    * 장점  
      * Javascript로 Frontend를 넘어서 Backend까지 하나의 언어로 처리가능
    <br>
    <details><summary>Nuxt.js</summary>
      <p>
        
      * Vue.js 베이스에 SSR처리기술을 더한 Framework
      * Vue 파일 쓰기 (*.vue)
      * 정적 파일 전송
      * ES6/ES7 지원
      * JS & CSS 코드 번들링 및 압축
      * <head> 요소 관리 (title, meta, 기타)
      * 모듈식 아키텍처 확장
      </p>
    </details> 
    <details><summary>Next.js</summary>
      <p>

      * React.js 베이스에 SSR처리기술을 더한 Framework
      * Single File Components
      * Global CSS
      * Typescript 지원
      </p>
    </details> 
    <details><summary>Nuxt.js 와 Next.js 공통점</summary>
      <p>

      * Hot Reload (저장시 자동 새로고침)
      * Automatic Routing (pages 폴더에 있는 파일은 자동으로 라우팅)
      * SPA(SSR) 단점을 극복하여 페이지 별로 소스코드가 존재
      * Code Splitting (코드 분할)
      </p>
    </details> 
    <details><summary>API</summary>
      <p>

      * Application Programming Interface
      * SPA에서 `CRUD`를 처리하고 제공
      </p>
    </details> 
    <details><summary>CRUD</summary>
      <p>

      * Create(생성), Read(읽기), Update(갱신), Delete(삭제)    
      </p>
    </details> 

  </p>
</details>

## Why?
<details><summary></summary>
  <p>
    
  * 시간과 비용 절약
  * 인력운용의 효율성
  * 안정적이고 검증된 기술
  * Frontend, Backend 모두 사용가능
  </p>
</details>



## Javascript Fullstack WebDeveloper Skill
<details><summary></summary>
  <p>
    
  * ECMAScript
  * Node.js
  * Express.js or Koa.js
  * Vue.js or React.js
  * Nuxt.js or Next.js
  * Component Design Patterns
  * Type Checking (Typescript + Jsdoc)
  * Unit Test
  </p>
</details>
    
## Javascript Fullstack Curriculum Sequence
<details><summary></summary>
  <p>
    
  * [형상관리 시스템](./Quest00/README.md)
  * [HTML과 웹의 기초](./Quest01/README.md)
  * CSS의 기초와 응용
  * 자바스크립트와 DOM
  * OOP (Object-Oriented Programming) 객체지향프로그래밍
  * 인터넷의 이해
  * Node.js의 기초
  * 웹 API의 기초: REST와 CRUD
  * 서버와 클라이언트의 통신
  * 인증의 이해
  * RDB의 기초와 연결
  * 보안의 기초
  * 정적 분석: 타입스크립트와 린트 시스템
  * 자동화된 테스트
  * 컴포넌트 기반 개발
  * 번들링과 빌드 시스템
  * 배포 파이프라인
  * 서비스의 운영: 로깅과 모니터링
  * Vue.js
  * Nuxt.js
  * Express.js
  </p>
</details>    
