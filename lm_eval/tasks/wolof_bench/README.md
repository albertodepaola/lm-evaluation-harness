# WolofBench

### Paper

WolofBench is a benchmark for evaluating language models in Wolof tasks. This is, it evaluates the ability of a language model to understand and generate Wolof text. WolofBench offers a combination of pre-existing, open datasets.

The datasets included in WolofBench are:

| Task          | Category       | Paper title          | Homepage  |
|:-------------:|:-----:|:-------------:|:-----:|
| FLORES_es | Translation | [The FLORES-101  Evaluation Benchmark for Low-Resource and Multilingual Machine Translation](https://arxiv.org/abs/2106.03193) | https://huggingface.co/datasets/facebook/flores |


### Groups and Tasks

#### Groups

- `flores_wol`: English and French translation tasks from or to Wolof.

#### Tasks

The following tasks evaluate tasks on PortugueseBench dataset using various scoring methods.

  - `flores_wol`
  - `flores_wo-en`
  - `flores_wo-fr`
  - `flores_en-wo`
  - `flores_fr-wo`

### Running with accelerate

`accelerate launch -m lm_eval --model hf --model_args pretrained=<model_id> --tasks wolof_bench --output_path ./results/ --log_samples --write_out`

### Checklist

* [x] Is the task an existing benchmark in the literature?
  * [ ] Have you referenced the original paper that introduced the task?
  * [ ] If yes, does the original paper provide a reference implementation?
    * [ ] Yes, original implementation contributed by author of the benchmark

If other tasks on this dataset are already supported:
* [ ] Is the "Main" variant of this task clearly denoted?
* [ ] Have you provided a short sentence in a README on what each new variant adds / evaluates?
* [ ] Have you noted which, if any, published evaluation setups are matched by this variant?
