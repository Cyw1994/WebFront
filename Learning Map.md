# 陈艺文-SAPVT-记录文档

## 一， 学习计划

### 1. 前期准备

- [x] ##### （1）了解开发模式（ Done ）：

- 瀑布模式
- 迭代模式
- 敏捷开发
  - Scrum模式
  - 看板模式

- [ ] ##### （2）技术准备（ one week ）：

基础技术：

1. HTML5 + CSS3  + javascript ( 2-day-work )
2. ES6 新特性 + TypeScript ( 1-day-work )

项目相关：

1. 基础概念和特性
2. 基于项目框架的Redux, Navigation

- [ ] ##### （3）工具

- IDE：Vitural Studio Code
- Github
- Node.js + npm + gulp
- Tslint

## 二， 项目相关

1. #####  GitHub地址： <https://github.wdf.sap.corp/csc-chery>

   a)      奇瑞线索APP： cherymobile

   b)      奇瑞线索PC端： cheryweb

2. ##### JIRA地址： <https://sapjira.wdf.sap.corp/secure/Dashboard.jspa>

   a)      Scrum+ 看板模式中的需求任务管理

   b)      注意随时跟进自己的task

3. ##### 开发系统（APP）：

   还有**测试系统**及**生产系统**，我们的业务目前只在开发系统中，如果bug在测试系统或者生产系统中需要可以问我要测试系统及生产系统的地址，因为生产系统已经上线，没有重大bug，不能在直连生产系统

   a)      默认账号/密码： 13333333333/Abc123456

   b)      后台地址： <https://cherydealerservicedevf1d1d8c7d.cn1.hana.ondemand.com>

   c)      后台管理系统地址：[https://cherywebdev-f1d1d8c7d.dispatcher.cn1.hana.ondemand.com/index.html](https://cherywebdev-f1d1d8c7d.dispatcher.cn1.hana.ondemand.com/index.html#/users/employees)

4. ##### APP下载地址： 

   a)   D系统

​                 i.  Android: <https://fir.im/gtk9>

​                ii.  IOS: <https://fir.im/5sl4>

​	b)   Q系统 

​                 i. Android: <https://fir.im/8qcs>

​                ii. IOS: <https://fir.im/fjm6> 

三个系统   开发 ，测试， 产品系统

5. ##### UI Prototype

   a)      地址：  <https://9v264s.axshare.com/#g=1&p=home>

   b)      密码： 6666

6. ##### 高保真素材地址：

   a)      <https://sap-my.sharepoint.com/personal/min_zhuo_sap_com/_layouts/15/onedrive.aspx?e=5%3Af5dc71e52c234aa792e55b2cb50a59ec&id=%2Fpersonal%2Fmin_zhuo_sap_com%2FDocuments%2FSap_Chery_Lead&FolderCTID=0x0120005B80B550E2065B4BBE503BAFEAC2FA53>

## 三. 实际操作记录

### 0. 技术补充

### react-redux  react-thunk

### 1. 部署项目：

**预备工作**

- GitHub地址： <https://github.wdf.sap.corp/csc-chery> 
  1. 选择"Cherymobile"->"Branches"->"Dev"->"Clone "
- 项目目录：   <C:\WorkSpace\Sap\cherymobile-master>
- 安装NODE : https://nodejs.org/zh-cn/
- 安装JAVA SE ：需要8.x版本（不然Android不支持）

http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

- Java环境变量配置：
  1. 新增JAVA_HOME: 值为 JAVA JDK 所在目录
  2. 添加Path:  值为 JAVA JDK 所在目录/bin;  JAVA JRE 所在目录/bin
  3. 新增CLASSPATH:  .;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;  (注意前面有个 . )
- 安装Androd SDK: http://sdk.android-studio.org/
  1. 新建目录 Android/sdk 作为安装目录
  2. 打开 SDK Manager.exe 应用程序，安装SDK包 （推荐 all selected）
- 配置 Android 环境
  1. 新增SDK_HOME：值为Android SDK的安装目录 
  2. 添加Path：;%SDK_HOME%\tools;%SDK_HOME%\platform-tools; 

- 安装yarn：  https://yarnpkg.com/lang/zh-hans/dotall/#windows-stable
  1. 项目目录文件下，执行 yarn install (类似 npm install)

- 安装安卓模拟器：Genymotion (个人版) + VM VitualBox   https://www.genymotion.com/fun-zone/
  1.  “Settings" -> "ADB" -> "Use custom Android SDK tools" -> ”Browse" 选择 SDK 所在目录

**实际部署**

yarn install

打开Genymotion虚拟机

react-native run-android



https://github.wdf.sap.corp/csc-chery/cherymobile.git



![1531281231663](img\learn1.png)



**Git Hub 提交流程**

1. 代码修改

2. 打开**Git Desktop**已修改文件出现在的**Changes**上

   ![1531284303896](img\learn2.png)

   本地提交修改：

   ![1531285595821](C:\Users\i353670\Desktop\文件夹\Learning\img\lear7.png)

3. 选择**CurrentBranch**创建新的**New branch**

   **注意：选择之前应该首先先把Branch选择在Dev下，不然后面新Branch无法Based on Dev**

   ![1531284358860](img\learn3.png)

   创建窗口

   ![1531284590602](img\learn4.png)

   Name 为任务编号

   ![1531284671682](img\learn5.png)

   Based on Dev :

   ![1531285381907](img\learn6.png)

4. 把修改提交到Git Hub上，选择 **Publish branch**

   ![1531285648869](img\learn8.png)

5. 登陆网页上的GitHub，Pull Request

6. Set Viewer 选择他人审核

7. 等待审核通过，打包，等待测试通过，