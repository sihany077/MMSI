# MMSI-Bench

## Environment Setup
conda create -n mmsi python=3.9 -y

conda activate mmsi

cd lmms-eval; pip install -e .


### Support: gpt-4o-2024-08-06, gpt-4.5-preview-2025-02-27, gpt-4.1-2025-04-14, gemini-2.5-pro-exp-03-25, gemini-2.5-pro-thinking, claude-3-7-sonnet-20250219, claude-3-7-sonnet-20250219-thinking ...
export OPENAI_COMPATIBLE_API_KEY=XXX
export OPENAI_COMPATIBLE_API_URL=XXX
lmms-eval --model openai_compatible --model_args model_version=gpt-4o-2024-08-06 --task msr_bench  --batch_size 1 --log_samples --log_samples_suffix gpt-4o-2024-08-06 --output_path ./logs



## For open-source models, set up the environment according to the instructions at: https://github.com/EvolvingLMMs-Lab/lmms-eval


CUDA_VISIBLE_DEVICES=0,1,2 lmms-eval --model qwen2_5_vl --model_args=pretrained="path_to/Qwen2.5-VL-72B-Instruct",max_pixels=12835456,min_pixels=1003520,use_flash_attention_2=False \
    --tasks msr_bench \
    --log_samples --log_samples_suffix Qwen2.5-VL-72B \
    --batch_size 1 \
    --output_path ./logs


