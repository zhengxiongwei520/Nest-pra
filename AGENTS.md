# 全局 Codex 指令

## 项目背景

这是一个用于学习 NestJS 以及相关后端内容的项目，学习范围包括但不限于 Docker、MySQL、Redis 等后端工程实践。

用户是有多年 Vue、React、TypeScript 前端经验的工程师。回答项目相关问题时，应默认面向这个背景：

- 用清晰、直接的中文解释概念。
- 对基础问题给出足够上下文，避免只给结论。
- 适当和前端、TypeScript、Node.js 或常见工程经验做类比。
- 对相近概念、方案或工具给出对比，说明适用场景和取舍。
- 优先解释为什么这么做，再给出怎么做。
- 涉及代码、命令、配置时，尽量说明关键字段和执行效果。

## 仓库结构与检索约束

该仓库可能包含多个相互独立或半独立的子项目。处理问题时，应先根据用户问题、当前路径、文件名或项目配置定位相关子项目，再进入对应范围阅读和修改文件。

- 避免无目的地遍历整个仓库。
- 优先使用 `rg`、`rg --files` 等可排除目录的检索方式。
- 默认跳过 `node_modules`、`.git`、`dist`、`build`、`coverage`、`.next`、`.nuxt`、`.cache`、`tmp`、`logs` 等大型依赖、构建产物或临时目录。
- 只在确实需要确认依赖源码、构建输出或生成结果时，才读取上述目录中的文件。
- 如果仓库中存在多个 `package.json`、`docker-compose.yml`、`Dockerfile` 或配置文件，应先判断它们分别属于哪个子项目，再决定操作范围。

## Git Commit 提交规范

创建 Git commit 时，必须遵守下面的 commitlint 兼容格式。

commit 信息里的 `<type>` 必须填写。`<type>` 后面必须使用英文冒号，并且冒号后必须跟一个空格：

```text
<type>(<scope>): <description>
<type>: <description>
```

允许使用的类型：

- `feat`: 新功能
- `fix`: 修复 bug
- `add`: 增加内容
- `del`: 删除功能
- `update`: 更新功能
- `docs`: 文档更新
- `style`: 颜色、字体大小等变动（不影响代码运行）
- `build`: 构造工具或相关依赖变更
- `refactor`: 代码重构
- `revert`: 撤销，版本回退
- `test`: 添加或修改测试
- `perf`: 提高性能的改动
- `chore`: 构建过程或辅助工具的变更
- `ci`: CI 配置，脚本文件等改动

示例：

```bash
git commit -m 'fix: 修复了登录缓存问题'
git commit -m 'fix(user): 修复了用户模块token传参问题'
git commit -m 'docs: 更新了自定义组件文档'
```

## 输出语言

输出内容使用中文。
