## Running the wolof bench

lm_eval --model hf --model_args pretrained=meta-llama/Llama-3.1-8B-Instruct --tasks wolof_bench --limit 10  --output_path ./results/ --log_samples --write_out --use_cache ./cache/sql_cache_

lm_eval --model hf --model_args pretrained=soynade-research/Oolel-v0.1 --tasks wolof_bench --limit 10  --output_path ./results/ --log_samples --write_out --use_cache ./cache/sql_cache_

## Running with accelerate

accelerate launch -m  lm_eval --model hf --model_args pretrained=soynade-research/Oolel-v0.1 --tasks wolof_bench  --output_path ./results/ --log_samples --write_out  --batch_size auto

accelerate launch -m lm_eval --model hf --model_args pretrained=meta-llama/Llama-3.3-70B-Instruct --tasks wolof_bench --limit 10  --output_path ./results/ --log_samples --write_out --batch_size auto
