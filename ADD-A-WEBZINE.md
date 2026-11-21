# 새 잡지 추가하기

## 1. 잡지 폴더 만들기

예: `worlds/new-topic/index.html`

이미지나 CSS, JavaScript가 별도 파일이면 같은 `new-topic` 폴더 안에 함께 넣습니다.

## 2. 경로 확인하기

- 좋은 예: `./assets/photo.jpg`, `./style.css`, `./script.js`
- 피할 예: `C:/Users/name/Desktop/photo.jpg`, `/assets/photo.jpg`

컴퓨터 개인 경로나 `/`로 시작하는 사이트 루트 기준 경로는 GitHub Pages의 저장소 하위 주소에서 깨질 수 있습니다.

## 3. 메인 서가에 책 추가하기

최상위 `index.html`의 `.books` 영역에 아래 형태의 링크를 추가합니다. `href`는 실제 잡지의 경로와 정확히 일치해야 합니다.

```html
<a class="book" href="worlds/new-topic/index.html" aria-label="새로운 탐구 주제 잡지 열기">
  <span class="num">NEW ISSUE</span>
  <div class="coverart">📘</div>
  <div class="booktitle">
    새로운 탐구 주제
    <span class="sub">짧은 설명</span>
    <span class="open-label">표지를 눌러 잡지 펼치기 ↗</span>
  </div>
</a>
```

로비 표지는 일반 링크로 각 잡지 페이지를 직접 엽니다. 모달, 공통 JavaScript 또는 로비의 iframe 동작에 의존하지 않습니다.

## 4. 잡지에서 서가로 돌아오는 링크 추가

각 잡지의 메인 `index.html` 상단에 다음 링크를 추가합니다.

```html
<a href="../../index.html">← 서가</a>
```

`worlds/<잡지-id>/index.html`에서 최상위 로비로 돌아가는 상대 경로입니다.

## 5. 업로드 전 확인

1. ZIP 압축을 풀었을 때 `index.html`이 프로젝트 최상위에 있는지 확인합니다.
2. CSS·JavaScript·이미지 파일이 빠지지 않았는지 확인합니다.
3. 로비에서 각 표지를 눌러 해당 잡지로 이동하는지 확인합니다.
4. 각 잡지의 `← 서가` 링크가 로비로 돌아가는지 확인합니다.
5. 퀴즈·버튼·내부 목차와 모바일 화면을 확인합니다.
6. GitHub 저장소 최상위에 프로젝트 파일을 업로드합니다.


## 현재 추가된 지구 곡률 기사

`worlds/earth-curvature/index.html`에 있습니다. 내부의 서가 링크는 `../../index.html`을 사용합니다.
