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

## 내 컴퓨터에서 확인하기

저장소를 내려받은 뒤 아래 명령은 모두 저장소 맨 위 폴더에서 시작합니다.

```sh
git clone https://github.com/hannnnn13/POPPOP.git
cd POPPOP
```

**미리 보기** (파일을 고치면 바로 반영됩니다)

```sh
cd site
hugo server --config hugo.yaml,pages.json
```

브라우저에서 터미널에 나온 주소(기본값 http://localhost:1313/POPPOP/)를 엽니다.

**배포와 같은 방식으로 빌드하기** (push 전에 오류가 없는지 확인할 때)

```sh
python3 .github/pages_build.py --build
```

`빌드 완료`가 나오고 `public/index.html`이 생기면 성공입니다. `public/` 폴더는 `.gitignore`로 저장소에 올라가지 않습니다.

## 수정할 파일 위치

| 바꾸고 싶은 것 | 파일 |
| --- | --- |
| 홈 화면 문구와 홈에 보일 글 | `site/content/_index.md` |
| 소개 페이지 | `site/content/about/_index.md` |
| 프로젝트 글 | `site/content/projects/<이름>/index.md` |
| 학습 기록 글 | `site/content/notes/<이름>/index.md` |
| 사이트 제목, 메뉴, 작성자, 푸터 | `site/hugo.yaml` |
| 테마 화면 문구의 한국어 번역 | `site/i18n/ko.yaml` |
| 테마 CSS 보완 | `site/layouts/_partials/extend_head.html` |
| 자동 배포 설정 | `.github/workflows/hugo-pages.yml` |

테마 원본(`site/themes/template`)은 직접 고치지 않고, 필요한 변경은 위의 `site/` 쪽 파일로 덮어씁니다.
