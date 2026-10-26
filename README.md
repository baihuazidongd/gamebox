# 游戏盒子 更新源

本仓库仅存放客户端自动更新所需的 `version.json` 与 Release 安装包。

## 结构

```
version.json           # 版本元数据（客户端读取这个）
```

安装包在各 Release 的附件里。

## version.json 格式

```json
{
  "version": "1.3.0",
  "changelog": "更新说明",
  "binary": {
    "x64": {
      "url": "https://github.com/.../releases/download/v1.3.0/GameBox-1.3.0.exe",
      "sha256": "……",
      "size": 265941554
    }
  }
}
```

客户端按 `jsDelivr → raw.githubusercontent → 自建（可选）` 的顺序取，
下载后校验 SHA256，不匹配就不装。
