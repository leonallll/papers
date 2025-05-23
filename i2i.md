## SpuerEdit（202505，字节）

* paper：https://arxiv.org/abs/2505.02370
* code：https://github.com/bytedance/SuperEdit
* dataset：limingcv/SuperEdit-40K
* benchmark：Real-Edit
* contributions：
  * 只关注于提升训练数据的质量对于图像编辑模型的能力提升有多大：高质量的数据可以有效弥补模型结构的简单，与SmartEdit模型相比，性能提升9.19%，训练数据小30倍，参数量小13倍
  * 使用VLMs来引导编辑指令，更好的与图像对对齐
  * 无论是编辑模型还是生成模型，不同的推理阶段对应生成图像的不同属性，与文本无关，(比如，前10个step对应图像整体，中间20step对应图像局部，最后10step着重细节优化）

## ICEdit（202504，浙大&哈佛）

* paper：https://arxiv.org/abs/2504.20690
* project：https://github.com/River-Zhang/ICEdit
* models：https://huggingface.co/RiverZ/normal-lora/tree/main
* try：https://huggingface.co/spaces/RiverZ/ICEdit
* Instruction based Image Edit，仅需1%的可训练参数（200M）和0.1%的训练数据（50k），泛化能力强，能够处理各种编辑任务
* 处理但张图片约9s，4GB显存
*
