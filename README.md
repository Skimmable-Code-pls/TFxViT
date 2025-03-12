### Road map
- [ ] Scaled Dot Product Attention with customisable scaling. Steal from [torch F.scaled-dot-product-attention semi-source code](https://pytorch.org/docs/stable/generated/torch.nn.functional.scaled_dot_product_attention.html#torch.nn.functional.scaled_dot_product_attention). Then benchmark speed, weight importable, and attention map.
- [ ] Self-Attention.  Steal from [Timm Attention](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py#L58) but take considerations in design philosophy of [Keras Attention](https://github.com/keras-team/keras/blob/v3.3.3/keras/src/layers/attention/attention.py#L8) wherever possible. Benchmark like above against [Timm Attention](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py#L58) and [Keras Attention](https://github.com/keras-team/keras/blob/v3.3.3/keras/src/layers/attention/attention.py#L8).
- [ ] ViT. Steal from [Timm Vision Transformer](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py). Benchmark like above against [Timm Vision Transformer](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py) and [Keras Vision Transformer][https://github.com/faustomorales/vit-keras].
- [ ] ViT x [region compilation](https://pytorch.org/tutorials/recipes/regional_compilation.html) mostly by modifying line 559-575 in [Timm Vision Transformer](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py#L559). Can reduce execution time from 24s -> 2s.
- [ ] Swin. Steal from [Timm Swin](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/swin_transformer.py). Benchmark like above
- [ ] RSBuilding. That model is built from backbone [Vision Transformer SAM from Open-CD](https://github.com/Meize0729/RSBuilding/blob/main/opencd/models/backbones/vit_sam_normal.py). From first impression, it looks like [Timm Vision Transformer SAM](https://github.com/Meize0729/RSBuilding/blob/main/opencd/models/backbones/vit_sam_normal.py) with couple extra functions.

