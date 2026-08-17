# Puzzle Defense

모바일 세로 화면을 우선한 브라우저 기반 2D 퍼즐 디펜스 프로토타입입니다.

## 현재 기능

- 5 x 5 퍼즐 보드
- 퍼즐 드로우 시 빈 칸을 좌측 상단부터 오른쪽 방향으로 순차 배치
- 퍼즐 조각 자동 공격
- 같은 등급 조각 드래그 합성
- Tier 1 ~ 6 공격 방식 차별화
- 웨이브 기반 몬스터
- 몬스터 처치 보상
- 플레이어 HP / GAME OVER
- PC 마우스 및 iPhone 터치 대응
- PWA manifest / service worker 포함

## GitHub Pages

이 저장소를 GitHub Pages로 배포하면 PC와 iPhone Safari에서 같은 주소로 플레이할 수 있습니다.

GitHub 저장소에서:

`Settings` → `Pages` → `Deploy from a branch` → `main` → `/ (root)` → `Save`

배포가 완료되면 생성된 GitHub Pages 주소로 접속하세요.

## 파일

- `index.html` — 게임 화면
- `app.js` — 게임 로직
- `styles.css` — 화면 및 게임 스타일
- `manifest.webmanifest` — 홈 화면 추가용 웹앱 정보
- `sw.js` — 캐시 / 오프라인 실행 기반
