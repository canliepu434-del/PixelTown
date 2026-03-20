# 像素小镇 - Android 源码

## 快速打包（3种方式）

### 方式一：Android Studio（推荐）
1. 下载并安装 [Android Studio](https://developer.android.com/studio)
2. 打开此文件夹（File → Open）
3. 等待 Gradle 同步完成（首次需联网下载依赖）
4. 点击顶部菜单 Build → Build Bundle(s)/APK(s) → Build APK(s)
5. APK 在 app/build/outputs/apk/debug/app-debug.apk

### 方式二：命令行打包
```bash
# 进入项目目录
cd PixelTown
# 给 gradlew 执行权限（Mac/Linux）
chmod +x gradlew
# 打包 debug APK
./gradlew assembleDebug
# Windows 用：
gradlew.bat assembleDebug
```

### 方式三：在线打包（无需安装任何软件）
1. 注册 [Appetize.io](https://appetize.io) 或
2. 使用 [GitHub Actions](https://github.com) - 把项目上传到 GitHub，添加 Android Build workflow

## APK 特性
- ✅ 真正全屏（无状态栏/导航栏）
- ✅ 强制横屏
- ✅ 沉浸式模式（IMMERSIVE_STICKY）
- ✅ localStorage 存档正常
- ✅ 屏幕常亮
- ✅ 最低支持 Android 5.0 (API 21)

## 文件说明
- app/src/main/assets/game.html - 游戏本体（902KB）
- app/src/main/java/.../MainActivity.java - WebView 壳
- app/src/main/AndroidManifest.xml - 权限和配置
