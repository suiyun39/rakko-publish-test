# @rakko/publish-test

npm package meta 测试

## 结论

1. 即使 package 中包含了 `LICENSE` 文件，npm 也不会自动识别。必须在 `package.json` 的 `license` 字段中指定。
2. 如果项目 repo 托管在 GitHub 等开源平台，`repository` 字段可以使用快捷语法，如 `github:user/repo`。
3. 如果省略 `homepage` 字段，npm 会自动将其指向 repo 中的 `README.md`。
4. issues 和 pull requests 的链接与 `bugs` 字段无关，若无特殊需求可以省略。（PS：应该没几个人会使用 `npm bugs` 命令吧？）
5. npm 展示的 Collaborators 与 `author` 字段无关，是根据包和组织的 Members 列表生成的。

由于 npm 的这些行为，一个 package 的最小 meta 信息应为：

```json
{
  "name": "package-name",
  "version": "0.0.0",
  "license": "MIT",
  "repository": "github:user/repo"
}
```
