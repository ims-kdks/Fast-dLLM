# Prefix cache + Parallel

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

# Prefix cache + delta DiT (cache 2 step) (2GPU)

Total number of tokens generated: 153817
Total time taken: 11025.921502113342 seconds
Tokens per second: 13.950489044189453
Total NFE is 168960
2025-07-18:04:38:02,482 INFO     [lm_eval.loggers.evaluation_tracker:272] Output path not provided, skipping saving results aggregated
llada_dist (model_path=GSAI-ML/LLaDA-8B-Instruct,gen_length=256,steps=256,block_length=32,use_cache=True,show_speed=True), gen_kwargs: (None), limit: None, num_fewshot: 5, batch_size: 1

|Tasks|Version|     Filter     |n-shot|  Metric   |   |Value |   |Stderr|
|-----|------:|----------------|-----:|-----------|---|-----:|---|-----:|
|gsm8k|      3|flexible-extract|     5|exact_match|↑  |0.7453|±  |0.0120|
|     |       |strict-match    |     5|exact_match|↑  |0.3897|±  |0.0134|

