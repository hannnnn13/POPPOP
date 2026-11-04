---
title: "AI가 코드를 짜는 시대, 보안과 책임"
date: 2026-11-04
summary: "AI로 늘어난 보안 위협 사례와 통계, 그리고 사람이 책임져야 하는 이유"
tags:
  - 보안
  - ai

content:
  format: "note"
  status: "published"
---

AI가 코드를 빠르게, 잘 짜게 되면서 개발은 쉬워졌습니다. 하지만 같은 도구를 공격하는 쪽도 씁니다. 보안에 관심을 갖게 된 이유를 정리하려고, 2023년부터 실제로 있었던 사례와 숫자를 모았습니다.

## AI가 짠 코드는 안전할까

| 수치 | 내용 | 출처 |
| --- | --- | --- |
| 45% | AI가 생성한 코드 중 보안 취약점이 있는 비율 (LLM 100여 개, 과제 80개) | [Veracode, 2025](https://www.veracode.com/press-release/ai-generated-code-poses-major-security-risks-in-nearly-half-of-all-development-tasks-veracode-research-reveals/) |
| 5개 중 4개 | AI 도움을 받은 개발자가 더 취약한 코드를 쓴 과제 수. 그러면서도 자기 코드가 더 안전하다고 믿었음 | [Stanford, 2023](https://arxiv.org/abs/2211.03622) |
| 19.7% | LLM이 추천한 패키지 중 실제로 존재하지 않는 이름의 비율. 공격자가 그 이름으로 악성 패키지를 올릴 수 있음 | [USENIX Security, 2025](https://arxiv.org/abs/2406.10279) |

## 실제로 있었던 일

| 시기 | 사례 | 출처 |
| --- | --- | --- |
| 2023년 7월 | 범죄용 챗봇 WormGPT가 판매되어, 기업 메일 사기 문안을 자동으로 만들어 냄 | [CSO Online](https://www.csoonline.com/article/646441/wormgpt-a-generative-ai-tool-to-compromise-business-emails.html) |
| 2024년 2월 | 러시아·북한·이란·중국의 해커 그룹이 LLM을 정찰과 피싱 문구 작성에 쓰다 계정이 차단됨 | [Microsoft](https://www.microsoft.com/en-us/security/blog/2024/02/14/staying-ahead-of-threat-actors-in-the-age-of-ai/) |
| 2024년 | 홍콩의 한 직원이 참석자 전원이 딥페이크인 화상회의에 속아 15번에 걸쳐 약 2,560만 달러를 송금 | [CNN](https://edition.cnn.com/2024/05/16/tech/arup-deepfake-scam-loss-hong-kong-intl-hnk) |
