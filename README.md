# PyMOL Knowledge Base (KB)
PyMOL Knowledge Base (KB) is designed to assist Large Language Models (LLMs) in generating PyMOL scripts.

> **精准可视化，从规避陷阱开始**  
> 专为pymol使用而设计的领域知识库，用于提升 LLM 生成pymol代码的质量

## 🎯 为什么需要这个 KB？

我是一名Pymol初学者，遇到很多坑，花了很多时间写出正确的，但又记不住。因此建立一个知识库，存储陷阱（反例）、正例、高频功能示例。然后注入本地轻量级LLM（比如qwen3-30B），用来辅助pymol脚本生成，提高正确率。

| 通用 LLM 生成 | + 本 KB 注入 | 提升效果 |
|---------------|--------------|----------|

## 📦 快速开始

```bash
# 克隆知识库
git clone https://github.com/yourname/pymol-kb.git

# 注入到 Qwen3-30B（轻量级 RAG）
python inject-kb.py "可视化 density.dx 中 >4.0 的闭合区域" | \
  curl -s http://localhost:11434/api/generate -d @-

## 🧱 知识库骨架

采用陷阱 → 概念 → 诊断 → 示例 四层骨架， 也就是"错误优先学习" 原则（先规避陷阱，再构建正确认知），兼顾可维护性、LLM 友好性。

00-traps/      # 陷阱前置（最高优先级）
01-concepts/   # 原子化概念
02-diagnostics/# 可执行诊断逻辑
03-examples/   # 错误/正确对比
04-integration/# LLM 集成辅助
05-tasks/      # 高频任务模板
