# React Native 学习笔记

## 一. Hello World

1. `npm install -g react-native-cli`

   react-native-cli是一个终端命令，它可以完成其余的设置工作。它可以通过npm安装。刚才这条命令会往你的终端安装一个叫做`react-native`的命令。这个安装过程你只需要进行一次。

2. `react-native init AwesomeProject  --version 0.44.3`

   这个命令会初始化一个工程、下载React Native的所有源代码和依赖包，最后在`AwesomePrjoect/iOS/AwesomeProject.xcodeproj`和`AwesomeProject/android/app`下分别创建一个新的XCode工程和一个gradle工程。

   **注意**：**不加 --version 的话，init 会报错 **


![native1](img\native1.png)

## 二. Flex 布局

Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。

任何一个容器都可以指定为 Flex 布局。

```react
.box{
  display: flex;
}
```

**注意**

设为 Flex 布局以后，子元素的`float`、`clear`和`vertical-align`属性将失效。 

### （一）基本概念

采用 Flex 布局的元素，称为 Flex 容器（flex container），简称"容器"。它的所有子元素自动成为容器成员，称为 Flex 项目（flex item），简称"项目"。 

![native2](img\native2.png)

容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis）。主轴的开始位置（与边框的交叉点）叫做`main start`，结束位置叫做`main end`；交叉轴的开始位置叫做`cross start`，结束位置叫做`cross end`。

项目默认沿主轴排列。单个项目占据的主轴空间叫做`main size`，占据的交叉轴空间叫做`cross size`。

### （二）容器的属性

设置在容器上的属性包括：

- flex-direction ：属性决定主轴的方向（即项目的排列方向），默认值`row`。

- flex-wrap ：属性规定如果一条轴线排不下，如何换行，默认值`nowrap`。 

- flex-flow ：属性是`flex-direction`属性和`flex-wrap`属性的简写形式，默认值为`row nowrap`。 

- justify-content ：属性定义了项目在主轴上的对齐方式 ，默认值`flex-start`。

- align-items ：属性定义项目在交叉轴上如何对齐，默认值`stretch`。 

- align-content ：属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用，默认值`strech`。


具体示例：

1. flex-direction 

   ```
   .box {
     flex-direction: row | row-reverse | column | column-reverse;
   }
   ```

![native3](img\native3.png)

- `row`（默认值）：主轴为水平方向，起点在左端。

- `row-reverse`：主轴为水平方向，起点在右端。
- `column`：主轴为垂直方向，起点在上沿。
- `column-reverse`：主轴为垂直方向，起点在下沿。

2. flex-wrap

   ```
   .box{
     flex-wrap: nowrap | wrap | wrap-reverse;
   }
   ```

- `nowrap`（默认值）：不换行。

  ![native4](img\native4.png)

- `row-reverse`：换行，紧接上一行下方。

  ![native5](img\native5.png)

- `column`：换行，上一行向下移位。

  ![native6](img\native6.png)

3. flex-flow

   `flex-flow`属性是`flex-direction`属性和`flex-wrap`属性的简写形式，默认值为`row nowrap`。 

   ```
   .box {
     flex-flow: <flex-direction> || <flex-wrap>;
   }
   ```

4. justify-content

   ```
   .box {
     justify-content: flex-start | flex-end | center | space-between | space-around;
   }
   ```

它可能取5个值，具体对齐方式与轴的方向有关。下面假设主轴为从左到右。

- `flex-start`（默认值）：左对齐

- `flex-end`：右对齐

- `center`： 居中

- `space-between`：两端对齐，项目之间的间隔都相等。

- `space-around`：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。

  ![native7.](img\native7..png)

5. align-items

   ```
   .box {
     align-items: flex-start | flex-end | center | baseline | stretch;
   }
   ```

![native8](img\native8.png)

它可能取5个值。具体的对齐方式与交叉轴的方向有关，下面假设交叉轴从上到下。

- `flex-start`：交叉轴的起点对齐。
- `flex-end`：交叉轴的终点对齐。
- `center`：交叉轴的中点对齐。
- `baseline`: 项目的第一行文字的基线对齐。
- `stretch`（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。

align-content

`align-content`属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。

> ```
> .box {
>   align-content: flex-start | flex-end | center | space-between | space-around | stretch;
> }
> ```

![img](img\native9.png)

该属性可能取6个值。

- `flex-start`：与交叉轴的起点对齐。
- `flex-end`：与交叉轴的终点对齐。
- `center`：与交叉轴的中点对齐。
- `space-between`：与交叉轴两端对齐，轴线之间的间隔平均分布。
- `space-around`：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
- `stretch`（默认值）：轴线占满整个交叉轴。



