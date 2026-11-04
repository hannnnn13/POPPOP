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

AI가 코드를 빠르게, 잘 작성하게 되면서 개발은 이전보다 압도적으로 쉬워졌습니다. 개발자만 할 수 있던 일을 이제는 누구나 AI로 할 수 있고, 상상하던 것을 직접 만들 수 있게 되었기 때문입니다. 반대로, 이는 보안 문제에 훨씬 더 많이 직면할 수 있다는 위험도 함께 키웁니다. 특히 개발자는 AI와 협의하면서 잘못 작성된 코드나 방향을 발견하고 조율하며 진행해 나갈 수 있지만, 비개발자는 거의 대부분을 AI의 행동에 의존하게 됩니다. 검토해 주는 사람도 없기 때문에 보안 위협에 처할 확률이 매우 높습니다.

여기, AI가 작성한 코드를 살펴본 조사를 인용했습니다.

## AI가 작성한 코드는 과연 안전한지에 대해 조사한 결과

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

## 그래서 내가 생각하는 것

AI 때문에 코딩하는 직업이 대체될 거라는 이야기가 많습니다. 하지만 AI가 짠 코드에서 문제가 생겼을 때, 그 잘못과 책임을 AI에게 온전히 돌릴 수는 없습니다. 코드를 쓰기로 정하고 배포한 것은 사람이기 때문입니다. 그래서 AI가 만든 결과는 반드시 사람이 검토하고, 사람이 책임질 수 있어야 한다고 생각합니다.

## AI가 작성한 코드를 쓰기 전에 확인해야 할 것

AI가 빠르게 코드를 작성하고 무작정 적용해 버리면, 코드를 작성하라고 지시한 사람은 흐름이 어떻게 되어 가고 있고 어떤 내용이 바뀌었는지 모르게 됩니다. 그러면 나중에는 자기가 무엇을 하고 있는지도 모르게 됩니다. 따라서 작성된 코드의 내용을 읽고, 전체 흐름이 어떤 식으로 흘러가고 있는지 정확히 알아야 합니다.

1. **직접 실행해 보기.** AI가 코드를 고치면 바로 현황을 파악할 수 있어야 하고, 내 의도와 다르게 동작할 수 있기 때문에 반드시 확인합니다.
2. **보안값이 노출되어 있는지 확인하기.** API 키나 비밀번호, 시크릿 값이 노출됐는지 파악합니다.
3. **의도와 다르게 흘러갈 경우 어떻게 할지 정하기.** 이상한 코드나 더 좋은 방안이 있었던 경우를 이해하고, 이해가 가지 않으면 사용하지 않습니다.
4. **바뀐 내용을 diff로 확인하고 커밋하기.** 마찬가지로 전체 흐름을 따라갈 수 있어야 합니다.
