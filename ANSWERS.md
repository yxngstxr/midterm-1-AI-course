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
| H |0.867 |kk degraded |0.767 | 0.591 | 0.882 | 21418|
| L |0.828 | kk clean  | 0.733| 0.556| 0.858| 18000|

Personal-data pages per year sent abroad under H:

### 2b. Memo (at most 300 words)
Who is served worst Overall accuracy H 0 867 156 out of 180 L 0 828 149 out of 180 The overall figure hide Kazakh Under L Kazakh score 0 733 in both conditions 22 out of 30 each 95 percent CI 0 556 to 0 858 Under H the weakest cell is Kazakh degraded 0 767 0 591 to 0 882 With 30 invoices per cell all intervals overlap so I cannot claim H is really more accurate Kazakh is lowest under both pipelines and L is lower there but this is a signal not a proof
Personal data three questions of Lecture 5 1 24 percent of pages carry a name and ИИН 788400 pages a year H the scan goes to a data centre abroad known Who stores it and for how long is unknown A vendors statement is not a compliance review so I would need to see the contract and get a legal check under law No 94 V L the scan stays on our server in Kazakhstan known We store it so we set retention but the period and access rules are not defined yet
Safeguards 1 No H use before contract and legal review 2 Under L delete scans after a fixed number of days verified by a monthly check of storage 3 Access log reviewed monthly no ИИН in application logs 4 Kazakh and degraded pages goes to human review 5 Quarterly accuracy check on a 30 page sample per language
Choice L costs 18000 dollars a year against 21418 dollars for H keeps all personal data pages in the country and its accuracy gap is not statistically proven Residual risk roughly a quarter of Kazakh invoices are extracted wrong so review is needed and a breach or weak retention on our own server is our responsibility
## Part 3: Explain your own numbers

### Q1

Number:2ю08
Why (at most 40 words): Щutput tokens cost 5x input tokens, and the mix differs: KK needs 2.44x the input but only 1.50x the output, so the cost-weighted ratio (2.08) is below the token ratio (2.34).

### Q2

Number 533
Why (at most 40 words): ноу the sentences tarts at about e5 token 533, beyond the 512 limit, so it is truncated and never embedded. The chunk cannot match it, and no error is raised: the failure is silent.
### Q3

Number:90.8
Why (at most 40 words): The ranking did not change softmax is monotonic Lower T sharpens probabilities, so Monday gets 90.8 %. Every token still has non-zero probability, so the sampleable set stays the same unless top-k or top-p cuts it.

### Q4

Number:
Why (at most 40 words):

### Q5

Number:
Why (at most 40 words):
