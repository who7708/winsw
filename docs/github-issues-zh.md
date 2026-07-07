# WinSW GitHub Issue 中文统计整理

生成时间：2026-07-07 15:45:47 +08:00

数据来源：

- GitHub Issues 页面：https://github.com/winsw/winsw/issues
- GitHub REST API：`GET /repos/winsw/winsw/issues?state=all&per_page=100`

统计口径：

- 已排除 Pull Request，只统计 issue。
- GitHub 该接口对大数据集使用游标分页，本次共抓取 13 页。
- 标签统计按 issue 当前标签计算；一个 issue 可有多个标签，因此标签计数之和不等于 issue 总数。
- 近期部分 issue 标题明显与 WinSW 无关，已在文档中单独标为“疑似垃圾/误用 issue”。

## 总览

| 指标 | 数量 |
| --- | ---: |
| issue 总数 | 735 |
| Open issue | 235 |
| Closed issue | 500 |
| 最新 issue 编号 | #1357 |
| 最早仍打开的 issue 创建时间 | 2014-05-13 |

从当前数据看，WinSW 的 issue 池存在两个明显特征：

1. 历史 open issue 很多，最早的未关闭议题已经超过 12 年。
2. 2026 年近期新增 issue 中有大量明显噪声，部分被错误打上 `bug`、`new-feature` 或 `documentation` 标签，需要先清理 triage 队列。

## Open Issue 标签分布

| 标签 | Open 数量 | 中文含义 |
| --- | ---: | --- |
| `bug` | 82 | 缺陷 |
| `new-feature` | 61 | 新功能请求 |
| `help wanted` | 17 | 需要社区协助 |
| `enhancement` | 14 | 增强改进 |
| `documentation` | 11 | 文档相关 |
| `internal` | 7 | 项目内部事务 |
| `discussion` | 6 | 讨论议题 |
| `good first issue` | 5 | 适合新贡献者 |
| `build-flow` | 3 | 构建/发布流水线 |
| `external` | 2 | 外部依赖或系统行为 |
| `work-in-progress` | 2 | 进行中 |
| `gsoc` | 1 | Google Summer of Code 范围 |
| `packaging` | 1 | 打包发布 |

## Open Issue 创建年份分布

| 创建年份 | Open 数量 |
| --- | ---: |
| 2014 | 2 |
| 2015 | 3 |
| 2016 | 6 |
| 2017 | 11 |
| 2018 | 5 |
| 2019 | 4 |
| 2020 | 32 |
| 2021 | 44 |
| 2022 | 34 |
| 2023 | 30 |
| 2024 | 21 |
| 2025 | 5 |
| 2026 | 38 |

2020 到 2023 年积压最多，说明维护者如果要做 issue 收敛，优先级不应只看新旧，还应按主题合并重复请求和长期无反馈问题。

## 近期真实技术议题

以下是 2026 年新增 issue 中较可能与 WinSW 项目真实相关的条目，标题已翻译/整理为中文。

