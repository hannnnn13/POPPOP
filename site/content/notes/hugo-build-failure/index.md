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
