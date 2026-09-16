# 단야구 (Dan-baseball)

2026 KBO 구단으로 즐기는 단순 야구 게임입니다.

## 플레이 링크

| 배포 | URL |
|------|-----|
| **Firebase Hosting** (권장) | https://dan-baseball.web.app |
| GitHub Pages | https://amaddaofficial.github.io/Dan-baseball/ |

Firebase 프로젝트 ID를 알면 `https://<프로젝트ID>.web.app` 주소로 바로 접속할 수 있습니다.

## Firebase 배포 설정 (한 번만)

1. [Firebase Console](https://console.firebase.google.com/) → 프로젝트 선택 → **Hosting** → **Get started** (Hosting 활성화)
2. GitHub 저장소에 Secrets 추가: [Settings → Secrets](https://github.com/amaddaofficial/Dan-baseball/settings/secrets/actions)
   - `FIREBASE_SERVICE_ACCOUNT` — 서비스 계정 JSON 전체 내용
3. `main`에 push하면 [Actions](https://github.com/amaddaofficial/Dan-baseball/actions)에서 자동 배포

### 서비스 계정 만들기

1. [Google Cloud IAM](https://console.cloud.google.com/iam-admin/serviceaccounts) → Firebase 프로젝트 선택
2. **Create service account** → 역할: **Firebase Hosting Admin**
3. JSON 키 다운로드 → GitHub Secret `FIREBASE_SERVICE_ACCOUNT`에 붙여넣기

## GitHub Pages 배포 (선택)

> 처음 한 번: [Settings → Pages](https://github.com/amaddaofficial/Dan-baseball/settings/pages)에서 **Source**를 **GitHub Actions**로 선택

## 업데이트 방법

1. `public/index.html` 수정
2. `main` 브랜치에 push
3. Firebase / GitHub Pages가 자동으로 다시 배포 (약 1~2분)

## 로컬 테스트

```bash
python3 -m http.server 8080 --directory public
```

브라우저에서 http://localhost:8080 으로 접속

## 저장소 구조

- `public/index.html` — 게임 전체 (HTML/CSS/JS 단일 파일)
- `firebase.json` — Firebase Hosting 설정
- `.github/workflows/firebase-hosting.yml` — Firebase 자동 배포
- `.github/workflows/pages.yml` — GitHub Pages 자동 배포
