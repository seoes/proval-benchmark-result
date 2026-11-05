# full-790

Run against the [Martian offline code review benchmark](https://github.com/withmartian/code-review-benchmark). The public offline board is [here](https://codereview.withmartian.com/?mode=offline).

|  |  |
| --- | --- |
| Profile | full |
| Model | openai / muse-spark-1.3-contributor |
| Started | 2026-11-02 12:06 |
| Code | 05017bf5ce9e |
| Planned | 150 |
| Recorded | 150 |
| Completed | 146 |
| Median review | 6.4 min |
| Core F2 | 48.4% |
| Precision | 52.9% |
| Recall | 47.4% |
| Judge | muse-spark-1.3-contributor |

Median review uses completed attempts. Core score is the primary score, from the first scored attempt of each PR.

## By project

| Project | PRs | Completed | Median | Range | Core score |
| --- | --- | --- | --- | --- | --- |
| cal_dot_com | 10 | 10 | 7.0 min | 1.7 min to 11.6 min | 50.0% |
| discourse | 10 | 10 | 5.5 min | 1.3 min to 14.7 min | 50.3% |
| grafana | 10 | 10 | 5.4 min | 2.7 min to 11.7 min | 39.8% |
| keycloak | 10 | 10 | 8.8 min | 2.2 min to 11.9 min | 45.1% |
| sentry | 10 | 9 | 7.2 min | 2.3 min to 10.8 min | 53.8% |

Group median is the median of the PR medians.

## By size

| Size | PRs | Completed | Median | Range | Core score |
| --- | --- | --- | --- | --- | --- |
| S | 11 | 11 | 5.1 min | 1.3 min to 11.9 min | 34.0% |
| M | 25 | 25 | 6.3 min | 1.7 min to 12.6 min | 50.4% |
| L | 13 | 13 | 7.7 min | 2.3 min to 14.7 min | 51.1% |
| XL | 1 | 0 | - | - | - |

S is up to 100 changed lines. M is up to 500. L is up to 2000. XL is above that. BZ is no text change.

## Where to look

### Slowest

| PR | Project | Size | Median |
| --- | --- | --- | --- |
| discourse__8 | discourse | L | 14.7 min |
| discourse__2 | discourse | M | 12.6 min |
| keycloak__36882 | keycloak | S | 11.9 min |
| grafana__106778 | grafana | L | 11.7 min |
| keycloak__32918 | keycloak | M | 11.6 min |

### Lowest core score

| PR | Project | Size | Core score | TP | FP | FN |
| --- | --- | --- | --- | --- | --- | --- |
| cal_dot_com__10600 | cal_dot_com | M | 0.0% | 0 | 5 | 4 |
| cal_dot_com__22345 | cal_dot_com | M | 0.0% | 0 | 1 | 1 |
| discourse__5 | discourse | S | 0.0% | 0 | 0 | 3 |
| discourse__9 | discourse | S | 0.0% | 0 | 0 | 2 |
| grafana__103633 | grafana | M | 0.0% | 0 | 0 | 3 |

## Score

Primary uses the first scored attempt of each PR. Pooled uses every scored attempt. A profile counts only golden comments in that profile. False positives stay in every profile.

Strict counts bug, security, concurrency, data and api comments. Core adds performance, test gap and documentation defects. All also adds style and speculative comments.

### Primary

| Profile | Precision | Recall | F1 | F2 | TP | FP | FN | Attempts |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| strict | 51.1% | 50.4% | 50.8% | 50.5% | 67 | 64 | 66 | 49 |
| core | 52.9% | 47.4% | 50.0% | 48.4% | 72 | 64 | 80 | 49 |
| all | 54.3% | 45.5% | 49.5% | 47.0% | 76 | 64 | 91 | 49 |

### Pooled

| Profile | Precision | Recall | F1 | F2 | TP | FP | FN | Attempts |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| strict | 51.7% | 49.9% | 50.8% | 50.2% | 198 | 185 | 199 | 146 |
| core | 53.4% | 46.7% | 49.8% | 47.9% | 212 | 185 | 242 | 146 |
| all | 54.8% | 44.9% | 49.3% | 46.6% | 224 | 185 | 275 | 146 |

## PR

Score columns use the primary core profile.

| PR | Project | Size | Lines | Files | Outcome | Median | Core score | TP | FP | FN |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| cal_dot_com__10600 | cal_dot_com | M | 316 | 16 | Completed 3 | 7.9 min | 0.0% | 0 | 5 | 4 |
| cal_dot_com__10967 | cal_dot_com | L | 584 | 22 | Completed 3 | 8.9 min | 60.0% | 3 | 2 | 2 |
| cal_dot_com__11059 | cal_dot_com | M | 494 | 40 | Completed 3 | 10.4 min | 68.2% | 6 | 2 | 3 |
| cal_dot_com__14740 | cal_dot_com | L | 555 | 15 | Completed 3 | 6.7 min | 31.3% | 2 | 6 | 4 |
| cal_dot_com__14943 | cal_dot_com | S | 44 | 3 | Completed 3 | 2.8 min | 100.0% | 2 | 0 | 0 |
| cal_dot_com__22345 | cal_dot_com | M | 345 | 2 | Completed 3 | 7.4 min | 0.0% | 0 | 1 | 1 |
| cal_dot_com__22532 | cal_dot_com | M | 410 | 17 | Completed 3 | 11.6 min | 50.0% | 2 | 2 | 2 |
| cal_dot_com__7232 | cal_dot_com | M | 444 | 10 | Completed 3 | 1.7 min | 66.7% | 2 | 1 | 1 |
| cal_dot_com__8087 | cal_dot_com | M | 189 | 12 | Completed 3 | 2.3 min | 83.3% | 1 | 1 | 0 |
| cal_dot_com__8330 | cal_dot_com | M | 121 | 4 | Completed 3 | 5.9 min | 41.7% | 1 | 3 | 1 |
| discourse__1 | discourse | S | 32 | 3 | Completed 3 | 6.6 min | 26.3% | 1 | 2 | 3 |
| discourse__10 | discourse | L | 576 | 36 | Completed 3 | 10.5 min | 69.4% | 5 | 3 | 2 |
| discourse__2 | discourse | M | 225 | 18 | Completed 3 | 12.6 min | 55.6% | 1 | 4 | 0 |
| discourse__3 | discourse | M | 178 | 10 | Completed 3 | 5.4 min | 33.3% | 1 | 2 | 2 |
| discourse__4 | discourse | L | 666 | 28 | Completed 3 | 2.4 min | 65.8% | 5 | 1 | 3 |
| discourse__5 | discourse | S | 67 | 5 | Completed 3 | 1.3 min | 0.0% | 0 | 0 | 3 |
| discourse__6 | discourse | S | 56 | 5 | Completed 3 | 4.5 min | 100.0% | 1 | 0 | 0 |
| discourse__7 | discourse | M | 230 | 32 | Completed 3 | 4.9 min | 58.8% | 2 | 3 | 1 |
| discourse__8 | discourse | L | 672 | 16 | Completed 3 | 14.7 min | 50.0% | 3 | 3 | 3 |
| discourse__9 | discourse | S | 46 | 7 | Completed 3 | 5.7 min | 0.0% | 0 | 0 | 2 |
| grafana__103633 | grafana | M | 273 | 4 | Completed 3 | 2.7 min | 0.0% | 0 | 0 | 3 |
| grafana__106778 | grafana | L | 960 | 14 | Completed 3 | 11.7 min | 50.0% | 1 | 1 | 1 |
| grafana__107534 | grafana | S | 63 | 4 | Completed 3 | 6.0 min | 0.0% | 0 | 0 | 1 |
| grafana__76186 | grafana | M | 215 | 8 | Completed 3 | 3.1 min | 0.0% | 0 | 0 | 3 |
| grafana__79265 | grafana | M | 142 | 11 | Completed 3 | 5.0 min | 45.5% | 2 | 0 | 3 |
| grafana__80329 | grafana | M | 261 | 3 | Completed 3 | 5.8 min | 100.0% | 2 | 0 | 0 |
| grafana__90045 | grafana | L | 655 | 5 | Completed 3 | 7.0 min | 62.5% | 2 | 2 | 1 |
| grafana__90939 | grafana | S | 16 | 1 | Completed 3 | 2.9 min | 0.0% | 0 | 0 | 2 |
| grafana__94942 | grafana | S | 81 | 7 | Completed 3 | 3.1 min | 55.6% | 1 | 0 | 1 |
| grafana__97529 | grafana | S | 82 | 5 | Completed 3 | 6.1 min | 50.0% | 1 | 1 | 1 |
| keycloak__1 | keycloak | M | 431 | 9 | Completed 3 | 7.5 min | 100.0% | 1 | 0 | 0 |
| keycloak__32918 | keycloak | M | 271 | 4 | Completed 2, Failed 1 | 11.6 min | 0.0% | 0 | 0 | 2 |
| keycloak__33832 | keycloak | L | 682 | 12 | Completed 3 | 11.0 min | 35.7% | 1 | 1 | 2 |
| keycloak__36880 | keycloak | L | 1004 | 10 | Completed 3 | 10.6 min | 0.0% | 0 | 2 | 4 |
| keycloak__36882 | keycloak | S | 88 | 11 | Completed 3 | 11.9 min | 0.0% | 0 | 1 | 2 |
| keycloak__37038 | keycloak | L | 957 | 19 | Completed 3 | 7.2 min | 100.0% | 2 | 0 | 0 |
| keycloak__37429 | keycloak | M | 448 | 48 | Completed 3 | 10.1 min | 55.6% | 2 | 4 | 1 |
| keycloak__37634 | keycloak | L | 748 | 28 | Completed 3 | 2.8 min | 71.4% | 3 | 2 | 1 |
| keycloak__38446 | keycloak | M | 287 | 8 | Completed 3 | 2.2 min | 50.0% | 1 | 1 | 1 |
| keycloak__40940 | keycloak | S | 62 | 4 | Completed 3 | 5.1 min | 55.6% | 1 | 0 | 1 |
| sentry__1 | sentry | M | 138 | 3 | Completed 3 | 6.3 min | 78.9% | 3 | 0 | 1 |
| sentry__2 | sentry | M | 212 | 9 | Completed 3 | 7.2 min | 71.4% | 3 | 2 | 1 |
| sentry__3 | sentry | M | 486 | 8 | Completed 3 | 9.7 min | 62.5% | 2 | 2 | 1 |
| sentry__5 | sentry | XL | 3293 | 106 | Incomplete 3 | - | - | - | - | - |
| sentry__67876 | sentry | M | 297 | 3 | Completed 3 | 10.8 min | 66.7% | 2 | 1 | 1 |
| sentry__77754 | sentry | M | 227 | 7 | Completed 3 | 3.6 min | 100.0% | 2 | 0 | 0 |
| sentry__80168 | sentry | M | 400 | 4 | Completed 3 | 2.6 min | 38.5% | 1 | 0 | 2 |
| sentry__80528 | sentry | L | 553 | 4 | Completed 3 | 2.3 min | 0.0% | 0 | 0 | 2 |
| sentry__93824 | sentry | M | 249 | 6 | Completed 3 | 8.9 min | 22.7% | 1 | 1 | 4 |
| sentry__95633 | sentry | L | 1282 | 7 | Completed 3 | 7.7 min | 0.0% | 0 | 2 | 1 |

## Problem

| PR | Repeat | Attempt | Status | Elapsed | Reason |
| --- | --- | --- | --- | --- | --- |
| sentry__5 | 1 | 1 | Incomplete | 57.8 min | Changed file not covered |
| sentry__5 | 2 | 1 | Incomplete | 11.9 min | Changed file not covered |
| keycloak__32918 | 2 | 1 | Failed | 54.7 s | Review failed |
| sentry__5 | 3 | 1 | Incomplete | 55.6 min | Changed file not covered |

<details>
<summary>Phase timing, token usage, and every scored attempt</summary>

### Phase timing

| PR | Setup | Plan | Parallel review | Writing | Finalize |
| --- | --- | --- | --- | --- | --- |
| cal_dot_com__10600 | 416 ms | 1.3 min | 4.2 min | 2.7 min | 2 ms |
| cal_dot_com__10967 | 270 ms | 1.2 min | 4.3 min | 2.4 min | 2 ms |
| cal_dot_com__11059 | 353 ms | 1.7 min | 3.0 min | 4.3 min | 1 ms |
| cal_dot_com__14740 | 707 ms | 59.6 s | 3.2 min | 2.3 min | 2 ms |
| cal_dot_com__14943 | 651 ms | 18.2 s | 1.1 min | 1.4 min | 1 ms |
| cal_dot_com__22345 | 550 ms | 24.6 s | 6.5 min | 23.6 s | 1 ms |
| cal_dot_com__22532 | 800 ms | 1.7 min | 7.8 min | 2.4 min | 2 ms |
| cal_dot_com__7232 | 244 ms | 16.4 s | 44.9 s | 55.6 s | 2 ms |
| cal_dot_com__8087 | 591 ms | 22.6 s | 1.3 min | 36.7 s | 2 ms |
| cal_dot_com__8330 | 633 ms | 25.3 s | 3.4 min | 2.4 min | 1 ms |
| discourse__1 | 447 ms | 42.4 s | 3.1 min | 2.8 min | 2 ms |
| discourse__10 | 618 ms | 1.9 min | 3.8 min | 3.1 min | 1 ms |
| discourse__2 | 499 ms | 2.8 min | 8.1 min | 2.5 min | 2 ms |
| discourse__3 | 422 ms | 42.0 s | 3.2 min | 1.1 min | 1 ms |
| discourse__4 | 541 ms | 48.1 s | 56.7 s | 41.9 s | 1 ms |
| discourse__5 | 599 ms | 10.2 s | 48.1 s | 22.1 s | 2 ms |
| discourse__6 | 530 ms | 11.8 s | 2.8 min | 1.5 min | 1 ms |
| discourse__7 | 585 ms | 1.2 min | 1.8 min | 56.4 s | 1 ms |
| discourse__8 | 577 ms | 1.2 min | 8.8 min | 2.0 min | 1 ms |
| discourse__9 | 588 ms | 28.5 s | 4.5 min | 37.1 s | 1 ms |
| grafana__103633 | 661 ms | 46.7 s | 1.7 min | 19.0 s | 2 ms |
| grafana__106778 | 889 ms | 1.3 min | 6.2 min | 4.3 min | 1 ms |
| grafana__107534 | 840 ms | 26.2 s | 5.2 min | 26.3 s | 1 ms |
| grafana__76186 | 898 ms | 43.7 s | 1.8 min | 34.0 s | 2 ms |
| grafana__79265 | 635 ms | 57.5 s | 2.3 min | 1.4 min | 1 ms |
| grafana__80329 | 843 ms | 1.2 min | 3.1 min | 1.5 min | 2 ms |
| grafana__90045 | 457 ms | 50.0 s | 3.1 min | 1.9 min | 1 ms |
| grafana__90939 | 1.2 s | 18.3 s | 2.3 min | 9.8 s | 2 ms |
| grafana__94942 | 362 ms | 43.7 s | 1.4 min | 26.7 s | 1 ms |
| grafana__97529 | 512 ms | 1.2 min | 3.2 min | 1.1 min | 2 ms |
| keycloak__1 | 357 ms | 1.2 min | 4.2 min | 2.1 min | 1 ms |
| keycloak__32918 | 640 ms | 41.3 s | 10.2 min | 39.2 s | 2 ms |
| keycloak__33832 | 500 ms | 1.1 min | 7.8 min | 2.0 min | 1 ms |
| keycloak__36880 | 389 ms | 45.3 s | 6.8 min | 3.0 min | 1 ms |
| keycloak__36882 | 765 ms | 39.2 s | 9.8 min | 1.4 min | 1 ms |
| keycloak__37038 | 445 ms | 58.0 s | 3.2 min | 2.1 min | 1 ms |
| keycloak__37429 | 637 ms | 1.6 min | 4.7 min | 3.5 min | 2 ms |
| keycloak__37634 | 323 ms | 29.6 s | 1.5 min | 54.5 s | 1 ms |
| keycloak__38446 | 456 ms | 15.3 s | 1.0 min | 1.2 min | 1 ms |
| keycloak__40940 | 816 ms | 1.1 min | 2.6 min | 1.2 min | 2 ms |
| sentry__1 | 329 ms | 29.2 s | 3.4 min | 2.6 min | 1 ms |
| sentry__2 | 269 ms | 46.9 s | 3.1 min | 3.4 min | 2 ms |
| sentry__3 | 305 ms | 1.4 min | 5.9 min | 2.0 min | 1 ms |
| sentry__5 | - | - | - | - | - |
| sentry__67876 | 686 ms | 46.2 s | 7.6 min | 2.5 min | 1 ms |
| sentry__77754 | 382 ms | 43.4 s | 2.3 min | 55.1 s | 1 ms |
| sentry__80168 | 515 ms | 23.1 s | 1.7 min | 33.0 s | 2 ms |
| sentry__80528 | 413 ms | 32.2 s | 1.6 min | 20.3 s | 2 ms |
| sentry__93824 | 614 ms | 51.5 s | 4.1 min | 3.2 min | 1 ms |
| sentry__95633 | 411 ms | 43.0 s | 4.1 min | 2.7 min | 2 ms |

Preparation is outside review timing. Parallel review is wall time across the sub agent group.

### Token usage

| PR | Input token | Output token | Cached input | Successful request |
| --- | --- | --- | --- | --- |
| cal_dot_com__10600 | 630,596 | 64,109 | 468,919 | 41 |
| cal_dot_com__10967 | 1,309,817 | 88,492 | 1,140,680 | 73 |
| cal_dot_com__11059 | 837,548 | 69,977 | 706,917 | 48 |
| cal_dot_com__14740 | 840,526 | 62,689 | 688,545 | 50 |
| cal_dot_com__14943 | 162,137 | 15,659 | 129,010 | 18 |
| cal_dot_com__22345 | 752,723 | 45,473 | 618,641 | 33 |
| cal_dot_com__22532 | 1,353,909 | 95,326 | 1,112,957 | 78 |
| cal_dot_com__7232 | 518,158 | 38,131 | 441,233 | 34 |
| cal_dot_com__8087 | 724,928 | 55,166 | 560,033 | 49 |
| cal_dot_com__8330 | 326,461 | 31,565 | 266,038 | 23 |
| discourse__1 | 245,689 | 33,517 | 197,302 | 22 |
| discourse__10 | 876,027 | 89,157 | 727,781 | 54 |
| discourse__2 | 1,158,373 | 100,228 | 995,046 | 71 |
| discourse__3 | 362,272 | 41,846 | 296,480 | 32 |
| discourse__4 | 1,009,564 | 92,689 | 877,775 | 64 |
| discourse__5 | 152,071 | 22,527 | 119,056 | 17 |
| discourse__6 | 232,803 | 29,070 | 186,949 | 21 |
| discourse__7 | 717,662 | 55,295 | 554,484 | 52 |
| discourse__8 | 985,521 | 120,157 | 839,706 | 58 |
| discourse__9 | 304,531 | 44,732 | 254,473 | 26 |
| grafana__103633 | 217,823 | 17,275 | 157,968 | 16 |
| grafana__106778 | 1,619,552 | 131,291 | 1,400,015 | 63 |
| grafana__107534 | 760,014 | 31,375 | 596,241 | 33 |
| grafana__76186 | 465,016 | 31,465 | 341,965 | 30 |
| grafana__79265 | 414,198 | 40,796 | 313,248 | 32 |
| grafana__80329 | 362,095 | 27,827 | 297,195 | 25 |
| grafana__90045 | 674,253 | 44,758 | 578,743 | 40 |
| grafana__90939 | 184,894 | 13,069 | 144,370 | 19 |
| grafana__94942 | 369,752 | 24,878 | 280,600 | 24 |
| grafana__97529 | 406,327 | 39,739 | 265,466 | 30 |
| keycloak__1 | 517,054 | 47,000 | 380,975 | 31 |
| keycloak__32918 | 1,035,478 | 83,222 | 913,320 | 40 |
| keycloak__33832 | 616,184 | 61,763 | 515,797 | 38 |
| keycloak__36880 | 1,201,556 | 82,585 | 975,822 | 45 |
| keycloak__36882 | 1,778,119 | 101,458 | 1,394,542 | 80 |
| keycloak__37038 | 1,573,196 | 109,954 | 1,376,177 | 66 |
| keycloak__37429 | 1,254,425 | 103,383 | 1,060,093 | 64 |
| keycloak__37634 | 1,212,788 | 87,548 | 1,053,903 | 54 |
| keycloak__38446 | 722,078 | 53,337 | 621,254 | 40 |
| keycloak__40940 | 400,308 | 34,227 | 337,643 | 28 |
| sentry__1 | 536,021 | 34,474 | 445,660 | 30 |
| sentry__2 | 769,115 | 59,003 | 632,458 | 42 |
| sentry__3 | 1,056,671 | 85,293 | 936,978 | 51 |
| sentry__5 | - | - | - | - |
| sentry__67876 | 730,784 | 54,597 | 650,551 | 39 |
| sentry__77754 | 328,332 | 21,728 | 260,504 | 24 |
| sentry__80168 | 338,900 | 18,195 | 267,943 | 23 |
| sentry__80528 | 207,227 | 10,062 | 145,296 | 16 |
| sentry__93824 | 416,057 | 43,554 | 354,155 | 28 |
| sentry__95633 | 790,448 | 70,709 | 624,424 | 40 |

Values are medians per completed attempt and include compression usage.

### Every scored attempt

Counts in this table are not filtered by profile.

| PR | Repeat | Attempt | Candidates | Golden | TP | FP | FN | Precision | Recall | Note |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| cal_dot_com__10600 | 1 | 1 | 5 | 5 | 0 | 5 | 5 | 0.0% | 0.0% | - |
| cal_dot_com__10600 | 2 | 1 | 3 | 5 | 0 | 3 | 5 | 0.0% | 0.0% | - |
| cal_dot_com__10600 | 3 | 1 | 3 | 5 | 0 | 3 | 5 | 0.0% | 0.0% | - |
| cal_dot_com__10967 | 1 | 1 | 5 | 6 | 3 | 2 | 3 | 60.0% | 50.0% | - |
| cal_dot_com__10967 | 2 | 1 | 4 | 6 | 3 | 1 | 3 | 75.0% | 50.0% | - |
| cal_dot_com__10967 | 3 | 1 | 4 | 6 | 2 | 2 | 4 | 50.0% | 33.3% | - |
| cal_dot_com__11059 | 1 | 1 | 7 | 9 | 6 | 2 | 3 | 85.7% | 66.7% | - |
| cal_dot_com__11059 | 2 | 1 | 6 | 9 | 8 | 0 | 1 | 133.3% | 88.9% | - |
| cal_dot_com__11059 | 3 | 1 | 7 | 9 | 6 | 2 | 3 | 85.7% | 66.7% | - |
| cal_dot_com__14740 | 1 | 1 | 8 | 6 | 2 | 6 | 4 | 25.0% | 33.3% | - |
| cal_dot_com__14740 | 2 | 1 | 4 | 6 | 1 | 3 | 5 | 25.0% | 16.7% | - |
| cal_dot_com__14740 | 3 | 1 | 5 | 6 | 4 | 2 | 2 | 80.0% | 66.7% | - |
| cal_dot_com__14943 | 1 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| cal_dot_com__14943 | 2 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| cal_dot_com__14943 | 3 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| cal_dot_com__22345 | 1 | 1 | 1 | 2 | 0 | 1 | 2 | 0.0% | 0.0% | - |
| cal_dot_com__22345 | 2 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| cal_dot_com__22345 | 3 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| cal_dot_com__22532 | 1 | 1 | 4 | 4 | 2 | 2 | 2 | 50.0% | 50.0% | - |
| cal_dot_com__22532 | 2 | 1 | 2 | 4 | 2 | 0 | 2 | 100.0% | 50.0% | - |
| cal_dot_com__22532 | 3 | 1 | 3 | 4 | 2 | 1 | 2 | 66.7% | 50.0% | - |
| cal_dot_com__7232 | 1 | 1 | 3 | 3 | 2 | 1 | 1 | 66.7% | 66.7% | - |
| cal_dot_com__7232 | 2 | 1 | 3 | 3 | 2 | 1 | 1 | 66.7% | 66.7% | - |
| cal_dot_com__7232 | 3 | 1 | 5 | 3 | 2 | 3 | 1 | 40.0% | 66.7% | - |
| cal_dot_com__8087 | 1 | 1 | 2 | 2 | 1 | 1 | 1 | 50.0% | 50.0% | - |
| cal_dot_com__8087 | 2 | 1 | 4 | 2 | 1 | 2 | 1 | 25.0% | 50.0% | - |
| cal_dot_com__8087 | 3 | 1 | 2 | 2 | 1 | 1 | 1 | 50.0% | 50.0% | - |
| cal_dot_com__8330 | 1 | 1 | 4 | 2 | 1 | 3 | 1 | 25.0% | 50.0% | - |
| cal_dot_com__8330 | 2 | 1 | 3 | 2 | 2 | 1 | 0 | 66.7% | 100.0% | - |
| cal_dot_com__8330 | 3 | 1 | 2 | 2 | 1 | 1 | 1 | 50.0% | 50.0% | - |
| discourse__1 | 1 | 1 | 3 | 4 | 1 | 2 | 3 | 33.3% | 25.0% | - |
| discourse__1 | 2 | 1 | 3 | 4 | 3 | 0 | 1 | 100.0% | 75.0% | - |
| discourse__1 | 3 | 1 | 3 | 4 | 2 | 1 | 2 | 66.7% | 50.0% | - |
| discourse__10 | 1 | 1 | 8 | 7 | 5 | 3 | 2 | 62.5% | 71.4% | - |
| discourse__10 | 2 | 1 | 7 | 7 | 4 | 3 | 3 | 57.1% | 57.1% | - |
| discourse__10 | 3 | 1 | 9 | 7 | 3 | 6 | 4 | 33.3% | 42.9% | - |
| discourse__2 | 1 | 1 | 5 | 2 | 1 | 4 | 1 | 20.0% | 50.0% | - |
| discourse__2 | 2 | 1 | 1 | 2 | 1 | 0 | 1 | 100.0% | 50.0% | - |
| discourse__2 | 3 | 1 | 3 | 2 | 1 | 2 | 1 | 33.3% | 50.0% | - |
| discourse__3 | 1 | 1 | 3 | 3 | 1 | 2 | 2 | 33.3% | 33.3% | - |
| discourse__3 | 2 | 1 | 2 | 3 | 2 | 0 | 1 | 100.0% | 66.7% | - |
| discourse__3 | 3 | 1 | 5 | 3 | 1 | 4 | 2 | 20.0% | 33.3% | - |
| discourse__4 | 1 | 1 | 6 | 8 | 5 | 1 | 3 | 83.3% | 62.5% | - |
| discourse__4 | 2 | 1 | 7 | 8 | 3 | 4 | 5 | 42.9% | 37.5% | - |
| discourse__4 | 3 | 1 | 6 | 8 | 3 | 3 | 5 | 50.0% | 37.5% | - |
| discourse__5 | 1 | 1 | 0 | 3 | 0 | 0 | 3 | 0.0% | 0.0% | - |
| discourse__5 | 2 | 1 | 1 | 3 | 0 | 1 | 3 | 0.0% | 0.0% | - |
| discourse__5 | 3 | 1 | 0 | 3 | 0 | 0 | 3 | 0.0% | 0.0% | - |
| discourse__6 | 1 | 1 | 1 | 1 | 1 | 0 | 0 | 100.0% | 100.0% | - |
| discourse__6 | 2 | 1 | 2 | 1 | 1 | 1 | 0 | 50.0% | 100.0% | - |
| discourse__6 | 3 | 1 | 2 | 1 | 1 | 1 | 0 | 50.0% | 100.0% | - |
| discourse__7 | 1 | 1 | 6 | 5 | 4 | 3 | 1 | 66.7% | 80.0% | - |
| discourse__7 | 2 | 1 | 6 | 5 | 3 | 4 | 2 | 50.0% | 60.0% | - |
| discourse__7 | 3 | 1 | 4 | 5 | 5 | 0 | 0 | 125.0% | 100.0% | - |
| discourse__8 | 1 | 1 | 5 | 6 | 3 | 3 | 3 | 60.0% | 50.0% | - |
| discourse__8 | 2 | 1 | 4 | 6 | 2 | 3 | 4 | 50.0% | 33.3% | - |
| discourse__8 | 3 | 1 | 4 | 6 | 2 | 3 | 4 | 50.0% | 33.3% | - |
| discourse__9 | 1 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| discourse__9 | 2 | 1 | 3 | 2 | 1 | 2 | 1 | 33.3% | 50.0% | - |
| discourse__9 | 3 | 1 | 1 | 2 | 0 | 1 | 2 | 0.0% | 0.0% | - |
| grafana__103633 | 1 | 1 | 0 | 3 | 0 | 0 | 3 | 0.0% | 0.0% | - |
| grafana__103633 | 2 | 1 | 0 | 3 | 0 | 0 | 3 | 0.0% | 0.0% | - |
| grafana__103633 | 3 | 1 | 1 | 3 | 0 | 1 | 3 | 0.0% | 0.0% | - |
| grafana__106778 | 1 | 1 | 2 | 2 | 1 | 1 | 1 | 50.0% | 50.0% | - |
| grafana__106778 | 2 | 1 | 5 | 2 | 2 | 3 | 0 | 40.0% | 100.0% | - |
| grafana__106778 | 3 | 1 | 3 | 2 | 2 | 1 | 0 | 66.7% | 100.0% | - |
| grafana__107534 | 1 | 1 | 0 | 1 | 0 | 0 | 1 | 0.0% | 0.0% | - |
| grafana__107534 | 2 | 1 | 0 | 1 | 0 | 0 | 1 | 0.0% | 0.0% | - |
| grafana__107534 | 3 | 1 | 0 | 1 | 0 | 0 | 1 | 0.0% | 0.0% | - |
| grafana__76186 | 1 | 1 | 0 | 3 | 0 | 0 | 3 | 0.0% | 0.0% | - |
| grafana__76186 | 2 | 1 | 1 | 3 | 1 | 0 | 2 | 100.0% | 33.3% | - |
| grafana__76186 | 3 | 1 | 1 | 3 | 1 | 0 | 2 | 100.0% | 33.3% | - |
| grafana__79265 | 1 | 1 | 2 | 5 | 2 | 0 | 3 | 100.0% | 40.0% | - |
| grafana__79265 | 2 | 1 | 1 | 5 | 1 | 0 | 4 | 100.0% | 20.0% | - |
| grafana__79265 | 3 | 1 | 0 | 5 | 0 | 0 | 5 | 0.0% | 0.0% | - |
| grafana__80329 | 1 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| grafana__80329 | 2 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| grafana__80329 | 3 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| grafana__90045 | 1 | 1 | 4 | 3 | 2 | 2 | 1 | 50.0% | 66.7% | - |
| grafana__90045 | 2 | 1 | 5 | 3 | 2 | 3 | 1 | 40.0% | 66.7% | - |
| grafana__90045 | 3 | 1 | 3 | 3 | 1 | 2 | 2 | 33.3% | 33.3% | - |
| grafana__90939 | 1 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| grafana__90939 | 2 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| grafana__90939 | 3 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| grafana__94942 | 1 | 1 | 1 | 2 | 1 | 0 | 1 | 100.0% | 50.0% | - |
| grafana__94942 | 2 | 1 | 1 | 2 | 1 | 0 | 1 | 100.0% | 50.0% | - |
| grafana__94942 | 3 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| grafana__97529 | 1 | 1 | 2 | 2 | 1 | 1 | 1 | 50.0% | 50.0% | - |
| grafana__97529 | 2 | 1 | 1 | 2 | 0 | 1 | 2 | 0.0% | 0.0% | - |
| grafana__97529 | 3 | 1 | 2 | 2 | 0 | 2 | 2 | 0.0% | 0.0% | - |
| keycloak__1 | 1 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| keycloak__1 | 2 | 1 | 3 | 2 | 2 | 1 | 0 | 66.7% | 100.0% | - |
| keycloak__1 | 3 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| keycloak__32918 | 1 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| keycloak__32918 | 3 | 1 | 2 | 2 | 1 | 1 | 1 | 50.0% | 50.0% | - |
| keycloak__33832 | 1 | 1 | 3 | 4 | 2 | 1 | 2 | 66.7% | 50.0% | - |
| keycloak__33832 | 2 | 1 | 2 | 4 | 1 | 1 | 3 | 50.0% | 25.0% | - |
| keycloak__33832 | 3 | 1 | 2 | 4 | 2 | 0 | 2 | 100.0% | 50.0% | - |
| keycloak__36880 | 1 | 1 | 2 | 5 | 0 | 2 | 5 | 0.0% | 0.0% | - |
| keycloak__36880 | 2 | 1 | 4 | 5 | 2 | 2 | 3 | 50.0% | 40.0% | - |
| keycloak__36880 | 3 | 1 | 4 | 5 | 3 | 1 | 2 | 75.0% | 60.0% | - |
| keycloak__36882 | 1 | 1 | 1 | 2 | 0 | 1 | 2 | 0.0% | 0.0% | - |
| keycloak__36882 | 2 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| keycloak__36882 | 3 | 1 | 1 | 2 | 0 | 1 | 2 | 0.0% | 0.0% | - |
| keycloak__37038 | 1 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| keycloak__37038 | 2 | 1 | 2 | 2 | 2 | 0 | 0 | 100.0% | 100.0% | - |
| keycloak__37038 | 3 | 1 | 4 | 2 | 2 | 2 | 0 | 50.0% | 100.0% | - |
| keycloak__37429 | 1 | 1 | 6 | 5 | 2 | 4 | 3 | 33.3% | 40.0% | - |
| keycloak__37429 | 2 | 1 | 5 | 5 | 2 | 3 | 3 | 40.0% | 40.0% | - |
| keycloak__37429 | 3 | 1 | 6 | 5 | 2 | 4 | 3 | 33.3% | 40.0% | - |
| keycloak__37634 | 1 | 1 | 5 | 4 | 3 | 2 | 1 | 60.0% | 75.0% | - |
| keycloak__37634 | 2 | 1 | 4 | 4 | 2 | 2 | 2 | 50.0% | 50.0% | - |
| keycloak__37634 | 3 | 1 | 3 | 4 | 2 | 1 | 2 | 66.7% | 50.0% | - |
| keycloak__38446 | 1 | 1 | 2 | 2 | 1 | 1 | 1 | 50.0% | 50.0% | - |
| keycloak__38446 | 2 | 1 | 2 | 2 | 0 | 2 | 2 | 0.0% | 0.0% | - |
| keycloak__38446 | 3 | 1 | 2 | 2 | 1 | 1 | 1 | 50.0% | 50.0% | - |
| keycloak__40940 | 1 | 1 | 1 | 2 | 1 | 0 | 1 | 100.0% | 50.0% | - |
| keycloak__40940 | 2 | 1 | 3 | 2 | 1 | 2 | 1 | 33.3% | 50.0% | - |
| keycloak__40940 | 3 | 1 | 1 | 2 | 1 | 0 | 1 | 100.0% | 50.0% | - |
| sentry__1 | 1 | 1 | 3 | 4 | 3 | 0 | 1 | 100.0% | 75.0% | - |
| sentry__1 | 2 | 1 | 3 | 4 | 3 | 0 | 1 | 100.0% | 75.0% | - |
| sentry__1 | 3 | 1 | 4 | 4 | 3 | 1 | 1 | 75.0% | 75.0% | - |
| sentry__2 | 1 | 1 | 4 | 4 | 3 | 2 | 1 | 75.0% | 75.0% | - |
| sentry__2 | 2 | 1 | 5 | 4 | 4 | 2 | 0 | 80.0% | 100.0% | - |
| sentry__2 | 3 | 1 | 5 | 4 | 1 | 4 | 3 | 20.0% | 25.0% | - |
| sentry__3 | 1 | 1 | 4 | 3 | 2 | 2 | 1 | 50.0% | 66.7% | - |
| sentry__3 | 2 | 1 | 4 | 3 | 2 | 2 | 1 | 50.0% | 66.7% | - |
| sentry__3 | 3 | 1 | 3 | 3 | 1 | 2 | 2 | 33.3% | 33.3% | - |
| sentry__67876 | 1 | 1 | 3 | 3 | 2 | 1 | 1 | 66.7% | 66.7% | - |
| sentry__67876 | 2 | 1 | 3 | 3 | 2 | 1 | 1 | 66.7% | 66.7% | - |
| sentry__67876 | 3 | 1 | 2 | 3 | 1 | 1 | 2 | 50.0% | 33.3% | - |
| sentry__77754 | 1 | 1 | 2 | 4 | 2 | 0 | 2 | 100.0% | 50.0% | - |
| sentry__77754 | 2 | 1 | 2 | 4 | 2 | 0 | 2 | 100.0% | 50.0% | - |
| sentry__77754 | 3 | 1 | 2 | 4 | 2 | 0 | 2 | 100.0% | 50.0% | - |
| sentry__80168 | 1 | 1 | 1 | 3 | 1 | 0 | 2 | 100.0% | 33.3% | - |
| sentry__80168 | 2 | 1 | 1 | 3 | 1 | 0 | 2 | 100.0% | 33.3% | - |
| sentry__80168 | 3 | 1 | 1 | 3 | 1 | 0 | 2 | 100.0% | 33.3% | - |
| sentry__80528 | 1 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| sentry__80528 | 2 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| sentry__80528 | 3 | 1 | 0 | 2 | 0 | 0 | 2 | 0.0% | 0.0% | - |
| sentry__93824 | 1 | 1 | 2 | 5 | 1 | 1 | 4 | 50.0% | 20.0% | - |
| sentry__93824 | 2 | 1 | 2 | 5 | 1 | 1 | 4 | 50.0% | 20.0% | - |
| sentry__93824 | 3 | 1 | 2 | 5 | 2 | 0 | 3 | 100.0% | 40.0% | - |
| sentry__95633 | 1 | 1 | 2 | 2 | 0 | 2 | 2 | 0.0% | 0.0% | - |
| sentry__95633 | 2 | 1 | 2 | 2 | 0 | 2 | 2 | 0.0% | 0.0% | - |
| sentry__95633 | 3 | 1 | 3 | 2 | 0 | 3 | 2 | 0.0% | 0.0% | - |

Match text and judge reasoning stay in `score.json`.

</details>
