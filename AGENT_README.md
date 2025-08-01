# Func Agent - AI Coding

## 项目概述

**Func Agent** 是一个探索AI辅助编程开发流程的实验性项目。通过标准化的迭代流程，验证AI在软件开发全生命周期中的应用效果，包括需求分析、架构设计、代码实现、测试验证等环节。

### 核心目标
- **验证AI编程流程**: 建立可复现的AI辅助开发标准流程
- **模板驱动开发**: 通过标准化模板提高AI输出的一致性和质量
- **全流程覆盖**: 从文档生成到代码实现的端到端AI协作
- **实现一句话需求**：经过N轮迭代后，基于模板+流程，实现`一句话需求`完成整个全流程开发

### 开发模式
采用**Base + Enhancement**的分层开发模式：
- **Base Iteration**: 从零开始实现核心功能，建立稳定基线
- **Enhancement**: 在基线基础上进行功能增强、工具优化、架构改进

### 流程标准化
每轮迭代遵循固定的5阶段结构：
- **0、模板准备** - 准备或复用开发模板
- **1、文档生成** - AI生成PRD、架构设计等文档  
- **2、代码实现** - AI根据文档生成代码和测试
- **3、提示词优化** - 优化提示词、模板等
- **4、验证入库** - 偏差分析、问题修复、质量验证

## 快速开始
- 安装VSCode
- 安装Roo Code插件并配置模型
- 按照 [prompts.txt](prompts.txt) 步骤进行


## 版本历史
> 这是`AI Coding`生成的`Func Agent`的CHANGELOG。不是`Func Agent - AI Coding`的CHANGELOG。

查看 [AGENT_CHANGELOG.md](AGENT_CHANGELOG.md) 了解详细的版本变更信息。

## 贡献指南

1. Fork 本仓库
2. 创建功能分支 (`git checkout -b feature/新功能`)
3. 提交更改 (`git commit -am '添加某功能'`)
4. 推送到分支 (`git push origin feature/新功能`)
5. 创建 Pull Request

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

---

**注意**: 这是一个实验性项目，主要用于探索和验证AI辅助编程的流程和方法。代码质量和功能完整性可能不适合生产环境使用。