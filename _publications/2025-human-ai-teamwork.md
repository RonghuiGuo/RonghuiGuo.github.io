---
title: "Empowering Agile-Based Generative Software Development through Human-AI Teamwork"
collection: publications
category: manuscripts
permalink: /publication/2025-human-ai-teamwork
excerpt: 'An agile-based generative software development framework (AgileGen) using Gherkin-based acceptance criteria and human-AI teamwork to ensure semantic consistency between requirements and code.'
date: 2025-07-03
venue: 'ACM Transactions on Software Engineering and Methodology (TOSEM), Vol. 34, No. 6'
paperurl: 'https://doi.org/10.1145/3702987'
citation: 'Sai Zhang, Zhenchang Xing, Ronghui Guo, Fangzhou Xu, Lei Chen, Zhaoyuan Zhang, Xiaowang Zhang, Zhiyong Feng, and Zhiqiang Zhuang. (2025). "Empowering Agile-Based Generative Software Development through Human-AI Teamwork." <i>ACM Transactions on Software Engineering and Methodology (TOSEM)</i>, Vol. 34, No. 6, Article 156, pp. 1–46.'
---
In software development, raw requirements proposed by users are frequently incomplete, impeding the full implementation of software functionalities. With the emergence of large language models (LLMs), recent top-down waterfall-model approaches employ questioning strategies to complete requirements. However, users—constrained by their domain knowledge—lack effective acceptance criteria, failing to capture implicit needs. Furthermore, cumulative errors in the waterfall model cause discrepancies between generated code and user requirements. Agile methodologies can reduce cumulative errors through lightweight iteration and user collaboration, but ensuring semantic consistency between requirements and code remains challenging.

To address these issues, we propose **AgileGen**, an agile-based generative software development framework built on human-AI teamwork. AgileGen makes the following key contributions: (1) it uses the Gherkin language (a formal Behavior-Driven Development language) to create testable requirement descriptions, serving as a bridge for semantic consistency between requirements and code; (2) a human-AI collaboration model where users participate in decision-making processes suited to their strengths (requirement proposal, clarification, and iterative acceptance), while AI handles technical code generation; (3) Gherkin-based requirements are translated into natural-language scenarios, reducing users' knowledge barriers; (4) consistency factors derived from Gherkin scenarios guide code generation to ensure alignment with user needs; and (5) a memory pool mechanism collects user decision-making scenarios and recommends them to new users with similar requirements.

AgileGen significantly outperformed existing best methods by 16.4% and garnered higher user satisfaction scores on both the UEQ (User Experience Questionnaire) and Likert scale assessments, evaluated across 40 diverse web projects and the SRDD software task dataset.
