## FLUX.1 Kontext（202505，Black-Forest_lab)

* technical report: https://cdn.sanity.io/files/gsvmb6gz/production/880b072208997108f87e5d2729d8a8be481310b5.pdf
* Try Demo: https://playground.bfl.ai/image/edit
* 三个版本：
  * max（prompt跟随、排版、一致性）
  * pro （本地编辑、生成式的修改、准确定位修改区域、多轮修改）
  * dev（蒸馏版本，会开源）
* 既可以文生图又可以参考生图，还可以图像编辑
* 上下文生成，输入文本或图像，可连续修改
* 一致性很好，可进行局部编辑、风格转换

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

## Insert Anything（202504，浙江大学&哈佛大学&南洋理工大学）

* paper：https://arxiv.org/pdf/2504.15009
* project：https://song-wensong.github.io/insert-anything
* code：https://github.com/song-wensong/insert-anything
* 支持多种实际场景，包括艺术创作、逼真的脸部交换、电影场景构图、虚拟服装试穿、配饰定制和数字道具更换
* 使用二联图（mask 引导）或三联图（instruction引导）的方式，利用DiT的上下文一致遵循能力进行图像编辑

## Step1X-Edit（202504，

* paper：https://arxiv.org/abs/2504.17761
* code：https://github.com/stepfun-ai/Step1X-Edit?tab=readme-ov-file
*
