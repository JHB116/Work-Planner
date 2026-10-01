# Work-Planner 작업 규칙

- 배포는 `main` 브랜치 기준이다. 사용자는 모든 작업을 PR 없이 바로 `main`에 배포하길 원한다.
- 작업을 마치면 커밋 후 지정된 작업 브랜치에 푸시하고, 같은 커밋을 `main`에도 바로 푸시한다(`git push origin HEAD:main`). PR은 만들지 않는다.
- `main`이 앞서 있으면 먼저 `git fetch origin main` 후 rebase/merge해서 fast-forward로 푸시한다. force-push는 하지 않는다.
- 배포할 때는 `sw.js`의 `SW_VERSION` 값을 바꿔야 앱에 새로고침 배너가 뜬다.
