# KoBERT-nsmc

- KcBERT를 이용한 네이버 영화 리뷰 감정 분석 (sentiment classification)
- 🤗`Huggingface Tranformers`🤗 라이브러리를 이용하여 구현

## Dependencies

- torch==1.5.1
- transformers~=3.0.1

## How to use KcBERT on Huggingface Transformers Library

```python
from transformers import AutoModel, AutoTokenizer

model = AutoModel.from_pretrained('beomi/kcbert-base')
tokenizer = AutoTokenizer.from_pretrained('beomi/kcbert-base')
```

## Usage

```bash
$ python3 main.py \
    --model_name_or_path beomi/kcbert-base \
    --do_train --do_eval \
    --max_seq_len 100
```

## Prediction

```bash
$ python3 predict.py --input_file {INPUT_FILE_PATH} --output_file {OUTPUT_FILE_PATH} --model_dir {SAVED_CKPT_PATH}
```

## Results


|                   | Accuracy (%) |
| ----------------- | ------------ |
| KcBERT            | **??.??**    |
| KoBERT            | 89.63        |
| DistilKoBERT      | 88.41        |
| Bert-Multilingual | 87.07        |
| FastText          | 85.50        |


## References

- [Monologg KoBERT for Transformers](https://github.com/monologg/KoBERT)
- [KoBERT](https://github.com/SKTBrain/KoBERT)
- [Huggingface Transformers](https://github.com/huggingface/transformers)
- [NSMC dataset](https://github.com/e9t/nsmc)
