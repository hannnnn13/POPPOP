# 밤걷의 포트폴리오 (POPPOP)

보안과 AI를 공부하는 밤걷의 개인 소개 사이트입니다. 초급프로젝트 과제 1로 Hugo 테마를 골라 내 사이트로 바꾸고, GitHub Actions로 자동 배포했습니다.

- 공개 사이트: https://hannnnn13.github.io/POPPOP/
- 저장소: https://github.com/hannnnn13/POPPOP
- 배포 기록: https://github.com/hannnnn13/POPPOP/actions

## 필요한 도구와 버전

| 도구 | 배포(GitHub Actions) | 작성자 PC에서 확인한 버전 |
| --- | --- | --- |
| Hugo extended | 0.167.0 (`.github/workflows/hugo-pages.yml`에 고정) | 0.169.0 |
| Python | 3.12 | 3.13.15 |
| Git | Actions 기본값 | 2.50.1 |
| OS | ubuntu-latest | macOS 26.3 |

- Hugo는 반드시 **extended** 버전을 설치합니다. macOS는 `brew install hugo`, Windows는 `winget install Hugo.Hugo.Extended`로 설치할 수 있습니다.
- 테마는 `site/themes/template`에 들어 있어 따로 내려받을 필요가 없습니다. npm 등 추가 의존성은 없습니다.
