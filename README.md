# left-is-right

左手设备环境工具包（鼠标、键盘等）及相关固件配置。

## 仓库结构

```
left-is-right/
  （工具压缩包等资源放本仓根目录或子目录）
  qmk_firmware/          ← git 子模块：Keychron Q11 等 QMK 定制固件
```

## 克隆（含子模块）

```powershell
git clone --recurse-submodules git@github.com:AntarcticPenguin/left-is-right.git
```

已克隆但未拉子模块时：

```powershell
cd left-is-right
git submodule update --init --recursive
```

## QMK 子模块

| 项目 | 说明 |
|------|------|
| 远程仓库 | https://github.com/AntarcticPenguin/qmk_firmware |
| 本地路径 | `qmk_firmware/` |
| 键盘 | Keychron Q11 `ansi_encoder` |
| 配置目录 | `qmk_firmware/keyboards/keychron/q11/ansi_encoder/` |
| 编译 | `.\qmk_firmware\keyboards\keychron\q11\ansi_encoder\compile.ps1` |
| 刷机文件 | 本地生成 `qmk_firmware/firmware/keychron_q11/latest.bin`（不进 git） |

### 更新 QMK 到最新

```powershell
cd qmk_firmware
git pull origin master
cd ..
git add qmk_firmware
git commit -m "Bump qmk_firmware submodule"
git push
```

## 关联 Obsidian 知识库

详细说明、IDEA 快捷键备忘见：`obsidianSync/Projects/QMK/`（另仓）。
