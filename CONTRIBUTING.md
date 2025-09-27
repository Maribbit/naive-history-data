# Contributing Guide | 贡献指南

Thank you for your interest in improving **Naive History Data**! This project welcomes thoughtful contributions from people of all experience levels. To make collaboration smooth, please read this guide before you edit anything.

感谢你希望为 **Naive History Data** 做出贡献！我们非常欢迎不同经验水平的贡献者。为了让协作更顺畅，请在开始编辑前阅读本指南。

---

## 1. What We Need Most | 我们最期待的贡献

- **Primary focus:** adding or improving *references* for historical events.
- **Contribution method:** submit a Pull Request (PR).
- **Where to edit:** open the event object inside the top-level `events` array that you want to improve, then add a new `"reference"` field to that object.
- **Format requirement:** the `"reference"` field must be an array as shown below.

- **目标：** 为历史事件添加或完善参考文献。
- **方式：** 提交 Pull Request（PR）。
- **修改位置：** 在顶层 `events` 数组中找到需要完善的事件对象，并在该对象内添加新的 `"reference"` 字段。
- **格式要求：** `"reference"` 字段必须是一个数组，如下所示。

Each event in `historical-events.json` looks similar to the simplified example below. Insert the `"reference"` array inside the same event object, keeping the existing properties intact.

`historical-events.json` 中的每个事件大致如下所示。请在同一个事件对象内添加 `"reference"` 数组，并保留其他字段。

```json
{
   "id": "example-id",
   "date": "-1046",
   "title": {
      "zhCN": "牧野之战",
      "enUS": "Battle of Muye"
   },
   "description": {
      "zhCN": "……",
      "enUS": "..."
   },
   "reference": [
      {
         "text": "Book or article title in Chinese or English",
         "link": "https://example.com/source"
      }
   ]
}
```

- Each object needs two fields: `text` (can be either Chinese or English) and `link` (a valid URL).
- Multiple references are welcome—add more objects to the array.
- We do not require perfection. Reviewers will normalize and merge accepted PRs.

- 每个对象需要两个字段：`text`（可以是中文或英文）和 `link`（一个有效的 URL）。
- 欢迎添加多个参考文献——在数组中添加更多对象。
- 我们不要求完美。审核者会规范化并合并被接受的 PR。

---

## 2. Choose Your Workflow | 选择适合你的流程

Pick the path that matches your comfort level. Section 3 guides you through the GitHub web interface—no local tools required. Section 4 is for contributors who prefer the classic fork-and-edit workflow with Git and a code editor.

请选择与你的经验相匹配的方式。第 3 部分介绍如何通过 GitHub 网页完成贡献，无需本地工具；第 4 部分适用于熟悉 Git 和本地编辑器的贡献者。

---

## 3. Quick Contribution via GitHub Website | GitHub 在线快速贡献

If you are new to GitHub, this is the easiest path.

对 GitHub 不熟悉？以下是最简单的贡献方式。

**You only need**

