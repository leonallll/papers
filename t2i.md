# 202504

## HiDream-I1——智象未来

* 模型：https://huggingface.co/HiDream-ai/HiDream-I1-Full
* 代码：https://github.com/HiDream-ai/HiDream-I1
* 评测指标：DPG-Bench & GenEval & HPSv2.1 benchmark
* 参数量：17B
* 三个版本：Full & Dev & Fast
* 结构：
  * 基于MoE的DiT架构
  * Flux开源的VAE
  * Flow Matching
  * 4个text encoder：OpenCLIP ViT-gibG & OpenAI CLIP VIT-L & T-XXL & Llama-3.1-8B-Instruct
* 体验：
  * 不同seed生成结果相似度很高
  * 支持最大分辨率768 * 1360，H100上的生成时间约为20s
  * prompt跟随不错
  * 特定中文场景生成能力有限（莫高窟之类）
