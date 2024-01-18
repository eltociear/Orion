<!-- markdownlint-disable first-line-h1 -->
<!-- markdownlint-disable html -->
![](./assets/imgs/orion_start.PNG)

<div align="center">
<h1>
  Orion-14B
</h1>
</div>

<p align="center">
🤗 <a href="https://huggingface.co/OrionStarAI/OrionStar-14B" target="_blank">HuggingFace 模型下载</a> |  🤖 <a href="https://modelscope.cn/models/OrionStarAI/Orion-14B/summary" target="_blank">ModelScope 模型下载</a>
</p>


<p align="center">
🤗 <a href="https://modelscope.cn/studios/OrionStarAI/Orion-14B/summary" target="_blank">💡在线Demo</a>
</p>


<div align="center">


<h4 align="center">
    <p>
        <b>中文</b> |
        <a href="https://github.com/OrionStarAI/Orion-14B/blob/main/README_en.MD">English</a>
    <p>
</h4>

</div>

# 目录

- [📖 模型介绍](#模型介绍)
- [🔗 下载路径](#下载路径)
- [🔖 评估结果](#评估结果)
- [📊 模型推理](#模型推理)
- [🥇 企业介绍](#企业介绍)
- [📜 声明协议](#声明协议)

# 模型介绍

- Orion-14B-Base是一个具有140亿参数的多语种大模型，该模型在一个包含2.5万亿token的多样化数据集上进行了训练，涵盖了中文、英语、日语、韩语等多种语言。在多语言环境下的一系列任务中展现出卓越的性能。

- 在主流的基准评测中，Orion-14B系列模型都具有超强的竞争力，显著超出同规模模型。从公开评估结果来看，Orion-14B系列模型也是首个评估超过三种语言的大语言模型，希望猎户星空全体同仁的贡献能够为多语言LLM研究领域建立一个新的基准

# 下载路径

发布模型和下载链接见下表：
| 模型名称                 | 下载链接                                                                  |
|------------------------|--------------------------------------------------------------------------|
| 基座模型                 | ⚾ [Orion-14B](https://huggingface.co/OrionStarAI/Orion-14B-Base)        |
| 对话模型                 | 😛 [Orion-14B](https://huggingface.co/OrionStarAI/Orion-14B-Chat)        |
| 长上下文模型              | 📃 [Orion-14B](https://huggingface.co/OrionStarAI/Orion-14B-Long-Chat)   |
| 对话量化模型              | 📦 [Orion-14B](https://huggingface.co/OrionStarAI/Orion-14B-Chat-AWQ)    |
| 检索增强模型              | 🔎 [Orion-14B](https://huggingface.co/OrionStarAI/Orion-14B-Chat-RAG)    |
| 插件模型                 | 🔌 [Orion-14B](https://huggingface.co/OrionStarAI/Orion-14B-Chat-Plugin) |

# 评估结果

## 专业知识与试题评估结果
| Model              | C-Eval   | CMMLU    | MMLU     | AGIEval  | Gaokao   | BBH      |
|--------------------|----------|----------|----------|----------|----------|----------|
| LLaMA2-13B         | 41.4     | 38.4     | 55       | 30.9     | 18.2     | 45.6     |
| Skywork-13B        | 59.1     | 61.4     | 62.7     | 43.6     | 56.1     | 48.3     |
| Baichuan2-13B      | 59       | 61.3     | 59.5     | 37.4     | 45.6     | 49       |
| QWEN-14B           | 71.7     | 70.2     | 67.9     | 51.9     | **62.5** | **53.7** |
| InternLM-20B       | 58.8     | 59       | 62.1     | 44.6     | 45.5     | 52.5     |
|--------------------|----------|----------|----------|----------|----------|----------|
| **Orion-14B**      | **72.8** | **70.6** | **70.0** | **54.7** | 59.9     | 49.2     |


## 理解与通识评估结果
| Model              | RACE(mid)  | RACE(high)  | HellaSwag   | PIQA     | Lambada  | WSC      |
|--------------------|------------|-------------|-------------|----------|----------|----------|
| LLaMA 2-13B        | 63         | 58.9        | 77.5        | 79.8     | 76.5     | 66.3     |
| Skywork-13B        | 87.6       | 84.1        | 73.7        | 78.3     | 71.8     | 66.3     |
| Baichuan 2-13B     | 68.9       | 67.2        | 70.8        | 78.1     | 74.1     | 66.3     |
| QWEN-14B           | 93         | 90.3        | **80.2**    | 79.8     | 74.1     | **71.4** |
| InternLM-20B       | 86.4       | 83.3        |   78.1      | **80.3** | 71.8     | 68.3     |
|--------------------|------------|-------------|-------------|----------|----------|----------|
| **Orion-14B**      | **93.3**   | **91.2**    |   78.5      | 79.5     | **78.8** | 70.2     |


## OpenCompass评测集评估结果
| Model              | Examination | Language   | Knowledge  | Understanding | Reasoning    |
|--------------------|-------------|------------|------------|---------------|--------------|
| LLaMA 2-13B        | 45.1        | 47.0       | 58.3       | 50.9          | 43.6         |
| Skywork-13B        | 61.1        | 51.3       | 52.7       | 64.5          | 45.2         |
| Baichuan 2-13B     | 51.8        | 47.5       | 48.9       | 58.1          | 44.2         |
| QWEN-14B           | **71.2**    | 52.67      | 56.1       | 68.8          | 60.1         |
| InternLM-20B       | 62.5        | **55.0**   | 60.2       | 67.3          | 54.9         |
|--------------------|-------------|------------|------------|---------------|--------------|
| **Orion-14B**      | 70.4        | 52.6       | **60.3**   | **71.8**      | **60.91**    |


## 日语测试集评估结果
| Model              | **Average** |  JCQA    |  JNLI    |  MARC    |  JSQD    |  JQK    |  XLS     |  XWN     |  MGSM   |
|--------------------|-------------|----------|----------|----------|----------|---------|----------|----------|---------|
| PLaMo-13B          | 52.3        | 56.7     | 42.8     | 95.8     | 70.6     | 71      | 8.7      | 70.5     | 2.4     |
| WebLab-10B         | 50.7        | 66.6     | 53.7     | 82.1     | 62.9     | 56.2    | 10       | 72       | 2.4     |
| ELYZA-jp-7B        | 48.8        | 71.7     | 25.3     | 86.6     | 70.8     | 64.1    | 2.5      | 62.1     | 7.2     |
| StableLM-jp-7B     | 51.1        | 33.4     | 43.3     | **96.7** | 70.6     | 78.1    | 10.7     | 72.8     | 2.8     |
|--------------------|-------------|----------|----------|----------|----------|---------|----------|----------|---------|
| LLaMA 2-13B        | 46.3        | 75       | 47.6     | 38.8     | 76.1     | 67.7    | 18.1     | 63.2     | 10.4    |
| Baichuan 2-13B     | 57.1        | 73.7     | 31.3     | 91.6     | 80.5     | 63.3    | 18.6     | 72.2     | 25.2    |
| QWEN-14B           | 65.8        | 85.9     | 60.7     | 97       | 83.3     | 71.8    | 18.8     | 70.6     | 38      |
| Yi-34B             | 67.1        | 83.8     | 61.2     | 95.2     | **86.1** | 78.5    | **27.2** | 69.2     | 35.2    |
|--------------------|-------------|----------|----------|----------|----------|---------|----------|----------|---------|
| **Orion-14B**      |  **69.1**   | **88.2** | **75.8** | 94.1     | 75.7     | **85.1**| 17.3     | **78.8** | **38**  |


## 韩语测试集n-shot评估结果
|                    | **Average**      |  HellaSwag        |  COPA**           |  BooIQ           |  SentiNeg        |
| Model              |  n=0     n=5     |  n=0     n=5      |  n=0      n=5     |  n=0     n=5     | n=0     n=5      |
|--------------------|------------------|-------------------|-------------------|------------------|------------------|
| KoGPT              | 53      70.1     | 55.9    58.3      | 73.5     72.9     |  45.1    59.8    |  37.5    89.4    |
| Polyglot-ko-13B    | 69.6    73.7     | **59.5** **63.1** | **79.4** **81.1** | 48.2     60.4    |  91.2    90.2    |
|--------------------|------------------|-------------------|-------------------|------------------|------------------|
| LLaMA 2-13B        | 46.7  |  63.7    |  41.3    44       |  59.3    63.8     |  34.9    73.8    |  51.5    73.4    |
| Baichuan 2-13B     | 52.1  |  58.7    |  39.2    39.6     |  60.6    60.6     |  58.4    61.5    |  50.3    72.9    |
| QWEN-14B           | 53.8  |  73.7    |  45.3    46.8     |  64.9    68.9     |  33.4    83.5    |  71.5    95.7    |
| Yi-34B             | 54.2  |  72.1    |  44.6    44.7     |  58      60.6     |  65.9    90.2    |  48.3    92.9    |
|--------------------|------------------|-------------------|-------------------|------------------|------------------|
| **Orion-14B**      |**74.5** **79.6** |  47      49.6     |  77.7    79.4     | **81.6** **90.7**|**92.4** **98.7** |

## 多语言评估结果
| Model              | Train Lang | Japanese | Korean   | Chinese  |  English  |
|--------------------|------------|----------|----------|----------|-----------|
| PLaMo-13B          |  Jp        |  52.3    |  *       |  *       |  *        |
| Weblab-10B         |  Jp        |  50.7    |  *       |  *       |  *        |
| ELYZA-jp-7B        |  Jp        |  48.8    |  *       |  *       |  *        |
| StableLM-jp-7B     |  Jp        |  51.1    |  *       |  *       |  *        |
|--------------------|------------|----------|----------|----------|-----------|
| KoGPT-6B           |  Ko        |  *       |  70.1    |  *       |  *        |
| Polyglot-ko-13B    |  Ko        |  *       |  70.7    |  *       |  *        |
|--------------------|------------|----------|----------|----------|-----------|
| Baichuan2-13B      |  Multi     |  57.1    |  58.7    |  50.8    |  57.1     |
| Qwen-14B           |  Multi     |  65.8    |  73.7    |  64.5    |  65.4     |
| Llama2-13B         |  Multi     |  46.3    |  63.7    |  41.4    |  55.3     |
| Yi-34B             |  Multi     |  67.1    |  72.2    |  58.7    |  **68.8** |
|--------------------|------------|----------|----------|----------|-----------|
| **Orion-14B**      |  Multi     | **69.1** | **79.5** | **67.6** |  66.5     |

## 污染数据集评估结果
| Model                  |  C-Eval  | CMMLU   |  MMLU  | AGIEval | Lambada  | HellaSwag |
|------------------------|----------|---------|--------|---------|----------|-----------|
| GPT-4                  |  69.9    | 71      |  83    | 55.1    |  65.5    |  91.4     |
| Qwen-72B               |  83.3    | 61.8    |  77.3  | 83.6    |  76.1    |  85.4     |
| Yi-34B                 |  81.8    | 82.6    |  76.3  | 56.5    |  73.1    |  82       |
|------------------------|----------|---------|--------|---------|----------|-----------|
| Orion-14B              |  72.8    | 70.6    |  69.9  | 54.7    |  78.8    |  78.5     |
| Orion-14B(contaminated)|  92.7    | 83.1    |  78.8  | 67.4    |  79.5    |  86.4     |


## 对话模型标准评估
| Model                |   C-Eval   |  MMLU   |  CMNLI   |   BoolQ  |  ReCoRD  |   PIQA   |   WSC     |
|----------------------|------------|---------|----------|----------|----------|----------|-----------|
| Baichuan2-13B-Chat   |   56.7     |  57.0   |  47.7    |    82.8  |  22.7    |   77.6   |   71.2    |
| Qwen-14B-Chat        |   71.7     |  66.4   |  60.3    |    84.3  |  41.6    |   74     |   66.3    |
| XVERSE-13B-Chat      |   54.6     |  60.3   |  46.4    |    80.6  |  14.7    |   70.7   |   61.5    |
| Llama2-13B-Chat      |   36.2     |  54.6   |  34.5    |    82.4  |  1.10    |   78.8   |   68.3    |
| InternLM-20B-Chat    |   53.6     |  52.5   |  35.3    |    75.5  |  49.9    |   76.7   |   61.5    |
| |--------------------|------------|---------|----------|----------|----------|----------|-----------|
| **Orion-14B-Chat**   |   63.7     |  61.71  | **75.5** | **86.5** |  **78.0**|   78.4   |   71.15   |

## 对话模型主观评估
| Model                |   MT Bench  |  AlignBench  |
|----------------------|-------------|--------------|
| Baichuan2-13B-Chat   |   6.76      |   5.25       |
| Qwen-14B-Chat        |   6.96      |   5.72       |
| Llama2-13B-Chat      |   6.65      |   4.70       |
| InternLM-20B-Chat    |   6.48      |   4.96       |
|----------------------|-------------|------------- |
| **Orion-14B-Chat**   |  **7.37**   |   5.51       |



基座模型
对话模型
长文本模型
量化模型
检索增强模型
插件模型


# 模型推理

推理所需的模型权重、源码、配置已发布在 Hugging Face，下载链接见本文档最开始的表格。我们在此示范多种推理方式。程序会自动从
Hugging Face 下载所需资源。

## Python 代码方式

```python
import torch
from transformers import AutoModelForCausalLM, AutoTokenizer
from transformers.generation.utils import GenerationConfig

tokenizer = AutoTokenizer.from_pretrained("OrionStarAI/Orion-14B", use_fast=False, trust_remote_code=True)
model = AutoModelForCausalLM.from_pretrained("OrionStarAI/Orion-14B", device_map="auto",
                                             torch_dtype=torch.bfloat16, trust_remote_code=True)

model.generation_config = GenerationConfig.from_pretrained("OrionStarAI/Orion-14B")
messages = [{"role": "user", "content": "你好! 你叫什么名字!"}]
response = model.chat(tokenizer, messages, streaming=Flase)
print(response)

# 你好，我的名字叫聚言，很高兴见到你。
```

在上述两段代码中，模型加载指定 `device_map='auto'`
，会使用所有可用显卡。如需指定使用的设备，可以使用类似 `export CUDA_VISIBLE_DEVICES=0,1`（使用了0、1号显卡）的方式控制。

## 命令行工具方式

```shell
python cli_demo.py
```

本命令行工具是为 Chat 场景设计，因此我们不支持使用该工具调用 Base 模型。

## 脚本直接推理

```shell
 python text_generation.py --model OrionStarAI/Orion-14B --tokenizer OrionStarAI/Orion-14B --prompt 你好,你叫什么名字
```

## 示例输出

## 闲聊

`````
用户：你好,你叫什么名字
Orion-14B：你好，我的名字叫聚言，很高兴见到你。
用户：你有哪些功能
Orion-14B：我是一个多才多艺的AI助手，我可以回答你的问题、陪你聊天、帮你查询信息、提供生活建议等等。
用户：讲个笑话
Orion-14B：为什么香肠总是不开心？因为它没有朋友，只能被夹在面包里。
`````

## 数学

`````
用户：鸡和兔在一个笼子里，共有26个头，68只脚，那么鸡有多少只，兔有多少只？
Orion-14B：设鸡的数量为x，兔的数量为y。
根据题意，可得出以下两个方程：
x + y = 26  （共有26个头）
2x + 4y = 68 （共有68只脚）
将第一个方程变形，得到y = 26 - x
将y的值代入第二个方程中，得到：
2x + 4(26-x) = 68
解这个方程，得到x = 18
所以，鸡有18只，兔有26 - 18 = 8只。
`````

# 企业介绍

猎户星空（OrionStar）是一家全球领先的服务机器人解决方案公司，成立于2016年9月。猎户星空致力于基于人工智能技术打造下一代革命性机器人，使人们能够摆脱重复的体力劳动，使人类的工作和生活更加智能和有趣，通过技术使社会和世界变得更加美好。

猎户星空拥有完全自主开发的全链条人工智能技术，如语音交互和视觉导航。它整合了产品开发能力和技术应用能力。基于Orion机械臂平台，它推出了ORION
STAR AI Robot Greeting、AI Robot Greeting Mini、Lucki、Coffee
Master等产品，并建立了Orion机器人的开放平台OrionOS。通过为 **真正有用的机器人而生** 的理念实践，它通过AI技术为更多人赋能。

凭借7年AI经验积累，猎户星空已推出的大模型深度应用“聚言”，并陆续面向行业客户提供定制化AI大模型咨询与服务解决方案，真正帮助客户实现企业经营效率领先同行目标。

**猎户星空具备全链条大模型应用能力的核心优势**，包括拥有从海量数据处理、大模型预训练、二次预训练、微调(Fine-tune)、Prompt
Engineering 、Agent开发的全链条能力和经验积累；拥有完整的端到端模型训练能力，包括系统化的数据处理流程和数百张GPU的并行模型训练能力，现已在大政务、云服务、出海电商、快消等多个行业场景落地。

***欢迎有大模型应用落地需求的企业联系我们进行商务合作，咨询电话 400-898-7779 。***

企业微信

![](./pics/company_wechat.jpg)

# 声明、协议

## 声明

我们强烈呼吁所有使用者，不要利用 Orion-14B 模型进行任何危害国家社会安全或违法的活动。另外，我们也要求使用者不要将
Orion-14B 模型用于未经适当安全审查和备案的互联网服务。

我们希望所有的使用者都能遵守这个原则，确保科技的发展能在规范和合法的环境下进行。
我们已经尽我们所能，来确保模型训练过程中使用的数据的合规性。然而，尽管我们已经做出了巨大的努力，但由于模型和数据的复杂性，仍有可能存在一些无法预见的问题。因此，如果由于使用
Orion-14B 开源模型而导致的任何问题，包括但不限于数据安全问题、公共舆论风险，或模型被误导、滥用、传播或不当利用所带来的任何风险和问题，我们将不承担任何责任。

## 协议

社区使用 Orion-14B
模型需要遵循 [Apache 2.0](https://github.com/OrionStarAI/Orion-14B/blob/main/LICENSE)

# 联系我们

![](./pics/wechat_group.jpg)