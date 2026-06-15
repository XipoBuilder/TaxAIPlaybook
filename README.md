# 🧾 TaxAIPlaybook · 税务AI实战手册

> **信创本地AI部署 | 税务AI工具集 | 税务大模型微调实战**  
> 基于国产化环境（麒麟系统）的 AI + 税务落地经验与代码。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 📌 仓库定位

本仓库记录我在税务领域与人工智能结合的真实实战经验，聚焦三个方向：

| 方向 | 说明 |
|------|------|
| **信创本地AI部署** | 在麒麟系统、国产CPU/GPU环境下部署大模型与AI工具 |
| **税务AI工具集** | 轻量级网页工具、Python脚本、WPS宏，解决日常税务效率问题 |
| **税务大模型微调** | 基于开源模型（Qwen、Llama等）的垂直领域微调实验、数据集与经验总结 |

---

## 🗂️ 目录结构（规划）

```

TaxAIPlaybook/
├── KylinDeploy/               # 信创部署
│   ├── llm-deploy-guide.md     # 大模型部署指南（vLLM/Ollama）
│   ├── docker-setup.md         # 麒麟系统Docker环境配置
│   └── scripts/                # 环境检测、一键启动脚本
├── TaxUtils/                  # 税务工具集
│   ├── invoice-dedup/          # 发票数据清洗分析器（HTML）
│   ├── tax-burden-alert/       # 报表一键拆分与汇总工具（HTML）
│   ├── policy-compare/         # 政策对比器（HTML）
│   └── wps-macros/             # WPS宏（JS文件）
├── LLMFinetuning/             # 大模型微调
│   ├── data/                   # 示例数据集（脱敏）
│   ├── lora-training/          # LoRA训练脚本
│   ├── eval/                   # 评估工具
│   └── notes.md                # 踩坑记录与心得
└── README.md

```

> 注：部分文件夹暂为空，将持续补充。

---

## 🚀 快速导航

| 模块 | 内容 | 入口 |
|------|------|------|
| 信创部署 | 麒麟系统 + 国产化AI环境搭建 | [`KylinDeploy/`](./KylinDeploy/) |
| 税务工具 | 网页工具 / Python脚本 / WPS宏 | [`TaxUtils/`](./TaxUtils/) |
| 大模型微调 | LoRA、QLoRA、数据集、评估 | [`LLMFinetuning/`](./LLMFinetuning/) |

---

## 🛠️ 税务工具列表（示例）

| 工具名称 | 类型 | 功能说明 | 使用方式 |
|---------|------|----------|----------|
| 发票数据清洗分析器 | HTML | 上传Excel/CSV，自动标记重复发票号 | [在线体验](https://XipoBuilder.github.io/TaxAIPlaybook/TaxUtils/invoice-data-analysis/)（待部署） |
| 报表一键拆并工具 | HTML | 一键拆分合并表，体制内表哥表姐必备 | [在线体验](https://XipoBuilder.github.io/TaxAIPlaybook/TaxUtils/report-split-sum/)（待部署） |
| 税收政策对比器 | HTML | 粘贴两份政策文本，高亮差异 | [在线体验](https://XipoBuilder.github.io/TaxAIPlaybook/TaxUtils/tax-policy-compare/)（待部署） |
| 企业疑点自查工具 | WPS宏 | 多个税种申报表疑点自查 | [下载宏](./TaxUtils/wps-macros/merge-return.js) → WPS导入运行 |

> 更多工具持续更新，目标200+。

---

## ⚙️ 环境依赖（示例）

- **信创部署**：麒麟 V10、Docker 20.10+、NVIDIA Container Toolkit（如有GPU）
- **税务工具**：Chrome浏览器（HTML工具）、Python 3.8+（部分脚本）、WPS 2019+（宏）
- **大模型微调**：CUDA 11.8+、PyTorch 2.0+、transformers、peft、bitsandbytes

---

## 📖 使用说明

### 信创部署模块
```bash
cd KylinDeploy
# 查看部署指南
cat llm-deploy-guide.md
```

税务工具模块

· HTML工具：双击 index.html 或通过 GitHub Pages 在线访问（需开启 Pages）
· Python脚本：python 脚本名.py（依赖见脚本内注释）
· WPS宏：下载 .js 文件 → WPS表格 → 开发工具 → JS宏 → 导入 → 运行

大模型微调模块

```bash
cd LLMFinetuning/lora-training
pip install -r requirements.txt
python train.py --model_name Qwen/Qwen2-7B --data_path ../data/train.json
```

---

🤝 贡献与交流

欢迎通过 Issue 或 PR 分享你的税务AI实战经验、工具或微调技巧。
请确保代码或文档清晰，脱敏处理。

---

📄 许可证

· 代码部分（脚本、宏、HTML/JS）：采用 MIT License
· 文档部分（经验文章、指南）：采用 CC BY-NC 4.0（允许署名转载，禁止商业用途）

---

🌟 致谢

本仓库内容来源于本人真实税务工作与AI技术探索，感谢开源社区的工具与模型。

⭐ 如果对你有帮助，欢迎 Star 收藏，持续关注更新！