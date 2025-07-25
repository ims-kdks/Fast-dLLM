# Prefix cache + Parallel (8 GPU)

Total number of tokens generated: 38490
Total time taken: 1299.71928191185 seconds
Tokens per second: 29.61408805847168
Total NFE is 13610
2025-07-13:03:06:21,568 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=8,block_length=32,use_cache=True,threshold=0.9,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

| Tasks | Version | Filter           | n-shot | Metric      |    |  Value |    | Stderr |
| ----- | ------: | ---------------- | -----: | ----------- | -- | -----: | -- | -----: |
| gsm8k |       3 | flexible-extract |      5 | exact_match | ↑ | 0.7832 | ± | 0.0114 |
|       |         | strict-match     |      5 | exact_match | ↑ | 0.3715 | ± | 0.0133 |

# Prefix cache + delta DiT (cache 6 step) (2 GPU)

Total number of tokens generated: 153723
Total time taken: 10197.139975309372 seconds
Tokens per second: 15.075109481811523
Total NFE is 168960
2025-07-17:05:05:09,149 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

| Tasks | Version | Filter           | n-shot | Metric      |    |  Value |    | Stderr |
| ----- | ------: | ---------------- | -----: | ----------- | -- | -----: | -- | -----: |
| gsm8k |       3 | flexible-extract |      5 | exact_match | ↑ | 0.6171 | ± | 0.0134 |
|       |         | strict-match     |      5 | exact_match | ↑ | 0.2919 | ± | 0.0125 |

# Prefix cache + delta DiT (cache 4 step) (2GPU)

**description**: only cache `mlp + attn` (equivenlent to delta of `x`)
Total number of tokens generated: 153213
Total time taken: 10296.591206073761 seconds
Tokens per second: 14.879973411560059
Total NFE is 168960
2025-07-18:01:27:31,194 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

| Tasks | Version | Filter           | n-shot | Metric      |    |  Value |    | Stderr |
| ----- | ------: | ---------------- | -----: | ----------- | -- | -----: | -- | -----: |
| gsm8k |       3 | flexible-extract |      5 | exact_match | ↑ | 0.6884 | ± | 0.0128 |
|       |         | strict-match     |      5 | exact_match | ↑ | 0.3503 | ± | 0.0131 |

# Prefix cache + delta DiT (cache 4 step, `attn`) (2GPU)

**description**: only cache entire `attn`
Total number of tokens generated: 152533
Total time taken: 11270.556265830994 seconds
Tokens per second: 13.533759117126465
Total NFE is 168960
2025-07-23:04:21:55,830 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

| Tasks | Version | Filter           | n-shot | Metric      |    |  Value |    | Stderr |
| ----- | ------: | ---------------- | -----: | ----------- | -- | -----: | -- | -----: |
| gsm8k |       3 | flexible-extract |      5 | exact_match | ↑ | 0.7225 | ± | 0.0123 |
|       |         | strict-match     |      5 | exact_match | ↑ | 0.3821 | ± | 0.0134 |

# Prefix cache + delta DiT (cache 4 step, `attn - x`) (2GPU)

**description**: only cache `attn - x` (delta of `attn`)
Total number of tokens generated: 174389
Total time taken: 11864.209438562393 seconds
Tokens per second: 14.698746681213379
Total NFE is 168960
2025-07-23:07:44:28,205 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

| Tasks | Version | Filter           | n-shot | Metric      |    |  Value |    | Stderr |
| ----- | ------: | ---------------- | -----: | ----------- | -- | -----: | -- | -----: |
| gsm8k |       3 | flexible-extract |      5 | exact_match | ↑ | 0.0136 | ± | 0.0032 |
|       |         | strict-match     |      5 | exact_match | ↑ | 0.0000 | ± | 0.0000 |

# Prefix cache + delta DiT (cache 4 step, `original_x - x`) (2GPU)

**description**: only cache `original_x - x` (true delta of `x`), the output is actually slightly different from `mlp + attn`
Total number of tokens generated: 152588
Total time taken: 10730.769718170166 seconds
Tokens per second: 14.219670295715332
Total NFE is 168960
2025-07-22:07:59:09,757 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

| Tasks | Version | Filter           | n-shot | Metric      |    |  Value |    | Stderr |
| ----- | ------: | ---------------- | -----: | ----------- | -- | -----: | -- | -----: |
| gsm8k |       3 | flexible-extract |      5 | exact_match | ↑ | 0.6801 | ± | 0.0128 |
|       |         | strict-match     |      5 | exact_match | ↑ | 0.3594 | ± | 0.0132 |

# Prefix cache + delta DiT (cache 4 step, `x`) (2GPU)

**description**: cache the entire output
Total number of tokens generated: 152613
Total time taken: 10617.774114608765 seconds
Tokens per second: 14.373351097106934
Total NFE is 168960
2025-07-23:17:24:44,276 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1
|Tasks|Version|     Filter     |n-shot|  Metric   |   |Value |   |Stderr|
|-----|------:|----------------|-----:|-----------|---|-----:|---|-----:|
|gsm8k|      3|flexible-extract|     5|exact_match|↑  |0.6808|±  |0.0128|
|     |       |strict-match    |     5|exact_match|↑  |0.3616|±  |0.0132|

# Prefix cache + delta DiT (cache 4 step, `attn`, only within block) (2GPU)

**description**: only cache entire `attn`, also cache only happens within each block, always do full computation at the begining of each block
Total number of tokens generated: 152513
Total time taken: 11391.031037330627 seconds
Tokens per second: 13.388866424560547
Total NFE is 168960
2025-07-24:16:20:31,446 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1
|Tasks|Version|     Filter     |n-shot|  Metric   |   |Value |   |Stderr|
|-----|------:|----------------|-----:|-----------|---|-----:|---|-----:|
|gsm8k|      3|flexible-extract|     5|exact_match|↑  |0.6990|±  |0.0126|
|     |       |strict-match    |     5|exact_match|↑  |0.3533|±  |0.0132|

# Prefix cache + delta DiT (cache 2 step) (2GPU)

Total number of tokens generated: 153817
Total time taken: 11025.921502113342 seconds
Tokens per second: 13.950489044189453
Total NFE is 168960
2025-07-18:04:38:02,482 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

| Tasks | Version | Filter           | n-shot | Metric      |    |  Value |    | Stderr |
| ----- | ------: | ---------------- | -----: | ----------- | -- | -----: | -- | -----: |
| gsm8k |       3 | flexible-extract |      5 | exact_match | ↑ | 0.7453 | ± | 0.0120 |
|       |         | strict-match     |      5 | exact_match | ↑ | 0.3897 | ± | 0.0134 |

# Prefix cache (2GPU)

Total number of tokens generated: 153706
Total time taken: 12639.665463209152 seconds
Tokens per second: 12.16060733795166
Total NFE is 168960
2025-07-19:06:29:23,797 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

| Tasks | Version | Filter           | n-shot | Metric      |    |  Value |    | Stderr |
| ----- | ------: | ---------------- | -----: | ----------- | -- | -----: | -- | -----: |
| gsm8k |       3 | flexible-extract |      5 | exact_match | ↑ | 0.7680 | ± | 0.0116 |
|       |         | strict-match     |      5 | exact_match | ↑ | 0.3609 | ± | 0.0132 |
