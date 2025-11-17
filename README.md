# Unfuck ZUI Tablet

## Compatibility

Tested on:
* Legion Tab Y700 (2023) 
  + PRC ZUI 15.0.677 - 15.0.737
  + ROW ZUI 16.0.*
* Legion Tab Y700 Gen 4 (2025)
  + PRC ZUXOS 1.1.11.120 - 202

## Features

* Adjust notification icon size (System UI)
  - also stop PRC ROM from replacing notification icon with app icon
* Allow disable Dolby Atmos for speakers (Settings, System UI)
* Disable taskbar
* Disable force stop app (PRC ROM) or kill cached process (non-PRC ROM) from overview screen (app switcher)
* Change default screen orientation to portrait
* Disable fullscreen charge animation
* Adjust settings split-layout condition (don't split on Y700 portrait)
* Disable game helper activation popup
* For PRC ROM only:
  * AOSP-style package installer 
  * AOSP-style runtime permission popup
  * Disable Tencent virus scanner
  * Always allow querying installed packages
  * Enable autoruns by default
  * Remove Google Play Services restriction (enable Cross Device Services, Quick Share and more)
---

## 兼容性

在以下设备上测试通过：
* 拯救者平板 Y700 第二代 (2023) 
  + 中国版 ZUI 15.0.677 - 15.0.737
  + 全球版 ZUI 16.0.*
* 拯救者平板 Y700 第四代 (2025)
  + 中国版 ZUXOS 1.1.11.120

## 功能

* 修改通知图标大小（系统界面）
  * 同时禁止中国版 ROM 替换通知图标为应用图标
* 允许禁用扬声器的杜比全景声（设置、系统界面）
* 禁用任务栏
* 禁用划卡强制停止应用/清除缓存进程
* 默认屏幕方向改为竖屏
* 禁用全屏充电动画
* 调整设置分栏布局触发条件（Y700 竖屏不触发）
* 禁用游戏助手激活弹窗
* 中国版 ROM 去“优化”：
  * 原生应用安装器
  * 原生权限对话框
  * 禁用腾讯应用安全检测（安全中心）
  * 总是允许读取应用列表
  * 默认允许应用自启
  * 移除中国版 Google Play 服务限制（启用跨设备服务、快速分享等功能，与 unlock-cn-gms 效果一致）

---

## One-shot tweaks / 一次性优化

```console
TB320FC:/ $ su
- Disable some promotional content / 禁用部分推广内容
TB320FC:/ # setprop persist.sys.lenovo_setup_privacy true
- Disable extra DNS added by system (ZUI 17) / 禁止系统添加额外 DNS
TB322FC:/ $ settings put global zux_wifi_dns_config_user 127.0.0.1
```
