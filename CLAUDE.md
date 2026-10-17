# P23-미로봇(Mirobot)

미로 사진을 넣으면 🤖 로봇이 BFS(가장 짧은 길 찾기)로 푸는 과정을 보여주고, 길이 없으면 "풀 수 없어요"라고 알려주는 웹페이지 (`index.html` 더블클릭으로 실행, 로고 `logo.svg`).
- 배포: 깃허브 `kmathlove-wq/Mirobot`(공개) → 깃허브 페이지 `https://kmathlove-wq.github.io/Mirobot/` (도메인 없는 예비 주소)
- 실제 서비스: Cloudflare **Pages** 프로젝트 `mirobot` → 미로봇.kro.kr(`xn--2o2b19djxa.kro.kr`) + www (내도메인.한국에서 CNAME → mirobot.pages.dev). kro.kr은 깃허브 인증서가 안 돼서 Cloudflare 사용.
- 고치면 **항상 둘 다**: 깃허브 커밋·푸시 + Cloudflare 배포. Cloudflare 배포는 `index.html`·`logo.svg`만 담은 한글 없는 임시 폴더(설정 파일 없는 곳)에서: `npx wrangler pages deploy <임시폴더> --project-name mirobot --branch main --force` (`pages project create`는 `--force` 없으면 Workers로 만들어짐)
- 구글 서치 콘솔: URL 접두어 속성 `https://미로봇.kro.kr/`, HTML 태그로 소유권 확인 완료(2026-10-17)·색인 요청함. `index.html`의 `google-site-verification` 메타·canonical(→ kro.kr)·description은 **지우지 말 것**.
<!-- 상위 CLAUDE.md 규칙을 여기 재서술하지 말 것 -->
