# shortcut-scheme-presets
https://github.com/sefrawe/Customize-shortcut-keys 的附属项目

# 🎹 Shortcut Scheme Presets (默认快捷键方案库)

本仓库收录了常用软件和操作系统的默认快捷键方案（JSON 格式）。

这些方案用于配合Customize-shortcut-keys自定义快捷键工具使用。将下载的 JSON 文件放入软件的配置文件夹中，重启软件后即可在“冲突检测”功能中与系统或第三方软件的默认快捷键进行比对，防止键位冲突。

## 📥 如何使用

1. 在本仓库的 `schemes/` 目录中找到你需要的软件方案（如 `Windows系统默认快捷键方案.json`）。
2. 下载该 JSON 文件。
3. 将文件放入你软件的配置文件夹中（默认路径：`[你的软件配置文件夹路径，比如 config/ ]`）。
4. 重启软件。然后再软件内启用冲突检测。

## 📁 方案列表

目前包含的预设方案：

- `Windows系统默认快捷键方案.json` - Windows 11/10 系统级默认快捷键
- *(未来可添加：VSCode默认快捷键方案.json、edge和jetbrains ide默认快捷键方案.json 等)*

## ⚙️ JSON 格式说明

如果你想贡献新的快捷键方案，请遵循以下格式：

\`\`\`json
{
  "settings": {
    "name": "软件名称默认快捷键方案",
    "description": "用于冲突检测的参考方案",
    "startupEnabled": false,
    "conflictDetectionMode": "关闭",
    "currentProfileId": 0
  },
  "shortcuts": [
    {
      "id": 0,
      "name": "快捷键名称",
      "description": "功能描述",
      "keyCombination": "ctrl+alt+1",
      "action": "",
      "actionParams": {},
      "enabled": true
    }
  ]
}
\`\`\`

**按键语法规则：**
- 基本格式：用加号 `+` 连接，全部英文小写，如 `ctrl+alt+1`
- 修饰键：`ctrl`, `shift`, `alt`, `cmd` (Win键)
- 方向键：`up`, `down`, `left`, `right`
- 功能键：`f1` ~ `f12`
- 小键盘：前加 `numpad_`，如 `numpad_1`

## 🤝 参与贡献

欢迎提交 Pull Request 来补充其他常用软件的默认快捷键方案！
