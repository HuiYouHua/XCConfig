# XCConfig
关于使用配置文件切换工程环境

首先建一个Config文件夹

![文件夹](https://github.com/HuiYouHua/XCConfig/blob/master/ConfigDemo/4.png "文件夹")

里面分别有AdHoc.xcconfig、Debug.xcconfig、Release.xcconfig和Shared.xcconfig，其中AdHoc.xcconfig、Debug.xcconfig、Release.xcconfig分别对应三种运行环境，Shared.xcconfig为公共的配置。

设置每个环境对应的配置文件
![配置](https://github.com/HuiYouHua/XCConfig/blob/master/ConfigDemo/1.png "配置")



Shared.xcconfig中的GCC_PREPROCESSOR_DEFINITIONS为GCC预编译头参数，添加的配置如需进行调用则需要在GCC_PREPROCESSOR_DEFINITIONS = $(inherited)后添加，每个键值以空格分割，不能换行，等号两边不允许有空格。



添加完毕后可以看到
![配置](https://github.com/HuiYouHua/XCConfig/blob/master/ConfigDemo/2.png "配置")


![配置](https://github.com/HuiYouHua/XCConfig/blob/master/ConfigDemo/3.png "配置")

通过切换环境可以看到控制台打印不同的内容
