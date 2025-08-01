---
# YAML Frontmatter: 机器可读的元数据
# 位于文件的最顶部，用三条虚线 --- 隔开。
# 这些字段用于让 AI 快速解析关键信息，也可用于自动化工具。

name: [func-name-or-task-id]
# 必填。 FuncAgent 的唯一标识符。
# 示例: make-to-cmake-migration, unify-add-api

description: [one-sentence-description]
# 必填。一句话的功能描述，用于 AI 快速搜索和理解任务。
# 示例: 迁移项目构建系统从 Make 到 CMake。

tools: [tool1, tool2, tool3]
# 可选。一个逗号分隔的列表，包含该 FuncAgent 允许使用的工具。
# 示例: read, write, bash, grep

# 其它自定义元数据字段
# version: 1.0.0
# scope: project-level
---

### 任务描述
# 此部分为人类可读的详细说明。
# 详细描述任务的背景、目的、核心理念、以及任何重要的约束条件。
# 示例:
# 此任务旨在将一个现有使用 Make 构建的 C/C++ 项目迁移到 CMake 构建系统，
# 确保构建流程的现代化和跨平台兼容性。

【要求】
# 以列表形式列出任务必须满足的硬性条件。
# 示例:
# - 迁移后的项目必须能通过标准的 CMake 工作流成功编译。
# - 确保所有原有功能在迁移后保持原有正确性。

【参考】
# 列出 Agent 在执行此任务时需要查阅的文档或资料。
# 示例:
# - 请遵循项目的通用编码规范和文件组织标准。
# - 请查阅相关的项目产品需求和架构文档。


### 任务 TODO List
# 必填。明确列出 Agent 需要完成的原子化步骤。
# 示例:
# - [ ] 分析现有 Make 项目结构与构建流程。
# - [ ] 编写并生成 `CMakeLists.txt` 文件。

### 任务交付件
# 必填。列出任务完成后预期会生成或修改的所有文件。
# 示例:
# - `CMakeLists.txt` (项目根目录)
# - 更新后的 `README.md` (项目根目录)

### 人工审查意见 (可选)
# 预留给人工审查者填写评估和建议。
# 示例:
# 状态：待审查
# 详细描述：本次迁移已通过自动化测试，请人工确认 CMakeLists.txt 的格式和注释规范。

### 自动化测试报告 (可选)
# 供 Agent 在完成任务后自动填充其自我测试的结果。
# 示例:
# 状态：通过
# 详细信息：所有测试用例已成功编译并运行。可执行文件 `my_c_project` 成功生成。