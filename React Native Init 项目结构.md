# React Native Init 项目结构

- **tests**

  测试文件夹，执行命令 “npm test”会调用此文件夹，在文件夹中需要引入待测试文件。

- **android**

  Android的原生开发目录，可以用Android Studio打开进行原生开发。

- **ios**

  Ios的原生开发目录，可以用Xcode打开进行原生开发。

- **node_modules**

  存放所有的项目依赖库，配置package.json之后执行“npm install”后自动创建的文件夹。

- **.babelrc**

  Babel的配置文件,Babel是一个广泛使用的转码器，可以将ES6代码转为ES5代码，从而在现有环境执行。babelrc用来设置转码规则和插件。

- **.buckconfig**

  buck的配置文件，buck是Facebook推出的一款高效率的App项目构建工具。

- **.flowconfig**

  Flow 是 Facebook 旗下一个为 JavaScript 进行静态类型检测的检测工具。它可以在 JavaScript 的项目中用来捕获常见的 bugs，比如隐式类型转换，空引用等等。

- **.gitattributes**

  git属性文件设定一些项目特殊的属性。比如要比较word文档的不同；对strings程序进行注册；合并冲突的时候不想合并某些文件等等。

- **.gitignore**

  用来配置git提交需要忽略的文件。

- **.watchmanconfig**

  用于监控bug文件和文件变化，并且可以出发指定的操作。

- **app.json**

  配置了name和displayName，不过没发现在哪里使用到了。（待研究。。）

- **index.android.js** 和 **index.ios.js**

  Android 和 Ios 入口文件，可以在android的MainApplication中的ReactNativeHost中重写getJSMainModuleName()方法更改; 在Ios的AppDelegate.m文件的didFinishLaunchingWithOptions方法中通过jsBundleURLForBundleRoot可以更改入口文件。

- **package.json**

  package.json定义了项目所需要的各种模块，以及项目的配置信息（比如名称、版本、许可证等元数据）。npm install命令根据这个配置文件，自动下载所需的模块，也就是配置项目所需的运行和开发环境。

- **yarn.lock**

  Yarn 是 一个由 Facebook 创建的新 JavaScript 包管理器；每次添加依赖或者更新包版本，yarn都会把相关版本信息写入yarn.lock文件。这样可以解决同一个项目在不同机器上环境不一致的问题。