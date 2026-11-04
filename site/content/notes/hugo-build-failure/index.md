---
title: "Hugo 빌드 실패를 해결한 기록"
date: 2026-11-04
summary: "예시 글을 지운 뒤 GitHub Actions 빌드가 멈춘 원인을 찾고 고친 과정"
tags:
  - hugo
  - github-actions
  - 문제해결

content:
  format: "note"
  status: "published"
---

## 무슨 일이 있었나

2026년 11월 3일, 메뉴를 고친 커밋을 push했는데 GitHub Actions의 빌드 단계가 실패했습니다. 그 뒤에 올린 커밋도 똑같이 실패해서, 공개 사이트는 그 전에 성공한 버전에 멈춰 있었습니다.

## 로그 읽기

실패한 실행([Actions 기록](https://github.com/hannnnn13/POPPOP/actions/runs/41632279413))의 빌드 로그에서 `ERROR`로 시작하는 줄을 찾았습니다.

```text
ERROR No Fate homepage: selected_writing references missing or unpublished path "/essays/maintenance-is-a-design-material/"
```

홈 화면의 `selected_writing` 설정이 존재하지 않는 글을 가리키고 있다는 뜻이었습니다.

## 원인

바로 전에 테마의 예시 글(essays 폴더)을 지웠는데, 홈 화면 설정 파일(`site/content/_index.md`)에는 그 글의 주소가 남아 있었습니다. 이 테마는 `strictHomeSelections` 설정이 켜져 있어서, 홈이 없는 글을 참조하면 경고에서 끝나지 않고 빌드 자체를 멈춥니다.

## 고친 방법

1. 배포 스크립트가 쓰는 것과 같은 Hugo 명령으로 내 컴퓨터에서 빌드해, 같은 오류가 나는 것을 먼저 확인했습니다.
2. 홈 설정에서 지운 글의 참조를 빼고, 쓰지 않는 모듈이 가리키던 다른 예시 글 주소도 함께 정리했습니다.
3. 다시 빌드해 오류가 사라진 것을 확인했습니다.

## 다시 확인한 결과

수정한 커밋을 push하자 Actions의 빌드와 배포가 모두 성공했고([Actions 기록](https://github.com/hannnnn13/POPPOP/actions/runs/41758654144)), 공개 사이트에도 변경이 반영됐습니다.

## 다음에는

- 파일을 지우기 전에 그 파일을 가리키는 곳이 있는지 먼저 검색합니다.
- push하기 전에 배포와 같은 명령으로 직접 빌드해 봅니다.
