# GUARD Sycophancy Study
Benchmarking LLM susceptibility to moral sycophancy across five moral foundations using the OpenAI API — presented at NCUR 2026.

This project was conducted by the Group for Undergraduate AI Research and Development (GUARD) at Mississippi State University.

## Overview
This study measures how large language models shift their moral judgments when exposed to social pressure. Each scenario was rated by the model under two conditions: a neutral baseline prompt and an altered prompt containing an embedded social cue suggesting a particular rating. The difference between the two scores serves as the sycophancy measure.

## Moral Foundations Tested
- Care/Harm
- Fairness/Cheating
- Loyalty/Betrayal
- Authority/Subversion
- Liberty/Oppression

## Methodology
- Models: gpt-5.4, gpt-5.4-mini, gpt-5.4-nano
- Access dates: March 19-26, 2026
- Trials: 33 Iterations per scenario
- top_p: OpenAI default (1.0)
- max_tokens: Not specified (OpenAI default)
- Seed: Not set (non-deterministic)
- Temperature Open AI default (1.0)
- System prompt: None
- Output parsing: Regex '-?\d+' — extracts the first integer from the model response

## Key Findings
- LLMs showed measurable moral position shifts when exposed to embedded social pressure
- Most susceptible foundations: Loyalty / Betrayal and Authority / Subversion
- Difference scores and directional t-tests were used to quantify and assess significance of sycophantic shifts

## How to Run
- Clone the repository
- Open Sycophancy_Code.ipynb in Google Colab
- Install dependencies if needed
- In import cells, replace "Your Own API Key" with your OpenAi API Key
- Run Baseline once per scenario
- Run Altered per alteration, (Strongly Negative, Slightly Negative, Slightly Positive, Strongly Positive)
