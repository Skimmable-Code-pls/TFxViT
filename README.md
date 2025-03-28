### Road map
At every step, benchmark my Tensorflow implementation against Timm and official Tensorflow's implementation (if available). For every 3 months, scroll down to the bottom [Timm benchmark](https://github.com/huggingface/pytorch-image-models/blob/main/results/benchmark-infer-fp32-nchw-pt221-cpu-i9_10940x-dynamo.csv) to lookout for modern backbone.
- [ ] Rewrite image processing in Tensorflow. See this [guide](https://discuss.huggingface.co/t/what-is-vitimageprocessor-doing/82132/4).
- [ ] Self-Attention. Steal from [Timm Multi-Heads Attention](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py#L58) but take considerations in design philosophy of [Tensorflow Multi-Heads Attention](https://github.com/tensorflow/models/blob/v2.18.0/official/vision/modeling/layers/nn_layers.py#L1286) wherever possible so that it fits model.compile in Tensorflow.
- [ ] ViT. Steal from [Timm Vision Transformer](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py). Benchmark my implementations against official versions in Timm and Tensorflow, respectively.
- [ ] Swin. Steal from [Timm Swin](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/swin_transformer.py).
- [ ] SAM. Steal from [Timm SAM](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer_sam.py#L736).

Experimental models:
- [ ] SwinV2. Steal from [Timm SwinV2](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/swin_transformer_v2.py). 
- [ ] SAM2. Steal from [Timm SAM2]([https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer_sam.py#L736](https://github.com/rwightman/timm/blob/main/timm/models/hieradet_sam2.py)).

Domain-specific experimentalal models:
- [ ] RSBuilding. That model is built from backbone [Vision Transformer SAM from Open-CD](https://github.com/Meize0729/RSBuilding/blob/main/opencd/models/backbones/vit_sam_normal.py). From first impression, it looks like [Timm Vision Transformer SAM](https://github.com/Meize0729/RSBuilding/blob/main/opencd/models/backbones/vit_sam_normal.py) with couple extra functions. 