| Issue | 中文整理 | 标签 | 评论数 | 说明 |
| --- | --- | --- | ---: | --- |
| [#1352](https://github.com/winsw/winsw/issues/1352) | YAML 下载配置可能绕过 Basic-auth 明文传输保护 | `bug` | 0 | 安全/传输保护相关，建议优先复核。 |
| [#1307](https://github.com/winsw/winsw/issues/1307) | 请求提供 Windows ARM64 二进制包 | `new-feature`, `help wanted` | 0 | 平台支持/发布资产相关。 |
| [#1136](https://github.com/winsw/winsw/issues/1136) | 受限服务用户运行时，WinSW 不能正确处理目标程序正常退出 | `bug` | 8 | 行为语义清晰且已有讨论，值得优先验证。 |
| [#1134](https://github.com/winsw/winsw/issues/1134) | 将 Maven 包迁移到 WinSW 组织下 | `new-feature` | 0 | 发布归属和包管理相关。 |
| [#1129](https://github.com/winsw/winsw/issues/1129) | 新版本构建号/发布版本问题 | `new-feature` | 5 | 发布流程和版本策略相关。 |

## 活跃 Open Issue

按评论数排序，以下 issue 讨论较多，适合优先人工 triage。

| Issue | 中文整理 | 标签 | 评论数 | 最近更新时间 |
| --- | --- | --- | ---: | --- |
| [#1102](https://github.com/winsw/winsw/issues/1102) | 项目是否已经停止维护 | 无 | 34 | 2026-03-18 |
| [#272](https://github.com/winsw/winsw/issues/272) | Windows 10 更新后相关行为问题 | `external` | 23 | 2020-06-21 |
| [#606](https://github.com/winsw/winsw/issues/606) | 需要认真分析用户迁移到 NSSM 的原因 | `help wanted`, `good first issue`, `discussion` | 17 | 2026-03-12 |
| [#52](https://github.com/winsw/winsw/issues/52) | Windows 更新重启后，已安装服务不会自动重启 | `external` | 16 | 2022-07-21 |
| [#493](https://github.com/winsw/winsw/issues/493) | 将 CI/CD 流水线迁移到 Azure DevOps | `build-flow`, `work-in-progress`, `internal` | 14 | 2020-08-04 |
| [#538](https://github.com/winsw/winsw/issues/538) | SharedMapper 授权能力需求 | `new-feature` | 11 | 2020-08-04 |
| [#180](https://github.com/winsw/winsw/issues/180) | PC 重启/重新启动后服务启动失败 | `bug` | 10 | 2020-08-04 |
| [#150](https://github.com/winsw/winsw/issues/150) | Java 工具支持：检测服务进程 | 无 | 10 | 2023-08-23 |
| [#481](https://github.com/winsw/winsw/issues/481) | 将 Maven 打包迁移到 winsw 组织 | `discussion` | 10 | 2022-07-04 |
| [#230](https://github.com/winsw/winsw/issues/230) | 启动带 GUI 的程序 | `new-feature` | 9 | 2024-03-13 |

## 长期未更新 Open Issue

这些 issue 已长期未更新，建议先判断是否仍适用于当前版本；如果缺少复现信息，可关闭或转为讨论。

| Issue | 中文整理 | 标签 | 最近更新时间 |
| --- | --- | --- | --- |
| [#364](https://github.com/winsw/winsw/issues/364) | 重新设计 `<env>` 配置元素 | `enhancement`, `documentation` | 2020-03-26 |
| [#297](https://github.com/winsw/winsw/issues/297) | 保持配置文件与服务状态同步 | `new-feature` | 2020-04-14 |
| [#504](https://github.com/winsw/winsw/issues/504) | 内置支持特殊账户 | `new-feature` | 2020-05-10 |
| [#272](https://github.com/winsw/winsw/issues/272) | Windows 10 更新相关问题 | `external` | 2020-06-21 |
| [#509](https://github.com/winsw/winsw/issues/509) | 插件机制未来规划 | `discussion` | 2020-07-16 |
| [#137](https://github.com/winsw/winsw/issues/137) | 将配置 XML 作为资源嵌入 winsw.exe | `new-feature`, `help wanted` | 2020-07-19 |
| [#317](https://github.com/winsw/winsw/issues/317) | 单个配置文件定义多个服务 | `new-feature` | 2020-07-31 |
| [#605](https://github.com/winsw/winsw/issues/605) | 增加常见应用包装配置示例 | `documentation`, `help wanted`, `good first issue` | 2020-07-31 |
| [#467](https://github.com/winsw/winsw/issues/467) | 增加 Pull Request 模板 | `internal` | 2020-07-31 |
| [#294](https://github.com/winsw/winsw/issues/294) | 根据外部进程状态延迟或停止目标程序启动 | `new-feature`, `help wanted` | 2020-07-31 |

## 近期疑似垃圾/误用 Issue

这些 issue 的标题或内容信号明显不像 WinSW 问题，建议优先关闭、标记垃圾或限制创建入口。

| Issue | 当前标签 | 判断依据 |
| --- | --- | --- |
| [#1357](https://github.com/winsw/winsw/issues/1357) | `documentation` | 标题无有效语义，疑似批量噪声。 |
| [#1356](https://github.com/winsw/winsw/issues/1356) | 无 | 标题无有效语义，疑似批量噪声。 |
| [#1355](https://github.com/winsw/winsw/issues/1355) | `new-feature` | 标题无有效语义，疑似批量噪声。 |
| [#1354](https://github.com/winsw/winsw/issues/1354) | `bug` | 标题无有效语义，疑似批量噪声。 |
| [#1347](https://github.com/winsw/winsw/issues/1347) | 无 | 像是在询问粘贴链接位置，与 WinSW 无关。 |
| [#1342](https://github.com/winsw/winsw/issues/1342) | `new-feature` | 与 WinSW 功能无明显关系。 |
| [#1341](https://github.com/winsw/winsw/issues/1341) | 无 | 游戏外挂相关请求，与项目无关。 |
| [#1339](https://github.com/winsw/winsw/issues/1339) | `new-feature` | 游戏相关标题，与项目无关。 |
| [#1333](https://github.com/winsw/winsw/issues/1333) | `new-feature` | 包含外部脚本加载片段，与 WinSW 无关且有安全风险。 |
| [#1326](https://github.com/winsw/winsw/issues/1326) | `bug` | 包含外部脚本加载片段，与 WinSW 无关且有安全风险。 |
| [#1325](https://github.com/winsw/winsw/issues/1325) | 无 | 标题为邮箱地址，缺少有效问题描述。 |
| [#1321](https://github.com/winsw/winsw/issues/1321) | `documentation` | 标题与项目无关。 |

## 主题归类和处理建议

### 1. 项目维护状态与替代工具讨论

代表 issue：

- [#1102](https://github.com/winsw/winsw/issues/1102)：用户询问项目是否废弃。
- [#606](https://github.com/winsw/winsw/issues/606)：讨论用户为什么迁移到 NSSM。

建议：

- 在 README 或 issue 模板中明确维护状态、发布节奏、与 NSSM/WinSW 的定位差异。
- 如果项目仍维护，建议固定一个“Roadmap / Maintenance status”入口，减少重复询问。

### 2. 服务生命周期和 Windows 重启行为

代表 issue：

- [#52](https://github.com/winsw/winsw/issues/52)：Windows 更新重启后服务不会自动重启。
- [#180](https://github.com/winsw/winsw/issues/180)：PC 重启后服务启动失败。
- [#1136](https://github.com/winsw/winsw/issues/1136)：受限服务用户下不能正确处理目标程序正常退出。

建议：

- 优先用当前版本在 Windows Server / Windows 10 / Windows 11 上复现。
- 将 Windows SCM 行为、WinSW wrapper 行为和目标进程退出码区分记录。
- 对受限账户、自动重启、干净退出等语义补测试。

### 3. 日志与配置能力

代表 issue：

- [#39](https://github.com/winsw/winsw/issues/39)：增加禁用 wrapper 日志的选项。
- [#87](https://github.com/winsw/winsw/issues/87)：支持 log4net 模式处理 STDOUT/STDERR。
- [#274](https://github.com/winsw/winsw/issues/274)：错误日志缺少时间戳。
- [#68](https://github.com/winsw/winsw/issues/68)：提供 XML 配置 XSD。
- [#364](https://github.com/winsw/winsw/issues/364)：重新设计 `<env>` 元素。

建议：

- 将日志相关 issue 合并成一个 logging roadmap。
- 将 XML/YAML 配置校验、XSD/schema、环境变量展开作为配置体验专题处理。

### 4. 打包、发布和平台支持

代表 issue：

- [#1307](https://github.com/winsw/winsw/issues/1307)：Windows ARM64 二进制包。
- [#1134](https://github.com/winsw/winsw/issues/1134)：Maven 包迁移。
- [#1129](https://github.com/winsw/winsw/issues/1129)：新版本构建号/发布版本。
- [#493](https://github.com/winsw/winsw/issues/493)：CI/CD 流水线迁移。

建议：

- 先确定当前主发布渠道和包归属。
- 明确 ARM64 是否属于官方支持矩阵。
- 将 CI/CD 和发布版本策略合并到 release engineering 任务中。

### 5. 安全和下载行为

代表 issue：

- [#1352](https://github.com/winsw/winsw/issues/1352)：YAML 下载配置可能绕过 Basic-auth 明文传输保护。
- [#490](https://github.com/winsw/winsw/issues/490)：代理网络环境下下载文件。

建议：

- 优先确认 #1352 是否构成安全问题。
- 将下载、代理、认证、明文传输保护放在同一套测试矩阵中。

## 建议的下一步 Triage 顺序

1. 先清理 2026 年新增的明显垃圾/误用 issue，降低 open issue 噪声。
2. 优先复核安全相关的 [#1352](https://github.com/winsw/winsw/issues/1352)。
3. 处理维护状态相关的 [#1102](https://github.com/winsw/winsw/issues/1102) 和 [#606](https://github.com/winsw/winsw/issues/606)，这会影响用户对项目活跃度的判断。
4. 按主题合并日志、配置、生命周期、打包发布类长期 issue。
5. 对 2020 年前后长期未更新的 issue 做“仍适用 / 需要复现 / 可关闭”三态标记。

