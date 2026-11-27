# eq-grab 인수인계 로그

## 2026-11-27 16:04 — 자료조사·PRD v0.2·저장소 생성 (코드는 아직 없음)

**지금 상태**: 문서만 있음. `docs/PRD.md`(v0.2) 결정 사항은 아래와 같고, 구현 코드는 없음.
- 동그란 2색 캡슐을 집어 열면 질문 쪽지가 나옴. 꽝 없음.
- 레퍼런스(기아 Lucky Grab)와 같은 구조: Three.js 3D 유리 기계 + Rapier 물리 + Firebase RTDB + 가로 폰 패드(십자키 + GRAB). 앱 느낌은 색·글꼴·캐릭터·말투로만 입힘.
- 저장소: `woojun-choi/eq-grab` (공개).

**남은 일**:
1. PRD 9장 1주차 — `screen.html`에 집 모양 유리 기계 + Rapier 캡슐 더미 + 키보드 조작 + 집기·출구
2. `play.html`(가로 패드) ↔ 큰 화면 연결 — Firebase RTDB `grab/{room}/` (Firebase 프로젝트 `eungdap-770f5`에 RTDB 켜야 함, 권한은 방장 issean99)
3. 질문 54개 선정 (응답하라 저장소 `자료/새 질문2.xlsx`, 기준은 PRD 5-5) → `questions.json`
4. 캡슐 열기 연출(SC-05/PH-05), Flow 에셋(PRD 8장), 진행자 화면

**하면 안 되는 일**:
- GitHub `yeon51422777-maker/lucky-grab`(비공식 재현판)의 코드·이미지·소리 복사 금지 — 라이선스 없음. 구조만 참고(큰 화면이 상태 주인, 폰은 `{dir, grab}` 입력만, `runTransaction`으로 자리 잡기, `onDisconnect`).
- 재현판을 그대로 실행하면 원작자의 실제 Firebase(`teacher-letter-48131`)에 씀 → 돌려 볼 땐 Firebase import 주소를 끊고 키보드 모드로만.
- 응답하라 저장소의 `전시_질문뽑기/시안/`(편지 봉투 2D/3D 시안)은 폐기됨. 봉투 모양으로 되돌리지 말 것 — 사용자가 "동그랗게, 열면 질문" 으로 바꿈.
- 비밀 키는 커밋하지 않기 (Firebase 웹 apiKey는 공개용이라 괜찮음).

**검증 방법**: 아직 실행할 코드 없음. 문서 확인은 `docs/PRD.md` 10장 "정해야 할 것"(전시 날짜·화면 방향, 실물 보상, 앱 연결 범위, 동시 인원)이 아직 미정인지 사용자에게 먼저 물어볼 것.

**참고**:
- `docs/PRD.md` — 요구사항 전부 (특히 5장 기능, 6장 앱 느낌 표, 7장 기술, 8장 Flow 에셋 프롬프트)
- `docs/기획.md` — 레퍼런스 조사: 아이엠파인 작품 페이지(2024·2025 Lucky Grab, 2026 Lucky Pinball), 재현판 구조 분석
- 앱 디자인 키트: 응답하라 저장소(issean99/eungdap) `app/design_ref/v0.11/Kit_Colors.html`, `Kit_Messenger.html`, 글꼴 `app/assets/fonts/`
- 응답하라 저장소 쪽 작업은 브랜치 `claude/exhibition-claw-machine-project-93be06`에 커밋 안 된 채로 남아 있음 (`전시_질문뽑기/` PRD·기획·폐기된 시안, `.claude/launch.json`)
