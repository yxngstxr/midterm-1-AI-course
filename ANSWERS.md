# Midterm 1: answers

GitHub username:
Session code:
Fingerprint:

> Fill in the three lines above from `my_data/DATA.md`. Do not rename headings or table columns: a script reads the numbers.
> Write only in the empty cells and lines. Percentages as 0.78 or 78 %, money as plain numbers.

## AI-use declaration

**Tools used:**
- Claude (claude.ai, Anthropic) as a chat assistant.
- Google Colab (Python, pandas) to run `make_my_data.py` and compute all numbers.

**What I used them for:**
1. *Understanding the task.* I used Claude to turn the exam text into a step-by-step plan: the order of parts, the submission procedure (GitHub web editor, commit URL), and how to work without git and local Python.
2. *Code.* I used Claude to help write Python snippets in Colab for recall@k, MRR@10, Wilson intervals, the cost formulas (request cost, pipeline H and L annual cost), and grouping by language and scan condition. I ran the code on my own data and checked the outputs against the formulas in the exam text. 
3. *Wording.* I used an AI assistant to  translate the text of the decision (1d), the memo (2b) and the Why lines (Part 3). 

**What I did myself:**
- Ran the generator with my own GitHub username and the session code, and checked that the fingerprint matches.
- Chose the recommended candidate (1d) and the pipeline (2b), and decided how to weigh accuracy, cost and risk.
- Read and checked every number in ANSWERS.md, and I can explain each one at the oral check.

**What I did not do:** I did not share my data or answers with other students, and I did not copy anyone else's text.


## Part 1: Retrieval and cost decision

### 1a. Metrics (all 60 questions)

| config | recall@1 | recall@3 | recall@5 | MRR@10 |
|---|---|---|---|---|
| A | | | | |
| B | | | | |

### 1b. Recall and 95 % Wilson interval of each candidate (recall at its own k)

| candidate | recall@k | lower | upper |
|---|---|---|---|
| A, k=3 | | | |
| A, k=5 | | | |
| B, k=3 | | | |
| B, k=5 | | | |

### 1c. Annual model cost in USD

| candidate | annual cost |
|---|---|
| A, k=3 | |
| A, k=5 | |
| B, k=3 | |
| B, k=5 | |

### 1d. Decision (at most 150 words)

Chosen candidate:

(Decision, using your intervals and the budget. Give the recall of your choice for EN, RU and KK separately.)

### 1e. Next measurement (at most 60 words)

## Part 2: A document pipeline you can defend

### 2a. Numbers

| pipeline | overall accuracy | weakest cell (language, condition) | accuracy there | lower | upper | annual cost |
|---|---|---|---|---|---|---|
| H | | | | | | |
| L | | | | | | |

Personal-data pages per year sent abroad under H:

### 2b. Memo (at most 300 words)

## Part 3: Explain your own numbers

### Q1

Number:
Why (at most 40 words):

### Q2

Number:
Why (at most 40 words):

### Q3

Number:
Why (at most 40 words):

### Q4

Number:
Why (at most 40 words):

### Q5

Number:
Why (at most 40 words):
