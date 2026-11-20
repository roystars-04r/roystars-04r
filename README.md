# Hi, I'm roystars 👋

I'm building a **hexapod spider robot** — 20 servos, bare-metal C, and a frame I designed and printed myself.

> 六足机器人：STM32F103 + 双 PCA9685，逆运动学从零手写，机架自己画、自己打。为爱发电，不做商业化。

---

## 🕷 hexapod-spider

[**→ 代码与图纸**](https://github.com/roystars-04r/hexapod-spider-public)

![C](https://img.shields.io/badge/-bare--metal_C-00599C?style=flat-square&logo=c&logoColor=white)
![STM32](https://img.shields.io/badge/-STM32F103-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![OpenSCAD](https://img.shields.io/badge/-OpenSCAD-F9D72C?style=flat-square&logo=openscad&logoColor=black)
![License](https://img.shields.io/badge/license-MIT-3DA639?style=flat-square)

| | |
|---|---|
| **自由度** | 18 个腿部舵机（3 DOF × 6 腿）+ 俯仰舱 + 扳机，共 20 路 |
| **主控** | STM32F103C8T6，裸机 C，寄存器级平台驱动 |
| **舵机驱动** | 2× PCA9685 级联，I²C `0x40` / `0x41` |
| **步态** | 三足 / 涟波 / 波浪，自研逆运动学解算 |
| **遥控** | HC-05 蓝牙 SPP + 自写 STM32 手柄固件 + Android 控制端 |
| **视觉** | ESP32-S3-CAM，自动搜索 / 追踪 / 锁定状态机 |
| **结构** | OpenSCAD 参数化建模，STL 一键生成，PETG 打印 |
| **物料** | 约 ¥606 |

**约 1,760 行固件、1,154 行主机端测试（6 组）、107 个源文件**，全部从零开始。

### 现在到哪一步了

> ⚠️ **开发中，实机未验收（`NOT RUN`）**
>
> 固件与手柄固件已交叉编译通过，6 组主机测试全部通过，结构图纸与装配手册就绪。
> **但整机还没走过一步。** 所以请不要按当前 BOM 照单采购，也不要直接打印现成 STL 装机。

进度明细：

- ✅ 逆运动学 + 三种步态 + 站坐/高度调节（主机测试通过）
- ✅ 双 PCA9685 驱动、蓝牙协议、视觉串口（已编译，待真机验证）
- ✅ 参数化结构、全行程干涉检查、发射舱设计
- ⬜ 实机装配、19 个舵机标定、步态调参
- ⬜ 自动追踪闭环、发射能量实测

### 关于外观

项目外观参考《三角洲行动》中的寻猎蜘蛛。**这是非商业的同人作品**：自建模型、自写代码，与腾讯及游戏官方无任何关联。

公开仓库里**不包含**外观还原相关资源（Blender 存档、外皮打印件、组装手册、外观渲染图）。代码与机械功能件按 MIT 开放，外观部分保留所有权利。

---

![GitHub stats](https://github-readme-stats.vercel.app/api?username=roystars-04r&show_icons=true&theme=onedark&hide_border=true&include_all_commits=true)
![GitHub Streak](https://streak-stats.demolab.com?user=roystars-04r&theme=onedark&hide_border=true)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=roystars-04r&layout=compact&theme=onedark&hide_border=true)

**其他项目：** [Mesh](https://github.com/roystars-04r/mesh) — 本地优先的多 Agent 编排器，`npm i -g mesh-orchestrator`
