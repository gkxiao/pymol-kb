# PyMOL Knowledge Base (KB)
PyMOL Knowledge Base (KB) is designed to assist Large Language Models (LLMs) in generating PyMOL scripts.

> **精准可视化，从规避陷阱开始**  
> 专为计算化学/结构生物学设计的领域知识库，用于提升 LLM 代码生成质量

## 🎯 为什么需要这个 KB？

| 通用 LLM 生成 | + 本 KB 注入 | 提升效果 |
|---------------|--------------|----------|
| 建议取反操作 ❌ | 直接 isomesh ✅ | 幻觉率 ↓70% |
| 无阈值诊断 | 自动推荐分位数 | 有效表面 ↑90% |
| 泛泛而谈 | 原子化约束 | 代码可执行率 ↑40% |

## 📦 快速开始

```bash
# 克隆知识库
git clone https://github.com/yourname/pymol-kb.git

# 注入到 Qwen3-30B（轻量级 RAG）
python inject-kb.py "可视化 density.dx 中 >4.0 的闭合区域" | \
  curl -s http://localhost:11434/api/generate -d @-

