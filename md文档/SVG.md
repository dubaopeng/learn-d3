### SVG的定义
- SVG 指可伸缩矢量图形 (Scalable Vector Graphics)
- SVG 用来定义用于网络的基于矢量的图形
- SVG 使用 XML 格式定义图形
- SVG 图像在放大或改变尺寸的情况下其图形质量不会有所损失
- SVG 是万维网联盟的标准
- SVG 与诸如 DOM 和 XSL 之类的 W3C 标准是一个整体

### SVG的优势
- SVG 可被非常多的工具读取和修改（比如记事本）
- SVG 与 JPEG 和 GIF 图像比起来，尺寸更小，且可压缩性更强。
- SVG 是可伸缩的
- SVG 图像可在任何的分辨率下被高质量地打印
- SVG 可在图像质量不下降的情况下被放大
- SVG 图像中的文本是可选的，同时也是可搜索的（很适合制作地图）
- SVG 可以与 Java 技术一起运行（这句话不知道是啥意思......??,有待以后研究）
- SVG 是开放的标准
- SVG 文件是纯粹的 XML

### SVG的基本用法
1. SVG 代码以`<svg>`元素开始，包括开启标签`<svg>`和关闭标签 </svg> 。这是根元素。
2. width 和 height 属性可设置此 SVG 文档的宽度和高度。
3. version 属性可定义所使用的 SVG 版本.
4. xmlns 属性可定义 SVG 命名空间。

### SVG的基本图形（6种）

* 矩形 `<rect>`
* 圆形 `<circle>`
* 椭圆 `<ellipse>`
* 线段 `<line>`
* 折线 `<polyline>`
* 多边形 `<polygon>`
* 另外，还有一种比较特殊，也是功能 **最强** 的元素:
`path`

#### 矩形`<rect>`
```
<svg width="100%" height="100%" version="1.1">
<rect x="20" y="20" rx="5" ry="5" width="250" height="250"
style="fill:blue;stroke:pink;stroke-width:5;
fill-opacity:0.1;stroke-opacity:0.9"/>
</svg>
```
* width，height定义矩形的宽度和高度;x，y,定义矩形在浏览器中的位置，相对于浏览器的左上角(0,0)位置;rx,ry,可以使矩形产生圆角
* css样式文件
    * fill：定义矩形的填充颜色 fill-opcity:定义填充色透明度
    * stroke: 定义矩形边框的颜色 stroke-width：定义边框的宽度 stroke-opacity：边框的透明度
    
#### 圆形 `<circle>`
```
<svg width="100%" height="100%" version="1.1">
<circle cx="100" cy="50" r="40" stroke="black"
stroke-width="2" fill="red"/>
</svg>
```
* cx,cy,r,分别定义圆心的位置与该圆的半径
* css样式其实和矩形的定义差不多

#### 椭圆 `<ellipse>`
```
<svg width="100%" height="100%" version="1.1">
<ellipse cx="300" cy="150" rx="200" ry="80"
style="fill:rgb(200,100,50);
stroke:rgb(0,0,100);stroke-width:2"/>
</svg>
```
* cx,cy,rx,ry,分别表示圆心的位置，以及水平半径，和垂直半径

#### 路径`path`
```
<svg width="100%" height="100%" version="1.1">
<path d="M250 150 L150 350 L350 350 Z" />
</svg>
```
* 它开始于位置 250 150，到达位置 150 350，然后从那里开始到 350 350，最后在 250 150 关闭路径
* 常用命令用于路径数据
    * M = moveto
    * L = lineto
    * H = horizontal lineto
    * V = vertical lineto
    * C = curveto
    * S = smooth curveto
    * Q = quadratic Belzier curve
    * T = smooth quadratic Belzier curveto
    * A = elliptical Arc
    * Z = closepath