### SVG�Ķ���
- SVG ָ������ʸ��ͼ�� (Scalable Vector Graphics)
- SVG ����������������Ļ���ʸ����ͼ��
- SVG ʹ�� XML ��ʽ����ͼ��
- SVG ͼ���ڷŴ��ı�ߴ���������ͼ����������������ʧ
- SVG ����ά�����˵ı�׼
- SVG ������ DOM �� XSL ֮��� W3C ��׼��һ������

### SVG������
- SVG �ɱ��ǳ���Ĺ��߶�ȡ���޸ģ�������±���
- SVG �� JPEG �� GIF ͼ����������ߴ��С���ҿ�ѹ���Ը�ǿ��
- SVG �ǿ�������
- SVG ͼ������κεķֱ����±��������ش�ӡ
- SVG ����ͼ���������½�������±��Ŵ�
- SVG ͼ���е��ı��ǿ�ѡ�ģ�ͬʱҲ�ǿ������ģ����ʺ�������ͼ��
- SVG ������ Java ����һ�����У���仰��֪����ɶ��˼......??,�д��Ժ��о���
- SVG �ǿ��ŵı�׼
- SVG �ļ��Ǵ���� XML

### SVG�Ļ����÷�
1. SVG ������`<svg>`Ԫ�ؿ�ʼ������������ǩ`<svg>`�͹رձ�ǩ </svg> �����Ǹ�Ԫ�ء�
2. width �� height ���Կ����ô� SVG �ĵ��Ŀ�Ⱥ͸߶ȡ�
3. version ���Կɶ�����ʹ�õ� SVG �汾.
4. xmlns ���Կɶ��� SVG �����ռ䡣

### SVG�Ļ���ͼ�Σ�6�֣�

* ���� `<rect>`
* Բ�� `<circle>`
* ��Բ `<ellipse>`
* �߶� `<line>`
* ���� `<polyline>`
* ����� `<polygon>`
* ���⣬����һ�ֱȽ����⣬Ҳ�ǹ��� **��ǿ** ��Ԫ��:
`path`

#### ����`<rect>`
```
<svg width="100%" height="100%" version="1.1">
<rect x="20" y="20" rx="5" ry="5" width="250" height="250"
style="fill:blue;stroke:pink;stroke-width:5;
fill-opacity:0.1;stroke-opacity:0.9"/>
</svg>
```
* width��height������εĿ�Ⱥ͸߶�;x��y,���������������е�λ�ã����������������Ͻ�(0,0)λ��;rx,ry,����ʹ���β���Բ��
* css��ʽ�ļ�
    * fill��������ε������ɫ fill-opcity:�������ɫ͸����
    * stroke: ������α߿����ɫ stroke-width������߿�Ŀ�� stroke-opacity���߿��͸����
    
#### Բ�� `<circle>`
```
<svg width="100%" height="100%" version="1.1">
<circle cx="100" cy="50" r="40" stroke="black"
stroke-width="2" fill="red"/>
</svg>
```
* cx,cy,r,�ֱ���Բ�ĵ�λ�����Բ�İ뾶
* css��ʽ��ʵ�;��εĶ�����

#### ��Բ `<ellipse>`
```
<svg width="100%" height="100%" version="1.1">
<ellipse cx="300" cy="150" rx="200" ry="80"
style="fill:rgb(200,100,50);
stroke:rgb(0,0,100);stroke-width:2"/>
</svg>
```
* cx,cy,rx,ry,�ֱ��ʾԲ�ĵ�λ�ã��Լ�ˮƽ�뾶���ʹ�ֱ�뾶

#### ·��`path`
```
<svg width="100%" height="100%" version="1.1">
<path d="M250 150 L150 350 L350 350 Z" />
</svg>
```
* ����ʼ��λ�� 250 150������λ�� 150 350��Ȼ������￪ʼ�� 350 350������� 250 150 �ر�·��
* ������������·������
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