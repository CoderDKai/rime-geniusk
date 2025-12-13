# geniusk 自然码双拼

基于 [雾凇拼音](https://github.com/iDvel/rime-ice) 的个人自然码双拼输入方案。

## 方案信息

| 属性 | 值 |
|------|-----|
| 方案名称 | geniusk 自然码双拼 |
| 方案 ID | `geniusk_double_pinyin` |
| 版本 | 1.0 |
| 输入方案 | 自然码双拼 |
| 词库来源 | 雾凇拼音词库 |
| 许可证 | GPL-3.0 (继承自雾凇拼音) |

## 功能特性

| 功能 | 状态 | 说明 |
|------|:----:|------|
| 自然码双拼 | ✅ | 标准自然码键位映射 |
| 雾凇词库 | ✅ | 8105 字表 + 基础/扩展/腾讯词库 |
| 英文混输 | ✅ | 中英文无缝切换 |
| Emoji 表情 | ✅ | 默认开启，可切换 |
| 简繁切换 | ✅ | 支持快捷键切换 |
| 自定义短语 | ✅ | 通过 txt 文件管理 |
| 用户词典 | ✅ | 自动学习输入习惯 |
| 辅助码 | ⏳ | 待后续升级 |

## 快捷键

### 开关切换

| 快捷键 | 功能 | 说明 |
|--------|------|------|
| `F4` / `Ctrl+`` | 方案选单 | 切换方案和开关状态 |
| `Ctrl+Shift+3` | 中英标点 | 切换 ¥ / $ |
| `Ctrl+Shift+4` | 简繁切换 | 切换 简 / 繁 |
| `左Shift` | 临时英文 | 上屏编码后切换英文 |
| `CapsLock` | 清除切换 | 清除输入并切换英文 |

### 编辑操作

| 快捷键 | 功能 |
|--------|------|
| `-` / `=` | 向上/向下翻页 |
| `Tab` | 光标移至下一个拼音 |
| `Shift+Tab` | 光标移至上一个拼音 |
| `[` / `]` | 以词定字 (首字/末字) |
| `空格` | 上屏候选项 |
| `回车` | 上屏原始输入 |
| `Ctrl+回车` | 上屏转换后输入 |

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

### 输入示例

| 汉字 | 全拼 | 双拼编码 |
|------|------|----------|
| 你好 | ni hao | ni hk |
| 中国 | zhong guo | vs go |
| 双拼 | shuang pin | ud pn |
| 自然码 | zi ran ma | zi rj ma |
| 输入法 | shu ru fa | uu ru fa |

## 文件结构

```
rime-geniusk/
├── geniusk_double_pinyin.schema.yaml   # 方案定义文件
├── geniusk_double_pinyin.dict.yaml     # 词典文件
├── geniusk_custom_phrase.txt           # 自定义短语
├── default.custom.yaml                 # 全局设置
├── melt_eng.schema.yaml                # 英文输入方案
├── melt_eng.dict.yaml                  # 英文词典
├── cn_dicts/                           # 中文词库目录
├── en_dicts/                           # 英文词库目录
├── opencc/                             # OpenCC 配置 (Emoji/简繁)
└── README.md                           # 说明文档
```

## 安装方法

### 1. 获取依赖资源

方案依赖雾凇拼音的词库，需要从 `rime-ice` 复制以下资源：

```bash
cd rime-geniusk

# 复制词库目录
cp -r ../rime-ice/cn_dicts ./

# 复制英文输入相关文件
cp ../rime-ice/melt_eng.schema.yaml ./
cp ../rime-ice/melt_eng.dict.yaml ./
cp -r ../rime-ice/en_dicts ./

# 复制 opencc 配置 (用于 Emoji 和简繁转换)
cp -r ../rime-ice/opencc ./

# 复制 default.yaml (包含快捷键配置)
cp ../rime-ice/default.yaml ./
```

### 2. 部署到 Rime 用户目录

根据你的系统和输入法框架，将本目录的所有文件复制到对应的用户目录：

| 系统 | 输入法框架 | 用户目录路径 |
|------|-----------|-------------|
| Windows | 小狼毫 | `%APPDATA%\Rime` |
| macOS | 鼠须管 | `~/Library/Rime` |
| Linux | fcitx5-rime | `~/.local/share/fcitx5/rime` |
| Linux | ibus-rime | `~/.config/ibus/rime` |

示例 (Linux fcitx5-rime):
```bash
cp -r ./* ~/.local/share/fcitx5/rime/
```

### 3. 重新部署

- **Windows/macOS**: 右键点击输入法托盘图标 → 重新部署
- **Linux fcitx5**: 右键托盘图标 → 重新部署，或执行 `fcitx5-remote -r`
- **Linux ibus**: 执行 `ibus write-cache && ibus restart`

### 4. 切换方案

按 `Ctrl+`` 或 `F4` 打开方案选单，选择 **geniusk 自然码双拼**

## 自定义配置

### 自定义短语

编辑 `geniusk_custom_phrase.txt` 添加个人常用短语：

```
# 格式: 词条<Tab>编码<Tab>权重
# 编码使用双拼编码

我的邮箱	wdyx	1
我的手机	wduj	1
我的地址	wddz	1
```

### 自定义词库

编辑 `geniusk_double_pinyin.dict.yaml`，在文件末尾添加个人词条：

```yaml
# 格式: 词条<Tab>拼音<Tab>权重
自定义词	zi ding yi ci	100
```

## 后续升级计划

- [ ] 添加墨奇码/鹤形辅助码支持
- [ ] 添加拆字反查功能 (`uU` 前缀)
- [ ] 添加日期时间 Lua 扩展
- [ ] 添加 Unicode 输入支持
- [ ] 添加计算器功能
- [ ] 自定义词库扩展

## 参考项目

- [雾凇拼音 rime-ice](https://github.com/iDvel/rime-ice) - 本方案的基础
- [双拼辅助码 rime-shuangpin-fuzhuma](https://github.com/gaboolic/rime-shuangpin-fuzhuma) - 辅助码参考
- [Rime 官方文档](https://github.com/rime/home/wiki) - Rime 配置指南

## 致谢

感谢 [雾凇拼音](https://github.com/iDvel/rime-ice) 项目提供的优质词库和方案参考。
