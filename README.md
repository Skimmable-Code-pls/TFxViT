### Road map
At every step, benchmark my Tensorflow implementation against Timm and official Tensorflow's implementation (if available). For every 3 months, scroll down to the bottom [Timm benchmark](https://github.com/huggingface/pytorch-image-models/blob/main/results/benchmark-infer-fp32-nchw-pt221-cpu-i9_10940x-dynamo.csv) to lookout for modern backbone.
- [ ] Self-Attention. Steal from [Timm Multi-Heads Attention](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py#L58) but take considerations in design philosophy of [Tensorflow Multi-Heads Attention](https://github.com/tensorflow/models/blob/v2.18.0/official/vision/modeling/layers/nn_layers.py#L1286) wherever possible. 
- [ ] ViT. Steal from [Timm Vision Transformer](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py). Benchmark my implementations against official versions in Timm and Tensorflow, respectively.
- [ ] Swin. Steal from [Timm Swin](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/swin_transformer.py). 
- [ ] SwinV2. Steal from [Timm SwinV2-Translated directly from Christopher original work](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/swin_transformer_v2_cr). Follow this code with caution for many FIXME issues to be fixed. For the [1st FIXME](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/swin_transformer_v2_cr.py#L114), the answer is embed_dim=192 from [official config](https://github.com/microsoft/Swin-Transformer/blob/main/configs/swinv2/swinv2_large_patch4_window12to24_192to384_22kto1k_ft.yaml). I'm not sure if [3rd FIXME](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/swin_transformer_v2_cr.py#L371-L374) is still an issue because it looks similar to [original version](https://github.com/microsoft/Swin-Transformer/blob/main/models/swin_transformer_v2.py#L280). In additions, [don't use "before padding" as pretrained SwinV2 wasn't trained with that on](https://github.com/huggingface/pytorch-image-models/issues/2438#issuecomment-2651749230).
- [ ] ViT-SAM. Steal from [Timm ViT-SAM](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer_sam.py#L736).
- [ ] RSBuilding. That model is built from backbone [Vision Transformer SAM from Open-CD](https://github.com/Meize0729/RSBuilding/blob/main/opencd/models/backbones/vit_sam_normal.py). From first impression, it looks like [Timm Vision Transformer SAM](https://github.com/Meize0729/RSBuilding/blob/main/opencd/models/backbones/vit_sam_normal.py) with couple extra functions. 
