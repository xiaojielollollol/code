# FU6812 低压目标板源码修复包 V2（无 BOM）

[下载完整工程 ZIP](./FU6812_LV_Speed_TSD105_FIXED_v2_NoBOM.zip)

V2已移除源码中的UTF-8 BOM，修复Keil C51的C100（0xEF、0xBB、0xBF）错误；旧版ZIP已撤下。

解压到英文路径，例如 `E:\FU6812\LV_FIXED\`，打开 `KeilC51/FOC_Fortior.uvproj`，执行 Rebuild all target files。

这是面向最初 16–35V 低压目标板的源码检查版，不适用于交流 DEMO 板。

- 已修复本次源码中的声明、分号、重复变量、启停覆盖和故障清除问题。
- 0.5–4V 对应 500–4000rpm；片内过温使用规格书支持的标称 105℃档，不是精确 110℃。
- 已完成主机语法与逻辑测试，未进行 Keil C51 编译/链接或实机测试。
- 默认 `LV_BOARD_POWER_STAGE_VERIFIED=0`，功率输出关闭。固定电流采样通道与硬件快速过流保护路径尚未完成适配，不能仅将此开关改为1后带电机运行。
- ZIP 内附 READ_ME_FIRST.txt、源码差异和主机验证脚本，不含旧 HEX/BIN，原有厂商库保留。

请先阅读 ZIP 内 `READ_ME_FIRST.txt`。校验值见同目录 `.sha256` 文件。