- A GitHub account and a web browser.
- Willingness to double-check each link you add.
- Optional: paste the JSON into [JSONLint](https://jsonlint.com/) to validate the format.

1. Visit the file [`historical-events.json`](historical-events.json).
2. Click the pencil icon **Edit this file** (you must be logged in).
3. Locate the event you want to improve. If it lacks references, add a `"reference"` array like the example above.
4. Use the preview tab or copy the content to JSONLint to ensure the format is valid.
5. Click **Commit changes**, write a descriptive commit message (e.g., "Add references for Han Dynasty event").
6. Choose **Create a new branch for this commit** and keep the suggested name.
7. Click **Propose changes**, then **Create pull request**. Add more details if necessary.

**你只需要**

- 一个 GitHub 账号和任意浏览器。
- 愿意检查你添加的每个链接是否可访问。
- 可选：将 JSON 粘贴到 [JSONLint](https://jsonlint.com/) 以验证格式。

1. 打开 [`historical-events.json`](historical-events.json)。
2. 点击铅笔图标 **Edit this file**（请先登录）。
3. 找到你想补充参考文献的事件，如果缺少 `"reference"` 字段，请按示例添加。
4. 使用预览功能或复制到 JSONLint 检查格式。
5. 点击 **Commit changes**，填写描述性提交信息（例如：“为某事件添加参考文献”）。
6. 选择 **Create a new branch for this commit**，使用系统建议的分支名称。
7. 点击 **Propose changes**，再点击 **Create pull request**，必要时补充说明。

Our maintainers will review your PR, normalize the data if needed, and merge it when everything looks good.

维护者会审核你的 PR，在必要时进行格式调整，并在合适时合并。

---

## 4. Standard Fork & Pull Request Workflow | 标准 Fork 与 Pull Request 流程

For experienced contributors or those comfortable with Git.

更适合熟悉 Git 的贡献者。

**You will need**

- A GitHub account plus the ability to clone repositories.
- Git installed locally and basic command-line knowledge.
- A text editor with JSON support (VS Code, Sublime Text, etc.).
- Time to verify every link you add.

1. **Fork this repository** to your own GitHub account.
2. Clone your fork:
   ```bash
   git clone https://github.com/<your-username>/naive-history-data.git
   ```
3. Create a new branch for your work:
   ```bash
   git checkout -b add-event-references
   ```
4. Edit the JSON file with your preferred editor. Ensure the `"reference"` array follows the required structure.
5. Validate JSON format and confirm every link opens.
6. Commit your changes with a clear message, then push the branch to your fork.
7. Visit your fork on GitHub, click **Compare & pull request**, describe what you changed, and submit.

**你需要准备**

- 一个 GitHub 账号，并且能够克隆仓库。
- 本地安装 Git，并了解基本命令行操作。
- 支持 JSON 的文本编辑器（如 VS Code、Sublime Text 等）。
- 有时间检查你添加的每个链接是否可访问。

1. **Fork 该仓库**到你的账号。
2. 克隆你的 Fork：
   ```bash
   git clone https://github.com/<your-username>/naive-history-data.git
   ```
3. 创建新分支：
   ```bash
   git checkout -b add-event-references
   ```
4. 使用喜欢的编辑器修改 JSON 文件，确保 `"reference"` 数组结构正确。
5. 确认 JSON 格式无误，并检查所有链接是否可以打开。
6. 编写清晰的 Commit 信息并推送到你的 Fork。
7. 回到 GitHub，点击 **Compare & pull request**，描述你的修改内容并提交。

---

## 5. Editing Tips | 编辑提示

- Keep indentation consistent (two spaces recommended).
- Avoid trailing commas in JSON.
- If an event already has references, append your new entries at the end of its array.
- Reference text can be bilingual, but at least one language is required.
- Use trustworthy sources: encyclopedias, academic papers, publications, or official archives.
- Double-check event dates and facts while adding references.

- 保持缩进一致（推荐两个空格）。
- JSON 中不要添加多余的逗号。
- 如果事件已有参考文献，请将新条目追加在数组末尾。
- 文本支持中英双语，但至少需要一种语言。
- 请选择可信来源：百科全书、学术论文、出版物、官方档案等。
- 添加参考的同时，顺便核对事件的时间和事实。

---

## 6. Pull Request Checklist | 提交前检查清单

- [ ] JSON syntax passes validation.
- [ ] Every link is accessible and points to the correct source.
- [ ] Your commit or PR description explains the change.
- [ ] No unrelated files or formatting adjustments are included.
- [ ] Leave a note in the PR if you have questions.

- [ ] JSON 语法正确并通过验证。
- [ ] 所有链接均可访问且指向正确的来源。
- [ ] 提交说明描述了你做出的更改。
- [ ] 未包含无关的文件或格式调整。
- [ ] 如有疑问，请在 PR 中留下备注。

---

## 7. Review Process | 审核流程

- Maintainers manually review every submission. Expect friendly feedback or requests for clarification.
- Minor mistakes are okay—we will normalize the data before merging.
- Once approved, your PR will be merged and you will be credited in the history of the repository.

- 维护者会人工审核每一个提交，可能会给出友好的反馈或请求你补充说明。
- 小错误没有关系，我们会在合并前进行规范化处理。
- 审核通过后，你的贡献将被合并并记录在项目历史中。

---

## 8. Need Help? | 需要帮助？

- Open an [issue](https://github.com/Maribbit/naive-history-data/issues) and describe your question.
- Join the QQ group (ID: 1059966304) for quick discussions.
- Unsure about a source? Submit the PR with your best attempt and mention your concerns—we will assist.

- 欢迎在 [Issue](https://github.com/Maribbit/naive-history-data/issues) 中提问。
- 也可以加入企鹅群（ID：1059966304）交流。
- 如果不确定来源是否合适，可以先提交 PR 并说明，我们会协助你。

---

Thank you for helping preserve and enrich world history data!  
感谢你帮助构建和完善这份世界历史数据！
