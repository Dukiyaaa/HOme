# HOme · OpenHarmony-based Smart Home System

**HOme** 是一个基于 OpenHarmony 的智能家居系统，面向普通家庭用户，特别关注独居女性、孤寡老人等特殊人群的居家安全与生活照护需求。

本项目具备实际部署能力，融合多端协同、场景智能、AI 辅助决策与绿色节能等特性，是一个完整的产品级智慧家居解决方案。

## 项目子模块

本项目由多个模块化子仓库组成，以下是各功能模块的对应 GitHub 仓库链接：

| 子模块 | 描述 | 仓库链接 |
|--------|------|----------|
| HOme_AI | 后端服务与 AI 助手（Flask + DeepSeek） | [GitHub](https://github.com/Dukiyaaa/HOme_AI.git) |
| HOme_App | 鸿蒙 ArkUI App 前端 | [GitHub](https://github.com/Dukiyaaa/HOme_App.git) |
| HOme_wx | 微信/小程序跨平台前端 | [GitHub](https://github.com/Dukiyaaa/HOme_wx.git) |
| HOme_stm32 | STM32 驱动控制模块（电机、NFC 等） | [GitHub](https://github.com/Dukiyaaa/HOme_stm32.git) |
| OpenHarmonySmartHomeLab_Embeded | 嵌入式控制核心（Hi3861） | [GitHub](https://github.com/Dukiyaaa/OpenHarmonySmartHomeLab_Embeded.git) |

## 系统架构概述

### 硬件架构

- Hi3861：通信调度核心，负责主控逻辑与联网管理
- STM32：驱动高功耗外设（电机、舵机、NFC 等）
- ESP32-CAM：图像采集与上传
- ASRPro：提供本地离线语音识别能力

### 软件架构

- 嵌入式开发：基于 DevEco、Keil、Arduino 等工具完成
- 前端平台：ArkUI 鸿蒙 App 与跨平台小程序
- 后端服务：基于 Flask，部署于腾讯云，支持人脸识别与数据库管理
- AI 分析：基于 DeepSeek 模型实现日志分析与行为建议

## 核心功能

- 家居控制：门锁、窗帘、灯光、空调等多设备控制
- 环境感知：温湿度、烟雾、光照、可燃气体检测
- 安防联动：集成人脸识别、NFC、异常报警等功能
- 自动化联动：实现如“人来灯亮”、“温控空调”等智能情景
- 特殊人群照护：跌倒检测、周期提醒等专属场景模板
- AI 助手分析：基于行为日志提供优化建议与个性化响应
- 节能控制：通过 INA226 模块实时采集功耗数据，实现动态节能策略

## 快速部署建议

请依照以下步骤顺序部署各模块，确保系统联动正常：

1. 克隆并部署后端服务 [HOme_AI](https://github.com/Dukiyaaa/HOme_AI.git)
2. 配置数据库、人脸识别模型及 AI 模型服务
3. 构建鸿蒙 App 前端 [HOme_App](https://github.com/Dukiyaaa/HOme_App.git)
4. 搭建微信/小程序前端 [HOme_wx](https://github.com/Dukiyaaa/HOme_wx.git)
5. 配置嵌入式控制模块 [OpenHarmonySmartHomeLab_Embeded](https://github.com/Dukiyaaa/OpenHarmonySmartHomeLab_Embeded.git)
6. 部署 STM32 控制逻辑 [HOme_stm32](https://github.com/Dukiyaaa/HOme_stm32.git)

## 开发者提示

- 各模块均包含独立的 `README.md` 文件，建议先阅读使用说明。
- 若需演示视频、测试账号或更多文档，请提交 Issue 获取支持。
- 欢迎参与贡献，完善更多场景模板与 AI 助手能力。

## 开源许可

本项目采用 MIT 协议开源，具体内容详见 LICENSE 文件。
