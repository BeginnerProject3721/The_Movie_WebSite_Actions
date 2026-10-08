# The Movie Website — GitHub Actions

Vue와 TMDB API를 사용하는 영화 웹사이트입니다. `main` 브랜치에 push하면 GitHub Actions가 빌드하고 GitHub Pages에 배포합니다.

## 로컬 실행

Node.js 24.12 이상인 24.x 버전에서 실행하세요.

```bash
npm ci
npm run dev
```

영화 데이터를 보려면 페이지에서 본인의 TMDB API Key (v3)를 입력하세요. 키는 탭 메모리에만 유지되며 새로고침하면 초기화됩니다.

## 자동 배포 설정

1. GitHub 저장소의 **Settings → Pages → Build and deployment → Source**를 **GitHub Actions**로 선택하세요.
2. 이 프로젝트 파일을 `main` 브랜치에 커밋하고 push하세요.
3. **Actions → Deploy Vue to GitHub Pages**가 성공했는지 확인하세요.

워크플로는 `npm ci` → `npm run build` → `dist` 업로드 → GitHub Pages 배포 순서로 실행됩니다.
`node_modules`와 `dist`는 Git에 올리지 않습니다.

배포 주소: https://beginnerproject3721.github.io/The_Movie_WebSite_Actions/

이 주소는 첫 배포가 성공한 뒤 사용할 수 있습니다.

## 로컬 빌드 확인

```bash
npm run build
npm run preview
```

TMDB 출처 정보는 [CREDITS.md](CREDITS.md)를 참고하세요.
