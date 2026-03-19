---
date: '2026-03-19'
draft: true
title: 'Evals for RAG apps'
tags: ["RAG","How I AI","evals"]
---

A RAG pipeline is something that extracts internal knowledge using Vector DBs, validates information using citation & confidence scoring & produce safe, context aware answers using LLM

- Knowledge Layer
    - Internal Documents
    - Private Sources
    - Chunking (Split into smaller pieces by using different strategies)
    - Store into a Vector DB (for a semantic search)
    - Also, store meta-data along with it for much better filtering late ron

- Retrieval Layer
    - Embed the user query
    - Execute a semantic search (meta-data based filtering)
    - Security Filters
    - Top K retrieval
    - This is what will be additional context for LLMs

- Generation Layer
    - Pass top K chunks as knowledge to LLM to answer user query
    - Elaborate system prompt on how to use the extracted chunks
    - Validation Layer (Citing of sources)

- Validation Layer
    - Cite the sources
    - Confidence Scoring
    - Knowledge based vaidation before output
    - Adding Human in the loop for a High Risk Task

Use Cases - Decision Support, Incident Resolutions

Some Axis to think about when making RAG system - Safety, Governance, Validation, Approval Layers

How to think about evals for RAG based systems?
Can structure evaluation of these systems
- Retrieval Evaluation
- Generation Evalation


Traditional Metrics
- BLEU
- ROUGE
- F1

RAG Evaluation
For retrieval
- Context Precision
- Context Recall

For Generation
- Faithfullness
- Answer Relevance

Can use LLM-as-a-judge for these
there is an open source



Recall @ K
Precision @ K
MRR Mean Reciprocal Rank
Normalized Discounted Cumulative gain

LLM as judge to check faithfull or Answer relevancy