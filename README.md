# On-the-Worst-Prompt-Performance-of-LLMs

## Introduction
We introduce a new benchmark, **RobustAlpacaEval**, that encompasses semantically equivalent queries of diverse real-world tasks, offering a more holistic assessment compared to existing benchmarks that focus solely on rephrasing task-level instructions.

RobustAlpacaEval is based on [TinyAlpaceEval](https://github.com/felipemaiapolo/tinyBenchmarks), which is a condensed subset of the [AlpacaEval](https://github.com/tatsu-lab/alpaca_eval) benchmark, created to enable efficient assessment of LLMs.  

We develop **RobustAlpacaEval** by creating ten paraphrases for each query within TinyAlpacaEval. To save manual efforts, this is first accomplished automatically through GPT4. Subsequently, each paraphrase is manually reviewed and revised to ensure semantic integrity and human-like fluency. We use carefully crafted prompts to promote the diversity of paraphrases, which is evidenced by the fact that the average of length-normalized edit distance (We compute the edit distance between prompts $x$ and $y$ normalized by their average length as: $\frac{2*EditDistance(x, y)}{(|x|+|y|)}$) between each pair of paraphrases is 0.7234 at the word level. 
