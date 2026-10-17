# Midterm 1: answers

GitHub username:
Session code:
Fingerprint:

> Fill in the three lines above from `my_data/DATA.md`. Do not rename headings or table columns: a script reads the numbers.
> Write only in the empty cells and lines. Percentages as 0.78 or 78 %, money as plain numbers.

## AI-use declaration

Tools used: Claude (Claude.ai) as a chat assistant; Google Colab to run python codes 
What I used them for:
1. Understanding the task: step-by-step plan
2. Code and calculation: Claude wrote Python for the variables
3. Wording: Claude drafted the decision



## Part 1: Retrieval and cost decision

### 1a. Metrics (all 60 questions)

| config | recall@1 | recall@3 | recall@5 | MRR@10 |
|---|---|---|---|---|
| A |0.383 |0.533 |0.617 |0.480 |
| B | 0.333| 0.500 |0.833| 0.484 |

### 1b. Recall and 95 % Wilson interval of each candidate (recall at its own k)

| candidate | recall@k | lower | upper |
|---|---|---|---|
| A, k=3 |0.533 | 0.409 | 0.654 |
| A, k=5 | 0.617| 0.490 | 0.729 |
| B, k=3 | 0.500| 0.377|0.623 |
| B, k=5 |0.833 |0.720 |0.907 |

### 1c. Annual model cost in USD

| candidate | annual cost |
|---|---|
| A, k=3 | 21827|
| A, k=5 |28338 |
| B, k=3 |14850 |
| B, k=5 | 16710|

### 1d. Decision (at most 150 words)

Chosen candidate:B, k=5

Annual cost is $16,710, within the $25,100 budget; (A,5) costs $28,338 and is excluded. Recall@5 is 0.833 (95 % CI 0.720-0.907). That interval does not overlap with (A,3) 0.533 (0.409-0.654) or (B,3) 0.500 (0.377-0.623), so it is better than both. It overlaps with (A,5) 0.617 (0.490-0.729), so I claim no difference there, but (A,5) is over budget anyway. Recall by language: EN 0.950 (0.764-0.991), RU 0.800 (0.584-0.919), KK 0.750 (0.531-0.888). Kazakh users are served worst; with n=20 per language these intervals overlap, so the language gap is not proven.

### 1e. Next measurement (at most 60 words)

Add about 60 more Kazakh and Russian test questions from real traffic and measure (B,5) recall@5 on them. If the Kazakh lower bound stays below 0.70, I would test a different chunk size or embedding model for Kazakh before launch.

## Part 2: A document pipeline you can defend

### 2a. Numbers

| pipeline | overall accuracy | weakest cell (language, condition) | accuracy there | lower | upper | annual cost |
|---|---|---|---|---|---|---|
| H |0.867 | | | | | |
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
