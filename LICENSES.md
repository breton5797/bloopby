# BLOOPBY 라이선스·출처

기록일: 2026-11-18 / 대상: `games/bloopby/build/` (웹판 1.0.0)

## 폰트

| 파일 | 폰트 | 라이선스 | 출처 | 게임/앱 임베딩 |
|---|---|---|---|---|
| `build/fonts/Pretendard-ExtraBold.woff2` | Pretendard ExtraBold (한글·라틴·가나) | SIL Open Font License 1.1 | https://github.com/orioncactus/pretendard / npm `pretendard@1.3.9` | 허용 (OFL: 소프트웨어에 번들·임베딩·재배포 가능, 폰트 단독 판매 금지) |
| `build/fonts/PretendardJP-ExtraBold.woff2` | Pretendard JP ExtraBold (일본어 한자 포함) | SIL Open Font License 1.1 | https://github.com/orioncactus/pretendard / npm `pretendard-jp@1.3.9` | 허용 (위와 같음) |

- 라이선스 원문: `build/fonts/OFL-Pretendard.txt` (Copyright (c) 2021, Kil Hyung-jin, Reserved Font Name Pretendard). 배포물에 원문을 함께 둔다.
- 예약 글꼴 이름(RFN) 조건: 원본 woff2를 수정하지 않고 그대로 쓴다. 서브셋 등으로 수정하면 "Pretendard" 이름을 쓸 수 없다.
- 중국어(간체): OFL Pretendard SC가 없어 시스템 글꼴(PingFang SC, Noto Sans CJK SC, Microsoft YaHei)로 표시한다. 별도 폰트 파일을 배포하지 않는다.
- 이전 빌드의 Google Fonts Jua `<link>`는 삭제했다(외부 폰트 요청 없음).

## 이미지

22개 이미지(`build/*.png`, `*.jpg`, `*.webp`)는 모두 **Higgsfield로 제작** (대표님 확인 2026-11-18). 프롬프트·생성일은 기록이 없다. 파일 목록은 `assets/SOURCES.md`.

## 사운드

외부 음원 파일 없음. 효과음·배경음은 코드(Web Audio 합성)로 만든다.

## 코드·외부 요청

- 서드파티 라이브러리·코드 없음 (단일 `index.html`, 외부 `<script>`·`<link>` 없음).
- `build/index.html`의 외부 URL 점검(2026-11-18, `grep -E "https?://"`): 1건 — `SHARE_URL` 상수 `https://claude.ai/artifact/P5xeVmoydKiKt3TEdnT4kC` (공유 버튼이 클립보드에 복사하는 문구용, 네트워크 요청 아님).
- `build/privacy.html`: 방침 본문에 링크 2건(https://www.anthropic.com/legal/privacy, https://policies.google.com/privacy). 사용자가 누를 때만 열리며 페이지 로드 시 외부 요청 없음.
- 웹판은 claude.ai 아티팩트 런타임(`window.claude`)의 db·user 기능을 쓴다(플랫폼 제공 기능, 별도 코드 번들 없음).
