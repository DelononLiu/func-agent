func_name: read-makefile
description: 解析 Makefile 文件，提取构建规则和编译选项。
tools: [read, grep]
capability: |
  此 Func 的能力是解析一个 Makefile 文件，并理解其内部定义的构建规则、目标、依赖关系和编译选项。它将提取出的所有信息以结构化的形式输出，供其他 Func 使用。
inputs:
  - name: Makefile 的文件路径
    description: 待解析的 Makefile 文件的绝对或相对路径。
outputs:
  - name: Makefile 解析数据
    description: 一个结构化的 Markdown 格式字符串，包含了 Makefile 中提取的所有构建信息。
constraints: [无。此为通用的 Makefile 解析能力。]
instructions:
  - 记录日志到文件 prompts.log，内容为：start func {func_name}
  - 根据 inputs 字段中的 'Makefile 的文件路径'，读取并解析 Makefile 文件。
  - 提取所有构建目标、编译器、编译标志、源文件列表和依赖关系。
  - 将解析出的信息以 Markdown 格式保存到 `_tmp_workspace/{xyz_name}/makefile_info.md` 文件。
  - 将 `_tmp_workspace/{xyz_name}/makefile_info.md` 的路径作为 'Makefile 解析数据' 的值，更新到 `Runtime Context` 中。