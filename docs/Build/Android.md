# Build for Android

目前我们使用 Ubuntu 和 Mac OS 作为宿主环境是没有问题的，Windows 平台可能需要 Msys 之类的东西

- 第一步，请先设置 NDK 的位置（本项目采用的 NDK 版本是 r21，用其他版本可能会有问题）
````
export NDK=/Users/lichi/ndk_test/android-ndk-r21
````

- 第二步，运行 init_android.sh , 来下载第三方库，和对第三方库进行交叉编译。
````
sh init_android.sh
````

- 第三步，运行 build_lib_android.sh 对 EyerLib 进行编译
````
sh build_lib_android.sh
````

- 第四步，运行 build_wand_android.sh 对 EyerVideoWand 进行编译
````
sh build_wand_android.sh
````

- 第五步，用 Android Studio 打开 EyerWandEditor 里的 Android 工程，进行编译和打包就行了

注意，默认使用 armv7a 的架构进行编译