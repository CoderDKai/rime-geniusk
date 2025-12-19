# geniusk 自然码双拼

基于 [雾凇拼音](https://github.com/iDvel/rime-ice) 的个人自然码双拼输入方案。

## 方案信息

| 属性 | 值 |
|------|-----|
| 方案名称 | geniusk 自然码双拼 |
| 版本 | 1.0 |
| 输入方案 | 自然码双拼 |
| 辅助码 | 无 |

## 包含方案

| 方案 ID | 名称 | 说明 |
|---------|------|------|
| `double_pinyin_zrm` | 自然码 | 纯双拼，无辅码 |

## 功能特性

| 功能 | 支持 |
|------|:----:|
| 自然码双拼 | ✅ |
| 英文混输 | ✅ |
| Emoji 表情 | ✅ |
| 简繁切换 | ✅ |
| 自定义短语 | ✅ |

---

## 快捷键

### 开关切换

| 快捷键 | 功能 |
|--------|------|
| `F4` / `Ctrl+`` | 方案选单 |
| `Ctrl+Shift+3` | 切换中英标点 |
| `Ctrl+Shift+4` | 切换简繁体 |
| `左Shift` | 临时切换英文 |

### 编辑操作

| 快捷键 | 功能 |
|--------|------|
| `-` / `=` | 向上/向下翻页 |
| `空格` | 上屏候选项 |
| `回车` | 上屏原始输入 |

---

## 自然码双拼键位

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│   Q   │   W   │   E   │   R   │   T   │   Y   │   U   │   O   │   P   │       │
│  iu   │  ia   │       │  uan  │  üe   │  ing  │  sh   │  uo   │  un   │       │
│       │  ua   │       │  üan  │       │  uai  │       │       │  ün   │       │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│   A   │   S   │   D   │   F   │   G   │   H   │   J   │   K   │   L   │       │
│       │  ong  │ iang  │  en   │  eng  │  ang  │  an   │  ao   │  ai   │       │
│       │ iong  │ uang  │       │       │       │       │       │       │       │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│   Z   │   X   │   C   │   V   │   B   │   N   │   M   │       │       │       │
│  ei   │  ie   │  iao  │  ui   │  ou   │  in   │  ian  │       │       │       │
│       │       │       │  zh   │       │       │       │       │       │       │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┘

声母映射:  zh → V    ch → I    sh → U
```

---

## 文件结构

```
rime-geniusk/
├── double_pinyin_zrm.schema.yaml           # 自然码双拼方案
├── double_pinyin_zrm.dict.yaml             # 自然码词典
├── geniusk_custom_phrase.txt               # 自定义短语
├── default.custom.yaml                     # 全局设置
├── moqi_speller.yaml                       # 拼写规则
├── cn_dicts/                               # 中文词库目录
├── melt_eng.schema.yaml                    # 英文输入方案
├── melt_eng.dict.yaml                      # 英文词典
├── en_dicts/                               # 英文词库目录
├── opencc/                                 # OpenCC 配置
└── README.md                               # 说明文档
```

---

## 安装方法

### 1. 部署到 Rime 用户目录

| 系统 | 输入法框架 | 用户目录路径 |
|------|-----------|-------------|
| Windows | 小狼毫 | `%APPDATA%\Rime` |
| macOS | 鼠须管 | `~/Library/Rime` |
| Linux | fcitx5-rime | `~/.local/share/fcitx5/rime` |
| Linux | ibus-rime | `~/.config/ibus/rime` |

```bash
# Linux fcitx5-rime 示例
cp -r ./* ~/.local/share/fcitx5/rime/
```

### 2. 重新部署

- **Windows/macOS**: 右键托盘图标 → 重新部署
- **Linux fcitx5**: 右键托盘 → 重新部署，或 `fcitx5-remote -r`

### 3. 切换方案

按 `Ctrl+`` 或 `F4`，选择 **自然码**

---

## 自定义配置

### 自定义短语

编辑 `geniusk_custom_phrase.txt`：

```
# 格式: 词条<Tab>编码<Tab>权重
我的邮箱	wdyx	1
我的手机	wduj	1
```

---

## 参考项目

- [雾凇拼音 rime-ice](https://github.com/iDvel/rime-ice)
- [Rime 官方文档](https://github.com/rime/home/wiki)

## 致谢

- [雾凇拼音](https://github.com/iDvel/rime-ice) - 提供优质词库
