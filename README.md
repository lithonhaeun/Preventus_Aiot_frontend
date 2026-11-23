# Aiot_frontend · 순찰 로봇 관제 대시보드

Preventus 대시보드 프론트. 화면 3개: 종합 화면(index) · 로봇 상태(robot) · 지도 상세(map)

## 폴더
| 위치 | 내용 |
|---|---|
| `index.html` `robot.html` `map.html` | 화면 3개 |
| `css/common.css` | 세 화면 공통 스타일 |
| `css/<화면>.css` · `js/<화면>.js` | 화면별 스타일 · 그리기 |
| `js/api.js` | 데이터 받아오기 (여기만 고치면 가짜 ↔ 실제 전환) |
| `mock/` | 백엔드 설계서 부록 A 표 모양 그대로 만든 가짜 JSON |
| `assets/` | 아이콘 · 그림 |

## 실행
- 파이참: 오른쪽 위 실행 구성 **로컬 서버 (5500)** ▶ → http://localhost:5500
- 터미널: `python3 -m http.server 5500`

`fetch`로 mock JSON을 읽기 때문에 HTML 파일을 더블클릭(file://)으로 열면 데이터가 안 보임. 꼭 서버로 열 것

## 백엔드 연결 (나중에)
1. 백엔드(preventus_backend) 받기
2. `js/api.js`에서 `USE_MOCK = false`
3. 실제 데이터: `ssh -N -L 8000:127.0.0.1:8000 hci-72` 후 백엔드 `/api/dashboard/*` 사용

## 참고 문서
- 화면 설계서 × DB 테이블 (item_id 표)
- Preventus 백엔드 설계서 v0.4 (3.3 조회 주소, 부록 A 표 정의)
- Figma: Dashboard (XsaA3beyb3J6eejkEdVVQ3)
