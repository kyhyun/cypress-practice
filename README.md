# cypress-practice

간단한 기능에 E2E Test를 적용하여 사용법을 익혀보자.

## 테스트를 수행할 기능

[js-counter]()
[js-calculator]()

### Cypress CLI Tools 실행 방법

1. 라이브러리 설치

```sh
# 프로젝트 경로로 이동 후 package.json 파일에 dev dependency 추가

# npm
npm install cypress --save-dev // npm i -D cypress

# yarn
yarn add cypress --dev
```

- [cypress 공식 문서](https://www.cypress.io/) 참조
- 시스템적인 요구사항도 있으니 자세한 사항은 공식 문서를 보고 참고한다. ( 매번 바뀌니 수시로 확인 필요 )

2. cypress 실행

```sh
# project root에서 다음 커맨드를 수행
npx cypress open

# yarn
yarn run cypress open

# The long way with the full path
./node_modules/.bin/cypress open

# with the shortcut using npm bin
$(npm bin)/cypress open
```

- 매번 실행할 때, 해당 커맨드의 작성에 불편함이 느껴진다면 `package.json`에서 스크립트 필드에 cypress 실행 명령을 추가하는 것이 편하다.

```json
{
  "scripts": {
    "cypress:open": "cypress open"
  }
}
```

- 이와 같이 project root에 커맨드를 추가해준다.

```sh
npm run cypress:open
```

- 이후에는 스크립트에 작성한 커맨드를 통해 실행할 수 있게 된다.

3. CLI tools

- Cypress를 실행하면 테스팅을 할 수 있도록 GUI의 실행화면이 제공되고, 해당 인터페이스를 통해서 테스트 타입(E2E, Component)을 정하고, 설정과 실행할 브라우저를 선택할 수 있다.
- 이후 테스트 작성 방법은 공식문서를 통해 자주 사용하는 명령어는 익히고, 잘 잊어 먹는 부분은 기록해두고 수시로 보는 시간을 들여서 숙지하는 방식으로 학습하면 된다.
