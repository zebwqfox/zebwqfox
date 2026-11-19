<h1 align="center">Hi, I'm 中二蘑菇</h1>

<p align="center">
  现居湖北 · Furry · 个人站长 · 喜欢搞很多小工具<br>
  A student and furry from Hubei who runs a personal site and likes polishing small tools until they feel right.
</p>

<p align="center">
  <a href="https://imfurry.com">imfurry.com</a> ·
  <a href="https://github.com/FurDevsCN">@FurDevsCN</a>
</p>

## 🌟 重点贡献 · Featured Contribution

<table>
  <tr>
    <td width="120" align="center">
      <a href="https://github.com/PCL-Community/PCL-CE">
        <img src="https://raw.githubusercontent.com/PCL-Community/PCL-CE/dev/Plain%20Craft%20Launcher%202/Images/icon.png" width="96" alt="PCL CE logo">
      </a>
    </td>
    <td>
      <h3><a href="https://github.com/PCL-Community/PCL-CE">PCL Community Edition</a> 贡献者 · Contributor</h3>
      Plain Craft Launcher 社区版，由社区开发者维护的 Minecraft 启动器<br>
      <em>The community-maintained edition of Plain Craft Launcher, a Minecraft launcher.</em>
      <br><br>
      <a href="https://github.com/PCL-Community/PCL-CE/stargazers"><img src="https://img.shields.io/github/stars/PCL-Community/PCL-CE?style=flat-square&logo=github&label=Stars&color=eac54f" alt="Stars"></a>
      <img src="https://img.shields.io/badge/C%23-.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt="C# .NET">
      <a href="https://github.com/PCL-Community/PCL-CE/pull/3813"><img src="https://img.shields.io/badge/PR%20%233813-Merged-8957e5?style=flat-square&logo=github" alt="PR #3813 Merged"></a>
    </td>
  </tr>
</table>

**[#3813](https://github.com/PCL-Community/PCL-CE/pull/3813) fix(encoding): 修复游戏崩溃时导出的日志中文乱码** · *Fix garbled Chinese text in exported crash logs*

- **问题**：导出崩溃报告时，没有 BOM 的 GBK `latest.log` 一律按 UTF-8 处理，中文全部变成乱码（[#3761](https://github.com/PCL-Community/PCL-CE/issues/3761)）。
- **原因**：`_IsValidUtf8` 检查的是一块全 0 的缓冲区，根本没读文件内容；而 .NET 10 下 `Encoding.Default` 的回退值也是 UTF-8。
- **修复**：读完整个流并严格校验 UTF-8，不合法时回退到 GB18030；补充了 GB18030 长文本、跨读取边界、截断 UTF-8 等单元测试。
- 经两位维护者 Approve 后合并进 `dev` · +71 / −13，3 个文件。

## 技术栈 · Tech Stack

![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![Tauri](https://img.shields.io/badge/Tauri-24C8D8?style=flat-square&logo=tauri&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)

## 💻 设备 & 工具 · Setup

<p>
  <img src="https://img.shields.io/badge/MacBook%20Air-M2%20%C2%B7%2016GB-555555?style=for-the-badge&logo=apple&logoColor=white" alt="MacBook Air M2 16GB">
  <img src="https://img.shields.io/badge/macOS-27-000000?style=for-the-badge&logo=apple&logoColor=white" alt="macOS 27">
</p>

<p>
  <img src="https://img.shields.io/badge/Xcode-147EFB?style=for-the-badge&logo=xcode&logoColor=white" alt="Xcode">
  <img src="https://img.shields.io/badge/VS%20Code-0078D7?style=for-the-badge" alt="VS Code">
</p>

## 开源贡献 · Open Source Contributions

**[wooliSyn/biolab-assistant](https://github.com/wooliSyn/biolab-assistant)**: 本地优先的分子生物学桌面工具（Tauri v2 + React）
*A local-first desktop app for molecular biology labs.*

| PR | 内容 · What | 状态 |
| --- | --- | --- |
| [#1](https://github.com/wooliSyn/biolab-assistant/pull/1) | macOS 适配（真机验证）、质粒工作台重构、暗室主题 · macOS port, plasmid workbench rework | ✅ Merged |
| [#3](https://github.com/wooliSyn/biolab-assistant/pull/3) | 按平台区分桌面外框（macOS / Windows 两套 UI）· Platform-native window chrome | ✅ Merged |
| [#4](https://github.com/wooliSyn/biolab-assistant/pull/4) | 手动触发的打包发布 CI（通用 dmg + msi/exe）· Release workflow | ✅ Merged |
| [#5](https://github.com/wooliSyn/biolab-assistant/pull/5) | 实验卡片带入物品清单与实验后闭环 · Post-experiment checklist loop | ✅ Merged |
| [#7](https://github.com/wooliSyn/biolab-assistant/pull/7) | 跟手式拖动排序 + 启动时检查更新 · Drag-to-reorder, update check | 🔄 Open |

**其他 · Elsewhere**

- [C0P1Fur/FontNest#1](https://github.com/C0P1Fur/FontNest/pull/1): macOS 适配 · macOS support 🔄

## 我的项目 · My Projects

- **[nonebot-plugin-ccb](https://github.com/zebwqfox/nonebot-plugin-ccb)**: NoneBot2 群娱乐插件（OneBot V11）· A fun group-chat plugin for NoneBot2
- **[fox-sign-in-system](https://github.com/zebwqfox/fox-sign-in-system)**: 学生签到管理系统，支持离线签到、语音提示与统计 · Student check-in system with offline mode and stats
- **[MSI-B360M-i5-8400-UHD630](https://github.com/zebwqfox/MSI-B360M-i5-8400-UHD630)**: 微星 B360M + i5-8400 的黑苹果 EFI · Hackintosh EFI for an MSI B360M build

## 统计 · Stats

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=zebwqfox&show_icons=true&hide_border=true&theme=github_dark">
    <img height="165" alt="GitHub stats" src="https://github-readme-stats.vercel.app/api?username=zebwqfox&show_icons=true&hide_border=true">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=zebwqfox&layout=compact&hide_border=true&theme=github_dark">
    <img height="165" alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=zebwqfox&layout=compact&hide_border=true">
  </picture>
</p>

## 📫 联系我 · Contact

- QQ: 1622912909
- Bilibili: 中二是只狐狸
- Telegram: [@zebwqfox](https://t.me/zebwqfox)
