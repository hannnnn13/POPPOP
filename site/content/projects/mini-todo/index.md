---
title: "mini-todo"
date: 2026-10-13
summary: "React와 Firebase로 만든 로그인 할 일 목록"
tags:
  - projects

content:
  format: "project"
  status: "완료"
  media_type: "website"
  collection: "수업 실습"

visual:
  mode: "editorial"
---

## 한눈에 보기

- **시기:** 2026년 10월, 초급프로젝트 7주차 수업 실습
- **상태:** 완료
- **역할:** 개인 실습. 수업에서 받은 시작 코드로 직접 따라 하며 배포까지 했습니다.

React 화면에 Firebase 로그인과 데이터베이스(Firestore)를 연결한 할 일 목록 앱입니다.

## 보안 관점에서 본 점

- Firebase 설정값은 `.env` 파일에 따로 두고, 이 파일은 `.gitignore`로 저장소에 올라가지 않게 했습니다.
- Firestore 보안 규칙(`firestore.rules`)으로 로그인한 사용자가 자기 데이터만 읽고 쓸 수 있게 했습니다.

## 결과물

- 배포된 페이지: [hannnnn13.github.io/mini-todo](https://hannnnn13.github.io/mini-todo/)
- 소스 저장소: [github.com/hannnnn13/mini-todo](https://github.com/hannnnn13/mini-todo)
