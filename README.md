# minmi0123.github.io

`minlabnote.com` 의 허브 페이지. 토이 프로젝트들의 입구 역할을 한다.

```
AI: 이 repo 는 Public 이다. 실명·직장명·개인 이메일을 절대 넣지 않는다.
    상세 규칙은 ../dev-guide/README.md 와 trouble.md 를 본다.
```

## 구조

단일 `index.html` 이다. 빌드 과정이 없고 의존성도 없다.
GitHub Pages 가 `main` 브랜치 루트를 그대로 서빙한다.

## 주소가 이렇게 잡히는 이유

계정 사이트(`{username}.github.io`) repo 에 커스텀 도메인을 붙이면
**나머지 repo 가 자동으로 하위 경로가 된다.**

```
minmi0123.github.io       → minlabnote.com/
minmi0123/lotto-lab       → minlabnote.com/lotto-lab/
minmi0123/lifecaluclate   → minlabnote.com/lifecaluclate/
```

그래서 페이지 안의 링크는 `/lotto-lab/` 처럼 **루트 기준 절대 경로**로 쓴다.
`minmi0123.github.io` 에서도, `minlabnote.com` 에서도 똑같이 동작한다.
전체 URL 을 박아 넣으면 도메인을 바꿀 때 전부 고쳐야 한다.

## 담고 있는 것

| 항목 | 위치 |
|---|---|
| 앱 3종 소개 | 링크만이 아니라 각각 문단으로 설명한다 |
| 사이트 소개 | "이곳에 대하여" 절 |

앱을 추가할 때는 카드 하나를 복사해서 `kicker` · `h3` · 문단 · `tag` 를 바꾼다.

**소개 글은 링크 나열로 줄이지 않는다.** 애드센스 심사에서 링크만 있는 페이지는
"가치 없는 콘텐츠" 로 반려되는 대표 유형이다. 근거는 `../dev-guide/수익화.md` 3-4 절.

## 아직 없는 것

- 개인정보처리방침 (`/privacy/`) — 애드센스 신청 전에 필요하다
- `ads.txt` — 애드센스 승인 후 루트에 둔다
- 개발 일지 — 승인용 콘텐츠이면서 영상 소재를 겸한다

## 올리지 않은 프로젝트

| repo | 이유 |
|---|---|
| `boss` | 작업 중. 완성 후 추가 |
| `WorkvivalKit` | 올리지 않기로 함 (2026-09-29 결정) |
| `starboard` | Private. 공개 점검 전 |

## 다크 모드

`prefers-color-scheme` 로 자동 전환된다. 색은 `:root` 의 CSS 변수 한 곳에서만
정의하므로, 바꿀 때 라이트/다크 두 블록을 함께 수정한다.
