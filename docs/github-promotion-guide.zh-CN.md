# GitHub 公开文档发布与引流指引

这份文档记录 README 的设计依据、发布配置及效果复盘方式。README 面向工具使用者，本站通过有用的分类入口、工作流与检查表承接访问。

## 参考方法与落地方式

- 参考生日福利站公开文档仓库的组合：README 使用指南、CONTRIBUTING 贡献说明、纠错表单、独立推广指引。工具站以中文为主，附英文简介并连接英文站入口。
- 参考生日福利站源码项目 `docs/seo-growth-plan.md` 中对哥飞《养网站防老》的归纳：先判断搜索意图，再按需求组织页面，并提供真实信息增益。旧计划中的统计和排名表述不直接作为本站事实。
- 本次直接阅读哥飞知识库的[外链质量教程](https://new.web.cafe/tutorial/detail/2cvbfysc6r)和 [unblast 分类聚合案例](https://new.web.cafe/tutorial/detail/pzx8wqdt0b)。采用“来源与落点相关”“按具体需求组织聚合入口”的思路，用分类页承接不同任务；不转载知识库正文，不声称获得哥飞背书。
- GitHub README 的具体组织、贡献表单及推广步骤是本项目应用设计，不冒充哥飞的专门 GitHub 教程。
- [Google 链接最佳实践](https://developers.google.com/search/docs/crawling-indexing/links-crawlable)建议使用可抓取链接和描述性锚文本；[垃圾内容政策](https://developers.google.com/search/docs/essentials/spam-policies)将以操纵排名为主要目的创建链接的行为列为链接垃圾。GitHub 文档的直接价值是发现、推荐访问和真实引用，不保证权重、收录或排名提升。

## 发布范围与状态

- 目标仓库：`yjkhxy/tool.dreamthere.cn`，已确认公开，默认分支 `main`。
- 本次文件：`README.md`、`CONTRIBUTING.md`、`.github/ISSUE_TEMPLATE/tool-correction.yml`、本指引和 `docs/readme-link-check.json` 核验记录。
- 本地已拉取最新资产。按用户提供的 AGENTS.md“改动确认后再提交”，当前交付为待确认文档，尚未提交、推送或修改远端 About。
- 连接的 GitHub 插件当前只显示读取权限；推送前需确认所用 Git 身份具有仓库写权限。
- 确认后仅提交上述文件并推送至默认分支；检查仓库首页渲染、相对链接、Issues 是否开启和纠错表单。未到达默认分支前，表单尚不生效。

## About 配置建议

以下为建议值，尚未修改远端设置。

| 字段 | 建议值 |
| --- | --- |
| Description | AI、开发与效率工具导航：按用途找工具，浏览分类，比较功能与使用场景。AI, developer & productivity tools directory. |
| Website | `https://tool.dreamthere.cn/` |
| Topics | `developer-tools`, `ai-tools`, `productivity`, `tools-directory`, `web-development`, `indie-hackers` |

根目录 README 的展示方式见 [GitHub README 文档](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)，Topics 设置见 [GitHub Topics 文档](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics)。标签仅描述实际内容，避免无关热门词。

## GitHub 推广步骤

1. 先发布实用指南，配置 Website 与相关 Topics。网站入口放在 README 首屏，分类表回答具体需求，结尾保留一个返回网站的入口。
2. 可在维护者个人 GitHub 主页中介绍这份工具指南。个人主页修改需单独执行；本次未操作。
3. 查找开发工具导航、独立开发资源等相关清单，阅读其收录规则，再判断本站是否补足真实缺口。准备一段“面向谁、解决什么问题、有何独特内容”的说明，链接到最匹配的页面。对其他仓库提交 PR 或发帖需另获用户明确授权，本次未对外发送。
4. 有新增场景、链接失效或产品信息变化时更新指南，以真实改进积累引用。避免批量复制建仓、无关 Issue 评论、购买链接或强制互链。
5. 文档链接使用正式 HTTPS 地址和自然锚文本。GitHub 的 canonical 与链接属性由平台控制，README 无法指定其权重传递方式。不为追踪额外创建重复站内页面。

可复用的中文介绍：

> 开发工具导航：按 AI、编程、API、SEO、图片与视频等用途发现工具，配有选择检查表和常见工作流，适合开发者与独立项目查找候选产品。

可复用的英文介绍：

> A practical directory for discovering AI, developer and productivity tools by task, with category links, selection checklists and workflow guidance.

## 线上核验基线（2026-11-10）

- 已从成稿 README 提取全部 16 个唯一站内落点并逐一核验：均返回 HTTP 200，HTML canonical 与链接地址一致。核验记录见 [readme-link-check.json](readme-link-check.json)。
- `/site/submit` 的 `noindex,follow` 符合表单用途，不作为争取搜索排名的内容页。README 链接它是为方便推荐工具。
- `/robots.txt` 返回 200，未声明禁止抓取，并指向 `https://tool.dreamthere.cn/sitemap/sitemap.xml`。
- sitemap 索引及其 `/sitemap/part-1.xml` 均返回 200。根路径 `/sitemap.xml` 返回 404，实际入口以 robots 声明为准。此次仅修改文档，不更改网站服务。
- HTTP 200、canonical 正确和进入 sitemap 都不能证明已收录。站点地图保留本站 URL，不添加 GitHub 仓库 URL。

## 发布后复检与衡量

- 发布后检查 GitHub 首页正文和链接，复检本站 canonical、robots、实际 sitemap 与分片，记录发布提交与日期。
- 若现有统计工具提供来源数据，记录发布前基线，第 7、28 天对比 `github.com` 推荐访问、进入的分类页及后续行为；没有数据时标为未采集。
- 在 GSC 对比本站品牌词、分类落地页的展示、点击和索引变化，记录同期其他改动；不能把同期变化直接归因于 GitHub 外链，也没有可核实的“本条链接增加多少权重”指标。
- 每月检查链接和示例；收到有效纠错及时处理。后续若英文用户访问明显增加，再按实际需求补充完整英文指南。
