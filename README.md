# eq-grab — 응답하라 질문 뽑기

[응답하라](https://eungdap-770f5.web.app) 전시 부스용 체험물.
큰 화면에 동그란 캡슐이 가득 든 뽑기 기계를 띄우고, 관람객은 QR로 자기 폰을 게임 패드로 써서 캡슐 하나를 집습니다.
캡슐을 열면 **오늘 저녁 가족에게 물어볼 질문**이 들어 있어요.

- 기획·요구사항: [docs/PRD.md](docs/PRD.md)
- 자료조사(레퍼런스: 기아 Lucky Grab, 아이엠파인): [docs/기획.md](docs/기획.md)

## 구성 (예정)

| 파일 | 하는 일 |
| --- | --- |
| `screen.html` | 큰 화면 — Three.js 3D 기계 + Rapier 물리, 게임 상태의 주인 |
| `play.html` | 관람객 폰 — 가로 패드(십자키 + GRAB), 캡슐 열기, 질문 카드 |
| `admin.html` | 진행자 — 대기열, 질문 켜고 끄기, 통계 |
| `questions.json` | 전시용 질문 (응답하라 질문 중 말로 바로 답할 수 있는 것) |
| `assets/` | Google Flow로 만든 그림·텍스처 (PRD 8장) |

실시간 연결은 Firebase Realtime Database(`grab/{room}/`), 배포는 Firebase Hosting.
