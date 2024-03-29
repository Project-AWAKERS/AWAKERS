# AWAKERS

## Vue.js 개발환경 설정 
1. 해당 리포지토리 .zip파일 다운
2. zip파일 바탕화면에 압축 해제
3. VScode에서 해당 폴더로 이동
4. `npm install`
5. `npm run dev`로 프로젝트 실행<br>

## 중요 명령어
- `npm run dev` : 개발자 모드로 실행
- `Ctrl + c` : `Y`입력시 작업 중지<br>

## GitHub 협업 하는 방법!!! (매우 중요!!!)
### `Feature-Branch` 전략 사용
- `Feature-Branch` 전략이란?
  -> `Main Branch`, `Develop Branch`, `Feature Branch` 이 세개의 브랜치를 사용하여 여러 팀원이 동시에 다양한 작업을 진행할 수 있으며, 변경 사항을 체계적으로 통합할 수 있게 해주는 방식
- `Main Branch` : 배포 브랜치 (실제 구동되고 있는 서비스, 직접적인 push 절대 불가)
- `Develop Branch` : 개발 용 브랜치
- `Feature Branch` : 개별 기능개발 용 브랜치 (`Develop` 브랜치에 PR한 이 후 삭제)

### 서로 다른 두 원격 저장소 병합하는 방법 
해당 블로그 참조 : https://velog.io/@www_1216/%EC%84%9C%EB%A1%9C-%EB%8B%A4%EB%A5%B8-%EB%91%90-%EC%9B%90%EA%B2%A9-%EC%A0%80%EC%9E%A5%EC%86%8C-%EB%B3%91%ED%95%A9%ED%95%98%EA%B8%B0
   1. 커밋 로그를 병합하기 위해 병합할 원격 저장소를 <병합할 저장소 이름>으로 추가
      - `git remote add <병합할 저장소 이름> <병합할 저장소 주소>`
      - ex) `git remote add pre https://github.com/... .../` *pre: 병합할 저장소 이름
   2. 원격 저장소에 저장된 커밋 기록들을 가져온다. (병합은 아직 하지 않는다.)
      - `git fetch <병합할 저장소 이름>`
      - ex) `git fetch pre` *pre: 병합할 저장소 이름
   3. 연관이 없는 기록들을 병합한다.
      - `git merge --allow-unrelated-hisotires <병합할 저장소 이름>/<병합하고 싶은 branch 이름>`
      - ex) `git merge --allow-unrelated-histories pre/master` *pre: 병합할 저장소 이름 master: 병합하고 싶은 branch 이름
   4. 병합이 완료되었으므로 병합된 원격 저장소 지운다.
      - `git remote remove <병합할 저장소 이름>`
      - ex) `git remote remove pre`
   5. 병합 완료된 로그를 커밋한다.
      - `git commit -m "커밋메시지"`

<br>

## Visual Studio Code Extensions
### 개발환경 단일화 관련
- `Vetur`
- `ES7 React snippets`
- `ESLint`
- `VSCode Great Icons`
- `Prettier-Code formatter`
- `IntelliCode`
- `HTML CSS Support` : HTML 요소의 class에서 css 선택자 요소를 쓸 때 자동 완성 기능 지원해주는 익스텐션
- `HTML to CSS autocompletion` : CSS에서 코딩할 때 HTML에서 사용한 속성이름을 자동 완성해주는 기능 지원해주는 익스텐션
- `Auto Rename Tag` : 태그 이름을 수정할 때, <>여는 태그와 </>닫는 태그를 동시에 수정하게 해주는 익스텐션
- `Auto Close Tag` : 태그를 작성할 때 여는 태그만 입력하면 닫는 태그가 자동으로 작성이 되게 하는 익스텐션
- `Highlight Matching Tag` : 쌍이 되는 태그를 표시해 주는 익스텐션
- `HTML End Tag Labels` : 마지막 닫는 태그에 클래스명을 주석처리로 표시하여 이 태그가 어느 역할을 하는 태그인지 알 수 있게 해주는 익스텐션
- `HTMLHing` : html 코딩할 때 알맞지 않은 문법이나 빠진 부분이 있으면 ide처럼 알려주는 익스텐션
- `image preview` : 이미지의 프리뷰를 볼 수 있게 하는 익스텐션
- `HTML Auto Completion` : 태그 구성 자동 완성 익스텐션
    1. !html 치고 엔터
    2. !table 치고 엔터
    3. !form 치고 엔터
- `Stylelint` : css 구문 오류를 잡아주게 도와주는 익스텐션
- `vscode-styled-components` : css문법 표현 자동완성 기능 제공하는 익스텐션
### GitHub 협업 관련
- `Gitmoji` : 깃에서 커밋 시 이모지를 사용할 수 있게 해주는 익스텐션
