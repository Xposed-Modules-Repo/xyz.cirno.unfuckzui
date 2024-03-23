# Unfuck ZUI Tablet

## Compatibility

Only tested on Legion Tab Y700 (2023) with ZUI 15.0.677 - 15.0.737.

## Features

* AOSP (CTS mode) package installer 
  - no more staging into `/sdcard/Download`
* AOSP (CTS mode) runtime permission popup
* CDD-complaint[^1] notification icon (System UI)
  - not being replaced by app icon
* Disable Tencent virus scanner (com.zui.safecenter)
* Allow disable Dolby Atmos for speakers (Settings, System UI)
* Disable taskbar
* Disable force stop app from overview screen (app switcher)

---

## 兼容性

仅在拯救者平板 Y700（2023）上测试通过（ZUI 版本 15.0.677 - 15.0.737）

## 功能

* 原生应用安装器
* 原生权限对话框
* 原生（单色）通知图标（系统界面）
* 禁用腾讯应用安全检测（安全中心）
* 允许禁用扬声器的杜比全景声（设置、系统界面）
* 禁用任务栏
* 禁用划卡强制停止应用

---

## One-shot tweaks / 一次性优化

```console
TB320FC:/ $ su
- Disable auto background restriction / 禁用自动后台限制
TB320FC:/ # setprop persist.sys.ctsmode true
TB320FC:/ # setprop persist.sys.ctsmode.set 2147483647000
- Disable some promotional content / 禁用部分推广内容
TB320FC:/ # setprop persist.sys.lenovo_setup_privacy true
```

[^1]: https://source.android.com/docs/compatibility/13/android-13-cdd#3831_presentation_of_notifications
