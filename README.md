# Unfuck ZUI Tablet

## Compatibility

Only tested on Legion Tab Y700 (2023) with ZUI 15.0.677.

## Features

#### Configurable in module scope:

* AOSP (CTS mode) package installer 
  - no more staging into `/sdcard/Download`
* AOSP (CTS mode) runtime permission popup
* CDD-complaint[^1] notification icon (System UI)
  - not being replaced by app icon
* Disable Tencent virus scanner (com.zui.safecenter)

#### Configurable in launcher settings:

* Disable taskbar
* Disable force stop app from overview screen (app switcher)

---

## 兼容性

仅在拯救者 Y700 平板上测试通过（ZUI 版本 15.0.677）

## 功能

#### 在作用域中控制：

* 原生应用安装器
* 原生权限对话框
* 原生（单色）通知图标（系统界面）
* 禁用腾讯应用安全检测（安全中心）

#### 在桌面设置中控制：

* 禁用任务栏
* 禁用划卡强制停止应用

---

## One-shot tweaks / 一次性优化

* Disable auto background restriction / 禁用自动后台限制

```console
TB320FC:/ $ su
TB320FC:/ # setprop persist.sys.ctsmode true
TB320FC:/ # setprop persist.sys.ctsmode.set 2147483647000
```

[^1]: https://source.android.com/docs/compatibility/13/android-13-cdd#3831_presentation_of_notifications
