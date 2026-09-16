# 단야구 (Dan-baseball)

2026 KBO 구단으로 즐기는 단순 야구 게임입니다.

## 플레이

**https://amaddaofficial.github.io/Dan-baseball/**

> 처음 한 번만: [Settings → Pages](https://github.com/amaddaofficial/Dan-baseball/settings/pages)에서 **Source**를 **GitHub Actions**로 선택해 주세요. 이후 `main`에 push할 때마다 자동 배포됩니다.

## 업데이트 방법

1. `index.html` 파일을 수정합니다.
2. `main` 브랜치에 push하면 GitHub Actions가 자동으로 사이트를 다시 배포합니다.
3. 배포가 끝나면(약 1~2분) 같은 링크에서 업데이트된 게임을 플레이할 수 있습니다.

## 로컬에서 테스트

브라우저에서 `index.html`을 열거나, 간단한 로컬 서버로 확인할 수 있습니다.

```bash
python3 -m http.server 8080
```

브라우저에서 http://localhost:8080 으로 접속하세요.

## 저장소 구조

- `index.html` — 게임 전체 (HTML/CSS/JS 단일 파일)
- `.github/workflows/pages.yml` — GitHub Pages 자동 배포 설정
