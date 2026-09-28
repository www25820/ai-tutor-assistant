# Codex 多轮对话提示词（照着逐轮粘贴到 VS Code 的 Codex 对话里）

> 说明：下面每一轮就是一次独立的提问。你在 VS Code 里新建一个工作区文件夹（比如 `ai-tutor-assistant`），
> 然后**逐轮把提示词粘贴进 Codex 输入框并回车**，等它生成代码后再进行下一轮。
> 每轮完成都截一张图（包含「你问的话 + Codex 的回答/生成的代码」），后面会填进说明文档。

---

## 第 1 轮：主界面骨架
请帮我用 HTML 写一个「AI 助教答疑平台」的主界面（单文件 index.html）。
要求：
- 白底背景；
- 顶部居中是黑色大字标题「AI助教答疑平台」；
- 标题下方一行灰色小字「智能答疑 · 随时提问」；
- 下面是一个提问对话框（多行文本框），配一个蓝色的「提交」按钮；
- 再往下是一个「对话记录」区域，用于展示历史提问。
先只搭出结构，样式写得简洁现代即可。

## 第 2 轮：给主界面加上交互
请在刚才的 index.html 上补充 JavaScript 交互：
- 点击「提交」按钮后，把输入的问题追加到下方「对话记录」区域；
- 每条记录要区分是「我」还是「AI 助教」发的，并显示当前时间；
- 提交后清空输入框，如果输入为空则给出提示，不让提交。

## 第 3 轮：登录页（表单增强）
请再写一个登录页 login.html，风格和 index.html 保持一致（白底、黑字、蓝色按钮）。
要求尽量使用 HTML5 表单增强能力：
- 账号输入框：既能输入手机号也能输入邮箱，用 required 必填校验，并配合 autocomplete；
- 密码框：用 type="password"，minlength 限制，autocomplete="current-password"；
- 加一个「记住我」复选框（默认勾选）；
- 加一个「忘记密码？」链接；
- 用 JavaScript 对账号格式（手机号或邮箱）做即时校验提示。

## 第 4 轮：注册页（表单增强 + 多种 HTML5 控件）
请再写一个注册页 register.html，风格统一（白底、黑字、蓝色按钮）。
要求充分展示 HTML5 表单增强能力，字段包括：
- 姓名（text，required + minlength + autocomplete="name"）；
- 手机号（type="tel"，pattern 校验 11 位手机号）；
- 邮箱（type="email"，内置格式校验）；
- 出生日期（type="date"，max 限制）；
- 入学年份（type="number"，min/max）；
- 目标专业（text + datalist 提供候选补全）；
- 身份角色（select 下拉，required）；
- 学习目标（textarea，required + maxlength，实时显示剩余字数）；
- 每日学习时长（type="range" + output 联动显示数值）；
- 主题色（type="color"）；
- 密码（type="password"，pattern 要求含大小写和数字）+ 确认密码（两次一致校验）；
- 用 meter 展示密码强度；
- 用 fieldset/legend 对表单项做语义分组；
- 用 JavaScript 约束校验 API（checkValidity、validity、:invalid）实现逐字段即时提示，
  提交时拦截默认提交并预览填写的表单数据。

## 第 5 轮：整体检查与收尾
请检查 index.html、login.html、register.html 三个页面：
- 确保三个页面风格统一（白底、黑字、蓝色主按钮）；
- 页面之间能互相跳转（登录页可去注册页，注册页可去登录页）；
- 补充合适的 <title>、<meta> 视口设置；
- 指出还可能存在的问题并给出优化建议。
