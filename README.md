# Agentic Systems for Automated GitHub Issue Solving: A Survey

## Introduction

Up to 2025-04-06, automated GitHub issue solving technologies can be mainly surveyed from 2 perspectives:
Design Paradigms and Foundation Model.

From the perspective of Design Paradigms, we can classify them into 3 categories:
> @Agent-Based Method  
> @Pipeline-Based Method  
> @RAG-Based Method

The workflow of these methods usually includes 3 phases: localization, repair, and patch validation.

From the perspective of Foundation Model, we can classify them into 2 categories:
> @SFT-Based Method  
> @RL-Based Method

## Table of Contents

- [Design Paradigms](#design-paradigms)
- [Foundation Model](#foundation-model)

[//]: # "[Paper]&#40;&#41;[Code]&#40;&#41;"

## Benchmarks

| Literature                                                                                             |        Name         |            Scope             | Journal/Conference |  Time   |                                                     Link                                                     |
|:-------------------------------------------------------------------------------------------------------|:-------------------:|:----------------------------:|:------------------:|:-------:|:------------------------------------------------------------------------------------------------------------:|
| SWE-bench: Can Language Models Resolve Real-World GitHub Issues?                                       |      SWE-bench      |          End-To-End          |      ICLR'24       | 2023-10 |         [Paper](https://arxiv.org/abs/2310.06770)<br/>[Code](https://github.com/swe-bench/SWE-bench)         |
| SWT-Bench: Testing and Validating Real-World Bug-Fixes with Code Agents                                |      SWT-Bench      | Reproduction Test Generation |      ICLR'25       | 2024-06 |       [Paper](https://arxiv.org/abs/2406.12952)<br/>[Code](https://github.com/logic-star-ai/SWT-Bench)       |
| SWE-bench-java: A GitHub Issue Resolving Benchmark for Java                                            |   Muti-SWE-bench    |          End-To-End          |       ARXIV        | 2024-08 | [Paper](https://arxiv.org/abs/2408.14354)<br/>[Code](https://github.com/multi-swe-bench/multi-swe-bench-env) |
| SWE-bench Multimodal: Do AI Systems Generalize to Visual Software Domains?                             | SWE-bench Mutimodal |          End-To-End          |      ICLR'25       | 2024-10 |         [Paper](https://arxiv.org/abs/2410.03859)<br/>[Code](https://github.com/swe-bench/SWE-bench)         |
| SWE-Bench+: Enhanced Coding Benchmark for LLMs                                                         |     SWE-Bench+      |          End-To-End          |       ARXIV        | 2024-10 |                                  [Paper](https://arxiv.org/abs/2410.06992)                                   |
| TestGenEval: A Real World Unit Test Generation and Test Completion Benchmark                           |     TestGenEval     | Reproduction Test Generation |      ICLR'25       | 2024-10 |      [Paper](https://arxiv.org/abs/2410.00752)<br/>[Code](https://figshare.com/s/51171ae97cd21d233d4f)       |
| A Real-World Benchmark for Evaluating Fine-Grained Issue Solving Capabilities of Large Language Models |      FAUN-Eval      |          End-To-End          |       ARXIV        | 2024-11 |                                  [Paper](https://arxiv.org/pdf/2411.18019)                                   |
| TDD-Bench Verified: Can LLMs Generate Tests for Issues Before They Get Resolved?                       |      TDD-Bench      | Reproduction Test Generation |       ARXIV        | 2024-11 |        [Paper](http://arxiv.org/abs/2412.02883)<br/>[Code](https://github.com/IBM/TDD-Bench-Verified)        |
| Multi-SWE-bench: A Multilingual Benchmark for Issue Resolving                                          |   Muti-SWE-bench    |          End-To-End          |       ARXIV        | 2025-04 |   [Paper](https://arxiv.org/abs/2504.02605)<br/>[Code](https://github.com/multi-swe-bench/multi-swe-bench)   |
| LocAgent: Graph-Guided LLM Agents for Code Localization                                                |      LocBench       |         Localization         |       ARXIV        | 2025-03 |            [Paper](https://arxiv.org/abs/2503.09089)<br/>[Code](https://arxiv.org/abs/2503.09089)            |

## Design Paradigms

### Issue Localization


### Repair

| Literature                                                                                         |             Name             | Journal/Conference |  Time   |   Label   |                                                    URL                                                     |
|----------------------------------------------------------------------------------------------------|:----------------------------:|:------------------:|:-------:|:---------:|:----------------------------------------------------------------------------------------------------------:|
| Swe-agent: Agent-computer interfaces enable automated software engineering                         |          SWE-Agent           |    NeurIPS 2024    | 2024-05 |  @Agent   |        [Paper](https://arxiv.org/abs/2405.15793)<br/>[Code](https://github.com/SWE-agent/SWE-agent)        |
| Autocoderover: Autonomous program improvement                                                      |        AutoCodeRover         |     ISSTA 2024     | 2024-04 |  @Agent   |  [Paper](https://arxiv.org/abs/2404.05427)<br/>[Code](https://github.com/AutoCodeRoverSG/auto-code-rover)  |
| CodeR: Issue Resolving with Multi-Agent and Task Graphs                                            |            CodeR             |       Arxiv        | 2024-06 |  @Agent   |           [Paper](https://arxiv.org/abs/2406.01304)<br/>[Code](https://github.com/NL2Code/CodeR)           |
| Alibaba LingmaAgent: Improving Automated Issue Resolution via Comprehensive Repository Exploration |         LingmaAgent          | FSE Companion 2025 | 2024-06 |  @Agent   | [Paper](https://arxiv.org/abs/2406.01422)<br/>[Code](https://github.com/RepoUnderstander/RepoUnderstander) |
| MASAI: Modular Architecture for Software-engineering AI Agents                                     |            MASAI             |       Arxiv        | 2024-06 |  @Agent   |                                 [Paper](https://arxiv.org/abs/2406.11638)                                  |
| Agentless: Demystifying llm-based software engineering agents                                      |          Agentless           |      FSE 2025      | 2024-07 | @Pipeline |      [Paper](https://arxiv.org/abs/2407.01489)<br/>[Code](https://github.com/OpenAutoCoder/Agentless)      |
| OpenHands: An Open Platform for AI Software Developers as Generalist Agents                        |          OpenHands           |     ICLR 2025      | 2024-07 |  @Agent   |      [Paper](https://arxiv.org/abs/2407.16741)<br/>[Code](https://github.com/All-Hands-AI/OpenHands)       |
| Specrover: Code intent extraction via llms                                                         | SpecRover (AutoCodeRover-v2) |     ICSE 2025      | 2024-08 |  @Agent   |  [Paper](https://arxiv.org/abs/2408.02232)<br/>[Code](https://github.com/AutoCodeRoverSG/auto-code-rover)  |
| SuperCoder2.0: Technical Report on Exploring the feasibility of LLMs as Autonomous Programmer      |          SuperCoder          |       Arxiv        | 2024-09 |  @Agent   |                                 [Paper](https://arxiv.org/abs/2409.11190)                                  |
| Hyperagent: Generalist software engineering agents to solve coding tasks at scale                  |          HyperAgent          |       Arxiv        | 2024-09 |  @Agent   |                                 [Paper](https://arxiv.org/abs/2409.16299)                                  |
| RepoGraph: Enhancing AI Software Engineering with Repository-level Code Graph                      |          RepoGraph           |     ICLR 2025      | 2024-10 | @Pipeline |         [Paper](https://arxiv.org/abs/2410.14684)<br/>[Code](https://github.com/ozyyshr/RepoGraph)         |
| SWE-Search: Enhancing Software Agents with Monte Carlo Tree Search and Iterative Refinement        |          SWE-Search          |     ICLR 2025      | 2024-10 |  @Agent   |   [Paper](https://arxiv.org/abs/2410.20285)<br/>[Code](https://github.com/aorwall/moatless-tree-search)    |
| Infant Agent: A Tool-Integrated, Logic-Driven Agent with Cost-Effective API Usage                  |         Infant Agent         |       Arxiv        | 2024-11 |  @Agent   |                                 [Paper](https://arxiv.org/abs/2411.01114)                                  |
| MarsCode Agent: AI-native Automated Bug Fixing                                                     |        MarsCode Agent        |       Arxiv        | 2024-11 |  @Agent   |                                 [Paper](https://arxiv.org/abs/2409.00899)                                  |


### Patch Validation



## Foundation Model

| Literature                                                                                            |      Name      | Journal/Conference | Time | Label |                    URL                    |
|-------------------------------------------------------------------------------------------------------|:--------------:|:------------------:|:----:|:-----:|:-----------------------------------------:|
| Lingma SWE-GPT: An Open Development-Process-Centric Language Model for Automated Software Improvement | Lingma SWE-GPT | FSE 2025 Industry  | 2024 | @SFT  | [Paper](https://arxiv.org/abs/2411.00622) |
