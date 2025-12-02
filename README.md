To train the model, some configuration should be as follows:
python "your path"/clevr_qwen2vl.py \
  --data_root "your path"/custom_dataset \
  --output_dir qwen2vl_clevr_e5_bs1_lr2e5 \
  --do_train \
  --epochs 5 \
  --batch_size 1 \
  --grad_accum 4 \
  --lr 2e-5 \
  --submission_path submission_e5_bs1_lr2e5_t01_ens5.csv \
  --ensemble_size 5 \
  --gen_max_new_tokens 128 \
  --gen_temperature 0.1 \
  --gen_top_p 0.8
