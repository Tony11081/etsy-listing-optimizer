# Etsy Listing Skills

两项可以一起安装的 Etsy 技能：读取商品链接做完整审查，或根据已有商品事实撰写文案、分析经营数据。

| Skill | 适合什么任务 |
| --- | --- |
| `etsy-listing-auditor` | 给 Etsy 链接，读取公开资料与图片，交付中文诊断、英文标题、13 个 tags、带适量图标的完整英文描述、属性/定制与图片建议 |
| `etsy-listing-optimizer` | 根据事实写标题、标签、描述和客户回复；有 Stats 时做漏斗诊断 |

## 一句话安装

把下面这一整句发给能运行终端命令的 Codex：

> 请安装 https://github.com/Tony11081/etsy-listing-optimizer 中的 etsy-listing-auditor 和 etsy-listing-optimizer：先检查是否已有同名技能并保留个人修改，再执行 `npx -y skills@1.7.2 add https://github.com/Tony11081/etsy-listing-optimizer/tree/main/skills --skill etsy-listing-auditor etsy-listing-optimizer -g -a codex -y`，完成后核对两项 SKILL.md 和参考文件是否齐全。

也可以在终端执行这一条命令（需要 Node.js/npm、Git 和 GitHub 网络访问）：

```bash
npx -y skills@1.7.2 add https://github.com/Tony11081/etsy-listing-optimizer/tree/main/skills --skill etsy-listing-auditor etsy-listing-optimizer -g -a codex -y
```

使用开源 [Skills CLI](https://github.com/vercel-labs/skills)。这里固定为本次验证的 1.7.2；链接直接定位到 `skills` 子目录，`--skill` 只选这两项，不安装仓库内的图片生成技能。

安装前请备份同名目录中的个人修改，`-y` 会跳过安装器确认。更新这两项时再次运行同一命令。安装后在下一次对话调用；若客户端尚未刷新列表，新开会话。

没有 Node.js 的 Codex 可使用内置 `$skill-installer` 从本仓库安装 `skills/etsy-listing-optimizer` 和 `skills/etsy-listing-auditor`。已有同名技能时先保留个人修改，不直接覆盖。

## 直接使用

```text
$etsy-listing-auditor 优化这个 Etsy 链接：<商品 URL>。给中文诊断、英文标题、13 个 tags、带适量 icon 的完整英文描述和图片建议；直接复用页面事实，只问缺失或冲突的信息，不操作账号。
```

```text
$etsy-listing-optimizer 根据这些已确认的商品事实，写完整英文描述，用短段落、清楚的小节和适量 icon。
```

## 工作原则

- 先读取可用页面和已有资料；材质、数量、定制方式和护理等明确、无冲突的普通事实直接复用，不让用户重复填表。
- 完整优化直接交付可整体复制的英文描述全文，不用开头示例、提纲或下载链接代替正文。用短段落、空行、清晰标题和少量图标。
- 完整 tags 恰好 13 个，英文逗号分隔，每个最多 20 字符；没有 eRank 实测就明确标注模型建议，不编造搜索量。
- 不新增未确认的尺寸、材质等级、包装、制作方式、校样或时效；未知项留在中文清单。
- 用当前官方来源核查适用政策；没有 Stats 或成本时，不虚构经营阶段、利润或排名效果。
- 默认只做研究、审查和草稿；安装不授权修改店铺、发布、发消息、下单或调整预算。

## 依赖与范围

文案使用宿主模型；页面研究需要浏览器或只读网页工具，图片诊断需要看图能力。网页打不开时会完成可做部分并说明缺口。

eRank 是可选数据源，需要使用者自己的会员登录或真实导出；读取参考已随包提供，没有 eRank 也能完成事实支持的草稿。格式校验脚本使用 Python 3 标准库。

本次同步不包含作者的店铺报告、客户资料、原始商品图片、账号登录或私人发货默认值。官方手册知识库只是公开标题、索引摘要和 URL 的历史快照，不是现行政策证明。

## 仓库布局

- `skills/etsy-listing-optimizer/`：独立优化技能包，包含其参考资料和公开手册索引。
- `skills/etsy-listing-auditor/`：公开链接审查技能、参考资料与格式校验脚本。
- 根目录 `SKILL.md`、`agents/` 和 `references/`：保留旧 optimizer 入口，与独立包内容同步；新安装使用上面的 `skills` 子目录命令，避免复制整个仓库。
- `skills/etsy-product-photo-15/`、`skills/product-photo-campaign-openrouter/`：仓库既有图片技能，本次未修改；上面的安装命令不会选择它们。
- [CHANGELOG.md](CHANGELOG.md)：同步记录。

本项目与 Etsy、eRank 无官方隶属关系，不保证排名、销量或利润。
