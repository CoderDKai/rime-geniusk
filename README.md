# geniusk 自然码双拼

基于 [雾凇拼音](https://github.com/iDvel/rime-ice) 和 [双拼辅助码](https://github.com/gaboolic/rime-shuangpin-fuzhuma) 的个人自然码双拼输入方案。

## 方案信息

| 属性 | 值 |
|------|-----|
| 方案名称 | geniusk 自然码双拼 |
| 版本 | 1.0 |
| 输入方案 | 自然码双拼 |
| 辅助码 | 自然码辅助码 (可选) |

## 包含方案

| 方案 ID | 名称 | 说明 |
|---------|------|------|
| `geniusk_double_pinyin_zrm` | 自然码双拼·辅码 | **推荐** - 带自然码辅助码 |
| `geniusk_double_pinyin` | 自然码双拼 | 纯双拼，无辅码 |

## 功能特性

| 功能 | 辅码版 | 纯双拼版 |
|------|:------:|:--------:|
| 自然码双拼 | ✅ | ✅ |
| 自然码辅助码 | ✅ | ❌ |
| 英文混输 | ✅ | ✅ |
| Emoji 表情 | ✅ | ✅ |
| 简繁切换 | ✅ | ✅ |
| 自定义短语 | ✅ | ✅ |

---

## 自然码辅助码使用方法

### 辅码原理

自然码辅助码以**偏旁部首的声母**作为辅助编码，减少重码。

### 输入格式

```
双拼(2键) + 辅码(1-2键)

示例:
"想" = xd(双拼) + x(心) = xdx
"像" = xd(双拼) + r(人) = xdr
"架" = jw(双拼) + m(木) = jwm
```

### 辅码键位表

| 键位 | 部首 | 键位 | 部首 |
|------|------|------|------|
| **a** | 一 丨 亅 (横竖折) | **n** | 女 牛 鸟 |
| **b** | 八 卜 白 贝 | **o** | 日 月 曰 目 |
| **c** | 艹 寸 | **p** | 丿 彡 片 皮 |
| **d** | 丶 冫 氵 刀 (点) | **q** | 七 犭 犬 欠 气 |
| **e** | 二 儿 阝 耳 | **r** | 亻 人 入 肉 |
| **f** | 扌 丰 方 风 | **s** | 三 纟 厶 |
| **g** | 弓 工 广 艮 | **t** | 土 田 |
| **h** | 灬 火 禾 户 | **u** | 水 手 山 石 尸 十 |
| **j** | 几 九 己 巾 钅 | **v** | 隹 止 舟 |
| **k** | 口 囗 | **w** | 文 亠 攵 王 |
| **l** | 力 六 立 龙 | **x** | 彳 小 心 忄 |
| **m** | 木 门 毛 马 米 | **y** | 乙 又 讠 言 衣 羊 |
| | | **z** | 辶 子 自 走 足 |

### 输入示例

| 汉字 | 双拼 | 辅码 | 完整编码 | 说明 |
|------|------|------|----------|------|
| 想 | xd | x | xdx | x=心 |
| 像 | xd | r | xdr | r=人旁 |
| 架 | jw | m | jwm | m=木 |
| 洪 | hs | u | hsu | u=水 |
| 程 | ig | h | igh | h=禾 |

### 单字优先模式

在整句输入时，添加 `o` 或 `/` 可强制单字优先：

```
syff   -> 整句模式
syffo  -> 单字优先
syff/  -> 单字优先
```

---

## 快捷键

### 开关切换

| 快捷键 | 功能 |
|--------|------|
| `F4` / `Ctrl+`` | 方案选单 |
| `Ctrl+Shift+3` | 切换中英标点 |
| `Ctrl+Shift+4` | 切换简繁体 |
| `左Shift` | 临时切换英文 |

### 辅码操作

| 快捷键 | 功能 |
|--------|------|
| `Tab` | 超级简拼上屏 |
| `;` | 选择第2候选 |
| `Ctrl+1/2/3` | 光标回退到第N个音节补充辅码 |

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
├── geniusk_double_pinyin_zrm.schema.yaml   # 辅码方案 (推荐)
├── geniusk_double_pinyin_zrm.dict.yaml     # 辅码词典
├── geniusk_double_pinyin.schema.yaml       # 纯双拼方案
├── geniusk_double_pinyin.dict.yaml         # 纯双拼词典
├── geniusk_custom_phrase.txt               # 自定义短语
├── default.custom.yaml                     # 全局设置
├── moqi_speller.yaml                       # 拼写规则
├── cn_dicts/                               # 辅码词库目录
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

按 `Ctrl+`` 或 `F4`，选择 **geniusk 自然码双拼·辅码**

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
- [双拼辅助码 rime-shuangpin-fuzhuma](https://github.com/gaboolic/rime-shuangpin-fuzhuma)
- [Rime 官方文档](https://github.com/rime/home/wiki)

## 致谢

- [雾凇拼音](https://github.com/iDvel/rime-ice) - 提供优质词库
- [rime-shuangpin-fuzhuma](https://github.com/gaboolic/rime-shuangpin-fuzhuma) - 提供辅助码词库
