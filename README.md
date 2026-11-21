# SCIENCE WORLD · GitHub Pages 통합본

이 프로젝트는 빌드 도구나 패키지 설치 없이 GitHub Pages에서 바로 게시할 수 있는 정적 웹사이트입니다.

## 현재 서가 구성 (총 5권)

- `worlds/cactus/` — 선인장은 전자파를 먹을까?
- `worlds/plant-voice/` — 식물은 칭찬을 알아들을까?
- `worlds/acid-rain/` — 산성비 맞으면 대머리 될까?
- `worlds/glass/` — 유리의 구조와 새로운 활용 (두 편을 한 권으로 통합)
- `worlds/earth-curvature/` — 산에 올라가면 지구가 둥근 게 보일까?
  - `part-01/` — 유리의 구조와 온도 변화
  - `part-02/` — 비결정성 고체의 활용과 차세대 안경

## GitHub에 올리는 방법

1. ZIP 파일을 컴퓨터에 다운로드한 뒤 압축을 풉니다.
2. GitHub 저장소를 열고 `Add file` → `Upload files`를 선택합니다.
3. **압축을 푼 폴더 안의 파일과 폴더를 저장소 최상위에 업로드**합니다. `index.html`이 저장소 최상위에서 바로 보여야 합니다.
4. `Commit changes`를 누릅니다.
5. 저장소 `Settings` → `Pages`에서 `Deploy from a branch`, `main`, `/(root)`를 선택하고 저장합니다.
6. Pages 화면에 표시되는 HTTPS 주소로 접속합니다.

## 경로와 통합 원칙

- 메인 페이지는 저장소 최상위 `index.html`입니다.
- 각 잡지는 `worlds/<magazine-id>/index.html`에서 독립적으로 열립니다.
- 유리 잡지는 한 개의 표지/칸을 사용하며, 내부에서 1부와 2부를 탭으로 전환합니다.
- 메인 페이지와 유리 통합 페이지는 **상대 경로**를 사용하므로 GitHub Pages의 저장소 하위 경로에서도 동작하도록 구성했습니다.
- 로비의 표지는 각 잡지의 상대 경로로 직접 연결됩니다. 각 잡지는 독립 페이지로 열리며, 별도 iframe 팝업이나 추가 JavaScript 동작에 의존하지 않습니다. 유리 잡지만 두 편의 기사를 내부 화면에서 전환합니다.
- 새 잡지에는 `worlds/<새-id>/index.html`을 만들고, 메인 `index.html`에 표지 버튼을 추가하면 됩니다.

## 친구들이 제출할 때

가장 좋은 제출 방식은 `index.html`, CSS, JavaScript, 이미지 등 **실행에 필요한 모든 파일을 ZIP 하나로 묶는 것**입니다. 메인 HTML 파일 이름은 `index.html`로 통일하고, 파일 경로는 `./assets/image.png`처럼 상대 경로로 작성해야 합니다. 컴퓨터 개인 경로(`C:/Users/...`)나 사이트 루트 기준 절대 경로(`/images/...`)는 피해주세요.

## 기술 점검 메모

- 네 잡지는 정적 HTML 페이지로 구성되어 별도 빌드가 필요하지 않습니다.
- 로비의 각 표지는 해당 잡지의 HTML 페이지로 직접 이동하는 일반 링크입니다. 각 잡지는 서로 독립된 폴더에서 열리므로 CSS와 JavaScript가 서로 간섭하지 않습니다.
- 식물·산성비 잡지는 Google Fonts를 사용합니다. 인터넷 연결이 없으면 기기 기본 글꼴로 표시될 수 있지만 본문과 기능은 계속 사용할 수 있습니다.
- 일부 외부 글꼴을 제외하면 이미지와 인터랙션은 각 HTML 파일 안에 포함되어 있습니다.
- GitHub 저장소와 Pages 사이트는 공개 설정일 수 있습니다. 개인 정보는 올리지 마세요.


## 이번 최종 추가 기사

- 지구 곡률 기사는 `worlds/earth-curvature/index.html`에 독립적으로 배치했습니다. 기사 내부의 `../../index.html` 링크는 이 폴더 구조에서 최상위 서가로 돌아갑니다.
GitHub Pages deployment refresh
