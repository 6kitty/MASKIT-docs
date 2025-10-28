---
title: Home
layout: home
nav_order: 1
---

MASKIT

MASKIT (마스킷)

AI 기반 지능형 PII 마스킹 솔루션: 이메일 속 개인정보, 이제는 알아서 보호합니다.

## 개요 (Overview)

MASKIT은 이메일 프록시 환경에서 전송되는 텍스트를 분석하여 개인정보(PII)를 자동으로 탐지하고, 사내 규칙 및 법규에 따라 지능적으로 마스킹하는 AI 솔루션입니다.

단순히 모든 개인정보를 마스킹하는 기존 DLP와 달리, MASKIT은 LLM(거대 언어 모델)과 RAG(검색 증강 생성) 기술을 활용하여 이메일의 **문맥(Context)**을 이해합니다. 이를 통해 '업무상 반드시 필요한 PII'와 '불필요하게 노출된 PII'를 구분하여, 보안성은 높이고 업무 효율 저하는 최소화하는 것을 목표로 합니다.

## 주요 기능 (Core Features)

🧠 문맥 인식 마스킹: 이메일의 송수신자, 목적 등을 파악하여 PII 마스킹 여부를 유연하게 결정합니다.
📚 규칙 기반 추론: 단순 사례 학습에 의존하지 않고, 사전에 정의된 **'애플리케이션 가이드'**와 법규를 최우선으로 참조하여 일관되고 설명 가능한 판단을 내립니다.
🔎 설명 가능한 AI (XAI): 왜 특정 정보를 마스킹했는지(또는 안 했는지)에 대한 판단 근거를 명확하게 제시하여 사용자의 신뢰도를 높입니다.
🚀 유연한 확장성: FastAPI 기반의 API로 설계되어 기존 이메일 시스템이나 다양한 워크플로우에 쉽게 연동할 수 있습니다.
## 아키텍처 (Architecture)

MASKIT은 LangGraph 프레임워크를 사용하여 체계적인 데이터 처리 파이프라인을 구축했습니다.

PII 탐지 (Detection): 이메일에서 마스킹이 필요한 개인정보 후보군을 식별합니다.
문맥 분석 (Context Analysis): LLM이 이메일의 비즈니스 맥락(목적, 송수신자 관계 등)을 분석합니다.
정보 검색 (Retrieval - RAG): 분석된 문맥을 기반으로 '애플리케이션 가이드', 사내 정책, 법률 DB에서 가장 관련성 높은 문서를 검색합니다.
추론 및 결정 (Reasoning & Decision): LLM이 이메일 내용, 문맥, 검색된 문서를 종합하여 최종 마스킹 여부와 방법을 결정합니다.
마스킹 처리 (Masking): 결정된 내용에 따라 이메일 본문을 수정하여 반환합니다.

This is a *bare-minimum* template to create a Jekyll site that uses the [Just the Docs] theme. You can easily set the created site to be published on [GitHub Pages] – the [README] file explains how to do that, along with other details.

If [Jekyll] is installed on your computer, you can also build and preview the created site *locally*. This lets you test changes before committing them, and avoids waiting for GitHub Pages.[^1] And you will be able to deploy your local build to a different platform than GitHub Pages.

More specifically, the created site:

- uses a gem-based approach, i.e. uses a `Gemfile` and loads the `just-the-docs` gem
- uses the [GitHub Pages / Actions workflow] to build and publish the site on GitHub Pages

Other than that, you're free to customize sites that you create with this template, however you like. You can easily change the versions of `just-the-docs` and Jekyll it uses, as well as adding further plugins.

[Browse our documentation][Just the Docs] to learn more about how to use this theme.

To get started with creating a site, simply:

1. click "[use this template]" to create a GitHub repository
2. go to Settings > Pages > Build and deployment > Source, and select GitHub Actions

If you want to maintain your docs in the `docs` directory of an existing project repo, see [Hosting your docs from an existing project repo](https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md#hosting-your-docs-from-an-existing-project-repo) in the template README.

----

[^1]: [It can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-site).

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
