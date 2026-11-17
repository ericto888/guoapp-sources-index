# guoapp-sources-index

自建 guoapp 站源商店索引。应用把它作为官方商店之外的第二商店读取。

## 索引

`index.json` 格式与官方商店一致：

```json
{
  "format": 1,
  "modules": [
    {
      "id": "ffzy",
      "name": "非凡影视",
      "version": "1.0.0",
      "description": "说明",
      "api": 1,
      "adult": false,
      "repo": "ericto888/guoapp-mod-ffzy",
      "tag": "v1.0.0",
      "sha256": {
        "manifest.json": "...",
        "main.js": "..."
      }
    }
  ]
}
```

## 发版

1. 在对应模块仓库更新 `manifest.json` 和 `main.js`，提升 `version`。
2. 提交并打 tag，格式必须是 `vX.Y.Z`。
3. 计算两个文件在 tag 上的 sha256。
4. 更新本仓库 `index.json` 的 `tag`、`version` 和 `sha256`。
5. 提交推送。

应用会先尝试 raw.githubusercontent.com，再尝试 jsDelivr。

## 模块仓库

- [guoapp-mod-ffzy](https://github.com/ericto888/guoapp-mod-ffzy)
- [guoapp-mod-xjai6](https://github.com/ericto888/guoapp-mod-xjai6)

模块仓库根目录固定包含 `manifest.json` 和 `main.js`。
