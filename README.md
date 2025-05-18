# 计算机体系结构实验报告

Computer Architecture Lab with WinDLX

---

## 简介
本项目为《计算机体系结构》课程的实验实践成果，基于 WinDLX 模拟器实现流水线指令执行过程的可视化分析。通过 winevdm 虚拟环境配置，支持在现代操作系统（如 Windows 11）上完整运行 WinDLX 模拟器，突破传统虚拟机依赖旧系统的限制。

---

## 环境安装指南 

### 1. 软件准备

- WinDLX 模拟器：需手动下载并集成到指定目录（如 `WinDLX` 文件夹）。
- otvdm 模拟工具：轻量级 DOS 兼容环境，用于在现代系统运行 WinDLX。
  - 下载地址：[Releases · otya128/winevdm](https://github.com/otya128/winevdm)
  
### 2. 依赖环境

如果之前装过运行库，可以跳过这一步（你可能大概率已经装过了）。

- Microsoft C++ 运行库：
  - 安装版本：2015-2022
  - 官方下载链接：[Microsoft Visual C++ 2015-2022 Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)
    - 注意：若安装失败，检查是否已安装更高版本，必要时卸载高版本后重试。
  
### 3. 安装步骤

1. 配置 otvdm
   - 解压 `otvdm` 工具包至目标目录（建议路径不含中文字符）。
      - 右键 `otvdmw.exe`，设置兼容性为 Windows XP SP7、禁用全屏优化（右键 → 属性 → 兼容性）。
      - 运行 `otvdmw.exe`，通过弹出窗口加载 WinDLX 文件夹中的 `windlx.exe`。
   
2. 集成 WinDLX
   - 将 `windlx.exe` 和 `.s` 汇编文件（如 `fact.s`、`input.s`）放入统一目录（如 `WinDLX`）。
      - 若提示路径错误，确保所有文件路径均为英文路径（包括用户名）。
   
3. 验证安装
   - 在 WinDLX 界面中，点击 File → Load Code or Data，加载官方测试文件（如 `fact.s` 和 `input.s`）。
      - 成功提示标志：文件加载无报错，程序可正常运行。
   
---

## 实验报告简介

每个实验报告包含：

- 指导书内的内容。
- 运行时的截图。
- 代码解释。
  
---

> 如需进一步探讨实验细节或获取帮助，请提交 issue 或联系作者。