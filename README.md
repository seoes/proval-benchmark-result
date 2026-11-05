# Proval benchmark results

These results are our own runs of the [Martian offline code review benchmark](https://github.com/withmartian/code-review-benchmark). The frozen set has 50 pull requests. The runner was rewritten for Proval, and every review was executed here. The public offline board is [here](https://codereview.withmartian.com/?mode=offline).

Each folder under `result/` is one published batch. Open a batch for the grouped view and the PR table. Core score is the primary score. Median review uses completed attempts.

## Latest full

|  |  |
| --- | --- |
| Batch | [full-790](result/full-790/) |
| Model | openai / muse-spark-1.3-contributor |
| Started | 2026-11-02 12:06 |
| Code | 05017bf5ce9e |
| Completed | 146 / 150 |
| Median review | 6.4 min |
| Core F2 | 48.4% |
| Precision | 52.9% |
| Recall | 47.4% |

## Runs

| Batch | Started | Profile | Model | Code | Completed | Median | Core score |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [full-790](result/full-790/) | 2026-11-02 12:06 | full | openai / muse-spark-1.3-contributor | 05017bf5ce9e | 146 / 150 | 6.4 min | 48.4% |
