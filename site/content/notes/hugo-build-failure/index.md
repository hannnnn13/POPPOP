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
