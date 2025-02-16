# AAD-MLLM


## Checklist

What you can find in this repo:

- AAD-MLLM
  - training code
  - trained model checkpoints
- others
  - evaluation results for LLaVA-Video, LLaVA-OneVision


## AAD-MLLM

### Training

Following the instruction of [LLaVA](https://github.com/haotian-liu/LLaVA) to prepare the environment, data (`LLaVA-Video-178K`) and pretraining models (e.g., `LLaVA-video-7b`). 

Train the model with AAD-MLLM. 

```bash
cd LLaVA
bash scripts/train/dpo_video_2.sh
```
The main modifications to the original LLaVA code for AAD-MLLM are detailed in (`.LLaVA-NeXT/llava/train/train_dpo2.py`) and (`LLaVA-NeXT/scripts/train/dpo_video_2.sh`).

### Checkpoint

Our models finetuned with AAD-MLLM:

Basic Model | Checkpoint
 :- | :-
`llava-AAD-MLLM` |[llava-video-7b-AAD-MLLM](https://huggingface.co/HuggingDaChen/llava-1.5-7b-AAD-MLLM)



### Evaluation

We provide (`./LLaVA-NeXT/simple_test.py`) (`./LLaVA-NeXT/simple_test2.py`) (`./LLaVA-NeXT/simple_test3.py`) for evaluation.  


## Acknowledgement

This repo is built on [LLaVA-NeXT](https://github.com/LLaVA-VL/LLaVA-NeXT) (models). Many thanks for their efforts. The use of our code should also follow the original licenses.
