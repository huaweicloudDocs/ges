# Gremlin查询<a name="ges_01_0024"></a>

## 操作场景<a name="section28251916185816"></a>

Gremlin是Apache Tinkerpop框架中使用的图遍历语言，使用Gremlin可以很方便的对图数据进行查询，进行图的修改、局部遍历和属性过滤等。

## 操作步骤<a name="section1059722175917"></a>

1.  进入图引擎编辑器页面，详细操作请参见[访问图引擎编辑器](访问图引擎编辑器.md)。
2.  在Gremlin查询区，输入查询语句，按“回车“键执行操作。

    常用的查询语句如下所示。

    -   点查询

        g.V\(\).limit\(100\)：查询所有点，但限制点的返回数量为100，也可以使用range\(x, y\)的算子，返回区间内的点数量。

        g.V\(\).hasLabel\('movie'\) ：查询点的label值为'movie'的点。

        g.V\('11'\) ：查询id为‘11’的点。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >不推荐使用“g.V\(\)“语法，由于点过大时，这种查询方式影响展示效果。  

    -   边查询

        g.E\(\)：查询所有边，不推荐使用，边数过大时，这种查询方式不合理，一般需要添加过滤条件或限制返回数量。

        g.E\('55-81-5'\)：查询边id为‘55-81-5’的边。

        g.E\(\).hasLabel\('rate'\)：查询label为‘rate’的边。

        g.V\('46'\).outE\('rate'\)：查询点id为‘46’所有label为‘rate’的边。

    -   属性查询

        g.V\(\).limit\(3\).valueMap\(\)：查询点的所有属性（可填参数，表示只查询该点， 一个点所有属性一行结果）。

        g.V\(\).limit\(1\).label\(\)：查询点的label。

        g.V\(\).limit\(10\).values\('userid'\)：查询点的name属性（可不填参数，表示查询所有属性， 一个点每个属性一行结果，只有value，没有key）。

    -   新增点
        -   方式1：

            a = graph.addVertex\(label,'user',id,'500','age','18-24'\)：新增点，Label为user，ID为500，age为18-24。

        -   方式2：

            g.addV\('user'\).property\(id,'600'\).property\('age','18-24'\)：新增点，Label为user，ID为500，age为18-24。


    -   删除点

        g.V\('600'\).drop\(\)：删除ID为600的点。

    -   新增边
        -   方式1：

            a = graph.addVertex\(label,'user',id,'501','age','18-24'\);

            b = graph.addVertex\(label,'movie',id,'502','title','love'\);

            a.addEdge\('rate',b,'Rating','4'\)：新增边，边的两个点ID分别为501、502。

        -   方式2：

            a = g.addV\('user'\).property\(id,'501'\).property\('age','18-24'\);

            b = g.addV\('movie'\).property\(id,'502'\).property\('title','love'\);

            g.addE\('rate'\).property\('Rating', '4'\).from\(a\).to\(b\)：新增边，边的两个点ID分别为501、502。


    -   删除边

        g.E\('501-502-0'\).drop\(\)：删除ID为“501-502-0”的边。



## 参考信息<a name="section782724155910"></a>

GES服务中的Gremlin与开源的差异点如[表1](#table144301911382)所示。

**表 1**  差异点

<a name="table144301911382"></a>
<table><thead align="left"><tr id="row1643118963812"><th class="cellrowborder" valign="top" width="32%" id="mcps1.2.3.1.1"><p id="p2043119917388"><a name="p2043119917388"></a><a name="p2043119917388"></a>差异点</p>
</th>
<th class="cellrowborder" valign="top" width="68%" id="mcps1.2.3.1.2"><p id="p19431593382"><a name="p19431593382"></a><a name="p19431593382"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row104311392388"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p043159173813"><a name="p043159173813"></a><a name="p043159173813"></a>Vertex and Edge IDs</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p194311499381"><a name="p194311499381"></a><a name="p194311499381"></a>Edge id是由source vertex的id，target vertex的id，以及区分重边的index，通过‘-’字符连接，sid-tid-index。Edge id和vertex id必须是String类型。</p>
</td>
</tr>
<tr id="row34311096389"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p14313913812"><a name="p14313913812"></a><a name="p14313913812"></a>User Supplied IDs</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p3431897380"><a name="p3431897380"></a><a name="p3431897380"></a>只有点id允许用户提供，不能带‘-’字符。</p>
</td>
</tr>
<tr id="row043111953816"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p1543115912387"><a name="p1543115912387"></a><a name="p1543115912387"></a>Vertex Property IDs</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p13431993389"><a name="p13431993389"></a><a name="p13431993389"></a>和边的属性一样，点属性没有id，返回的id为点的id。</p>
</td>
</tr>
<tr id="row4431893387"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p343110912382"><a name="p343110912382"></a><a name="p343110912382"></a>Vertex and Edge Property</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p164311994382"><a name="p164311994382"></a><a name="p164311994382"></a>GES的vertex 和 edge property由元数据文件定义，所以没有真的增加以及删除property的方法，只有修改以及清除的操作，类似property()，remove()等方法，都是修改属性的值，property()设置的值由参数决定，remove()，会把string类属性，变为空字符串，数字类属性变为0。List属性变为空list。</p>
</td>
</tr>
<tr id="row18431209173819"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p4431129183810"><a name="p4431129183810"></a><a name="p4431129183810"></a>Variables</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p1743119983811"><a name="p1743119983811"></a><a name="p1743119983811"></a>GES graph structure不支持variables特性。</p>
</td>
</tr>
<tr id="row4431196383"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p143119919382"><a name="p143119919382"></a><a name="p143119919382"></a>Cardinality</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p14311793387"><a name="p14311793387"></a><a name="p14311793387"></a>GES支持single 和list cardinality，GES的点的属性的value类型由元数据文件定义，所以设置propety的值的时候，不会增加新的属性，之后修改对应的定义的属性。</p>
</td>
</tr>
<tr id="row44311899388"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p16431797385"><a name="p16431797385"></a><a name="p16431797385"></a>Transactions</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p14313920385"><a name="p14313920385"></a><a name="p14313920385"></a>GES的Gremlin实现不支持显式地使用Transactions。</p>
</td>
</tr>
</tbody>
</table>

使用feature函数可以看到当前支持的Gremlin特性，显示false表示GES服务不支持此特性，显示为true表示GES服务支持此特性，特性详情可参考[Gremlin官网](http://tinkerpop.apache.org/docs/current/reference/#_features)。

```
gremlin> graph.features()
==>FEATURES
```

>![](public_sys-resources/icon-note.gif) **说明：**   
>目前暂时不支持以下step命令：  
>-   tryNext\(\)  
>-   explain\(\)  
>-   tree\(\)  

