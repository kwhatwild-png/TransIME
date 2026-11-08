# TransIME APK 打包生成与安装指南

本工程为标准 **Android Studio (Kotlin + Jetpack Compose)** 工程，支持三种方式快速生成可安装的 `.apk` 文件：

---

## 方式一：Android Studio 一键生成 APK (最推荐，耗时约 30 秒)
1. 下载并安装 [Android Studio](https://developer.android.com/studio)；
2. 解压本工程 ZIP，点击 **Open** 选择解压后的根目录；
3. 等待右下角 Gradle 同步完成；
4. 点击顶部菜单栏：
   `Build` -> `Build Bundle(s) / APK(s)` -> **`Build APK(s)`**；
5. 编译完成后，Android Studio 会在右下角弹出提示：
   *"APK(s) generated successfully for module 'app'"*，点击 **`locate`**；
6. 即可看到生成的 **`app-debug.apk`**，发送到安卓手机即可直接安装使用！

---

## 方式二：命令行一行命令编译
无需打开 Android Studio 界面，直接在终端执行：

### Windows 系统：
```cmd
gradlew.bat assembleDebug
```

### Mac / Linux 系统：
```bash
chmod +x gradlew
./gradlew assembleDebug
```

编译完成后，APK 生成在目录：
`app/build/outputs/apk/debug/app-debug.apk`

---

## 方式三：GitHub Actions 云端免费在线打包 (无需本地安装任何开发环境)
本工程已经预置了 `.github/workflows/build-apk.yml` 自动化构建流：
1. 创建一个新的 GitHub 仓库并将本工程文件上传；
2. GitHub 会自动触发构建任务；
3. 构建完成后，在仓库的 **Actions** 页面点击最新的一次构建；
4. 在底部的 **Artifacts** 区域即可直接下载编译好的 **`TransIME-debug-apk`**！
