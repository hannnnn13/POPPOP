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
| 2025년 7월 | 북한 해킹 조직이 챗GPT로 만든 가짜 군무원 신분증으로 국내 기관에 피싱 메일을 보냄 | [뉴스1](https://www.news1.kr/it-science/general-it/5912484) |
| 2025년 8월 | 악성 npm 패키지가 개발자 PC의 AI 코딩 도구를 실행시켜 비밀 정보를 빼 감 | [Socket](https://socket.dev/blog/nx-packages-compromised) |
| 2025년 8월 | 범죄자 한 명이 AI 코딩 도구로 침투를 자동화해 최소 17개 기관의 데이터를 빼내고 돈을 요구 | [Anthropic](https://www.anthropic.com/news/detecting-countering-misuse-aug-2025) |
| 2025년 11월 | 국가 배후로 추정되는 그룹이 AI 에이전트로 약 30개 기관을 공격. 사람은 중간중간 몇 번만 개입 | [Anthropic](https://www.anthropic.com/news/disrupting-AI-espionage) |

## 속이는 기술도 좋아졌다

- AI로 만든 피싱 메일의 클릭률은 54%로, 일반 피싱(12%)의 약 4.5배였습니다. ([Microsoft 보고서 보도, 2025](https://www.theregister.com/2025/10/16/ai_makes_phishing_45x_more_effective))
- 2024년 1월부터 10월까지 국내 경찰에 접수된 딥페이크 성범죄는 964건이었고, 검거된 사람의 81.2%가 10대였습니다. ([파이낸셜뉴스, 경찰청 발표](https://www.fnnews.com/news/202410301102016945))

## AI는 막는 쪽에서도 쓰인다

- Google의 AI 에이전트 Big Sleep은 실제 오픈소스 소프트웨어의 취약점을 찾아, 악용되기 전에 막았다고 발표했습니다. ([Google](https://blog.google/innovation-and-ai/technology/safety-security/cybersecurity-updates-summer-2025/))
- 미국 DARPA의 AI 사이버 대회(AIxCC)에서는 AI 시스템이 심어 둔 취약점 63개 중 54개를 찾아내고 43개를 고쳤습니다. ([DARPA, 2025](https://www.darpa.mil/news/2025/aixcc-results))

결국 AI는 도구이고, 공격과 방어 중 어느 쪽에 쓰일지는 사람에게 달려 있습니다.
