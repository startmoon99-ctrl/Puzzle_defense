# Puzzle Defense Prototype

모바일 세로 화면을 우선한 브라우저 기반 2D 퍼즐 디펜스 프로토타입입니다. 외부 의존성이 없는 정적 웹 앱이라 Windows에서는 브라우저로, iPhone에서는 Safari로 동일한 게임 로직을 실행할 수 있습니다.

## 실행

정적 파일 서버로 프로젝트 폴더를 열어 `index.html`에 접속합니다. 예를 들어 Python이 설치돼 있다면:

```powershell
python -m http.server 4173
```

그런 다음 `http://localhost:4173`을 엽니다.

## 조작

- `PUZZLE DRAW` — 50원으로 조각을 뽑으며, 퍼즐판의 빈 칸을 좌측 상단부터 순서대로 채웁니다.
- 퍼즐 조각 — 배치된 모든 조각이 자동으로 가장 가까운 몬스터를 공격합니다.
- 조각 드래그 후 빈 칸에 놓기 — 이동
- 같은 Tier 조각 위에 놓기 — 다음 Tier로 합치기

## 조정 가능한 데이터

`app.js` 파일 상단의 `GAME_DATA`에서 자원, Tier 공격력/공격 타입, 몬스터, 웨이브 데이터를 한곳에서 변경할 수 있습니다.

## 플랫폼 메모

입력은 Pointer Events로 통합되어 마우스와 터치를 같은 로직으로 처리합니다. CSS의 `viewport-fit=cover`, safe-area inset, 반응형 grid를 적용했고, 특정 플랫폼 API는 게임 로직에 사용하지 않았습니다. iOS 앱으로 배포할 때는 이 정적 앱을 Capacitor 등의 WebView 컨테이너로 감싸면 됩니다.

## iPhone 화면 보정

좁은 iPhone 화면에서 퍼즐판과 뽑기 버튼이 가로로 넘치지 않도록 반응형 폭과 safe viewport 기준을 적용했습니다.
