### Road map
- [ ] Scaled Dot Product Attention with customisable scaling. Steal from [torch F.scaled-dot-product-attention semi-source code](https://pytorch.org/docs/stable/generated/torch.nn.functional.scaled_dot_product_attention.html#torch.nn.functional.scaled_dot_product_attention). Then benchmark speed, weight importable, and attention map.
- [ ] ViT. Steal from [Timm Vision Transformer](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/vision_transformer.py). Again benchmark like above
- [ ] Swin. Steal from [Timm Swin](https://github.com/huggingface/pytorch-image-models/blob/main/timm/models/swin_transformer.py). Again benchmark like above
- [ ] RSBuilding. That model is built from backbone [Vision Transformer SAM from Open-CD](https://github.com/Meize0729/RSBuilding/blob/main/opencd/models/backbones/vit_sam_normal.py). From first impression, it looks like [Timm Vision Transformer SAM](https://github.com/Meize0729/RSBuilding/blob/main/opencd/models/backbones/vit_sam_normal.py) with couple extra functions.

