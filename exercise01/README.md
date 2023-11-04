# Exercise 1

## 📌 Result

![alt result1](/exercise01/public/result1.png)

## 📌 개발환경 세팅

### ✔️ 빌드도구 : Vite

- 정의
  - 전체 어플리케이션을 빌드하지 않고 모듈 단위로 필요한 부분만 즉시 컴파일 가능한 빌드 도구
  - 빌트인 CSS 및 CSS 전처리기 지원
  - [공식 문서 페이지](https://vitejs.dev/guide/)

<br/>

- 설치 과정

  1. Vite 설치

     ```
     npm create vite@latest
     ```

  2. 프로젝트 환경 구성 및 개발 서버 실행

     ```
     cd [프로젝트 폴더명]  // #1 단계에서 생성한 프로젝트 폴더명
     npm install
     npm run dev
     ```

  > <br/>
  > ✅<code>npm run dev</code><br/>
  > - 개발 세션을 시작할 때 실행(개발 서버 생성 -> 코드의 변경사항을 실시간으로 반영)<br/>
  > - 단, vite.config.js나 .env 파일과 같은 환경 설정에 변경사항이 있으면 명령어를 재실행하여 서버를 재시작
  > <br/><br/>
  > ✅ <code>npm run build</code><br/>
  > - 코드가 압축되면서 불필요한 코드가 제거 및 최적화 <br/>
  > - 번들링<br/>
  > - 정적 파일(dist/, build/등) 생성 및 환경 변수 설정<br/><br/>

<br/>

### ✔️ 개발 환경 설정 파일

- <strong>node_modules</strong>

  - 프로젝트에 필요한 모든 외부 라이브러리와 모듈을 포함하는 폴더
  - `npm install` 실행 시, package.json 파일에 정의된 모든 의존성(dependencies)들이 설치되는 폴더
  - 직접 설정하지 않음
    <br/>

- <strong>package.json</strong>

  - 프로젝트의 메타데이터와 필요한 의존성 목록을 정의하는 파일
  - scripts 섹션에 사용자 정의(커스텀) 스크립트 명령어 정의 가능
  - 개발자 수동 편집이 가능

        {
          ...
          "scripts": {
            "dev": "vite",
            "build": "vite build",
            "preview": "vite preview"
          },
          "devDependencies": {
            "vite": "^4.4.5"
          }
        }

    <br/>

- <strong>package-lock.json</strong>

  - 프로젝트에서 사용하는 모든 패키지의 버전과 함께 의존성 트리를 정확하게 기록
    (즉, 이를 통해 동일한 패키지 설치를 다른 환경/다른 개발자의 컴퓨터에서 재현 가능)
  - 프로젝트가 의존하는 모든 패키지와 하위 의존성을 잠금(lock)하여 일관성 보장
  - 일반적으로 개발자가 수동으로 편집하지 않음
  - `npm install` 또는 `npm update`명령어 실행시 자동 생성 및 업데이트

<br/>

- <strong>vite.config.js</strong>

  - Vite 프로젝트의 구성파일로, 프로젝트가 어떻게 빌드되고 서버에 제공될지를 결정
  - 예: 플러그인 설정, 빌드 옵션 지정등

<br/>

- <strong>dist/</strong>

  - 최종적으로 프로덕션 환경에 배포될 정적 파일들을 포함하는 폴더
  - `npm run build` 실행시 자동 생성

<br/>

✅정리
|명령어|해당 명령어가 실행 후, 생성되는 파일|
|--|--|
|`npm create vite@latest`|프로젝트의 메타데이터와 의존성이 정의된 package.json, <br/> 프로젝트 빌드 및 개발 서버 옵션을 구성하기 위한 Vite 구성파일인 vite.config.js|
|`npm install`|(package.json에 정의된 의존성을 기반으로 필요한 패키지 설치 후)<br/>node_modules, pacakge-lock.json|
|`npm run build`|(프로젝트 빌드 후)<br/>최적화된 정적 자원들이 dist/, build/등과 같은 폴더에 생성됨|

<br/>

## 📌 CSS Study Review

- (Grid item안에 아무리 내용의 양이 적어도) 최소한 100px, 최대 자동(auto)으로 세로 길이가 늘어나도록 처리
  `grid-template-rows : repeat(3, minmax(100px, auto))`
  <br/>

- auto-fill / auto-fit 차이
  - `auto-fill` : 셀의 수가 초기 설정보다 모자라면, 빈 자리는 공간이 빈 상태 그대로 존재 <br/>
    `grid-template-columns: repeat(auto-fill, minmax(20%, auto))`
  - `auto-fit` : 셀의 수가 초기 설정보다 모자라면, 빈 자리는 나머지 셀이 차지 <br/>
    `grid-template-columns: repeat(auto-fit, minmax(20%, auto))`

<br/>

## 📌 References

- Education Courses App @Andrew Sereda <br/>
  https://dribbble.com/shots/19526780-Education-Courses-App
