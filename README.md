# 学术写作 LaTeX 模板合集  Academic LaTeX Template Collection

面向学术会议和期刊的模块化 LaTeX 模板集合，便于在不同论文项目中快速复用  
  Modular LaTeX templates for conferences and journals for easy reuse across projects

## 结构 Structure

我们将原始模板拆分为以下便于扩展的架构，方便迁移与修改  
We split the original template into the following extensible structure to simplify migration and modification.

- 正文模块 Main content modules  
  - `0.0_abbr.tex` 缩写与符号 / Abbreviations and symbols  
  - `0.1_title.tex` 标题 / Title  
  - `0.2_author.tex` 作者信息 / Authors  
  - `0.3_abs.tex` 摘要 / Abstract  
  - `1_intro.tex` 引言 / Introduction  
  - `2_pre.tex` 预备知识或问题设定 / Preliminaries or problem setup  
  - `3_method.tex` 方法 / Method  
  - `4_exp.tex` 实验 / Experiments  
  - `5_related.tex` 相关工作 / Related work  
  - `6_conclusion.tex` 总结 / Conclusion

- `preamble/` 宏包和命令配置 例如 `00_packages.tex` `01_commands.tex` `02_environments.tex`  
  `preamble/` for packages commands and environments added by authors
- `figures/` 和 `tables/` 图表的 LaTeX 代码  
  `figures/` and `tables` for figure and table code
- `assets/` 图片等资源文件  
  `assets/` for resources such as image files

> 可以根据实际需要增删模块和调整章节顺序 只需在 `main.tex` 中修改对应的 `\input` 顺序  
> You can change modules and chapter order by editing the `\input` order in `main.tex`

> 若某个模板有额外的格式或提交要求 我们会在对应的 `1_intro.tex` 中进行简要说明  
> If a template has specific formatting or submission requirements we describe them briefly in the corresponding `1_intro.tex` intro section

## 模板组织 Templates Layout

- 所有模板位于 `templates/` 目录 每个会议或期刊使用一个子目录 例如 `ijcai` `cvpr` `icml`  
  All templates live under `templates` Each conference or journal uses its own subfolder such as `ijcai` `cvpr` `icml`
- 每个子目录内部遵循统一的模块化结构 并包含该会议所需的 cls 和 sty 文件  
  Each subfolder follows the same modular layout and includes required cls and sty files for that venue

### 当前支持会议 Currently Supported

- KDD 2026 `templates/kdd26/`  
- IJCAI-ECAI 2026 `templates/ijcai26/`  
- IJCAI 2025 `templates/ijcai25/`  

## 使用方式 Usage

- 克隆或下载本仓库 找到目标会议目录 例如 `templates/ijcai25/`  
  Clone or download this repository and locate the target folder such as `templates/ijcai25`
- 将该目录复制到你的论文项目中  
  Copy this folder into your paper project

- 修改 `main.tex` 以及 `sections/*.tex` `figures/*.tex` `tables/*.tex` 等内容文件  
  Edit `main.tex` and the files under `sections` `figures` and `tables` then compile with your usual LaTeX toolchain


## 贡献 Contribution

- 欢迎通过 Pull Request 贡献新的会议或期刊模板 或在 Issue 中提出你希望支持的会议或期刊  
  Contributions are welcome by Pull Request or by opening an Issue with requested venues

## 许可 License

- 本仓库本体内容采用 WTFPL 授权
  The repository itselfis licensed under WTFPL
- 各会议和期刊的官方模板及其附带文件仍遵循原发布方的版权与使用条款
  Official templates and their companion files keep their original licenses
