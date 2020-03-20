# PageRank算法<a name="ges_01_0032"></a>

## 概述<a name="section204471932366"></a>

PageRank算法又称网页排名算法，是一种由搜索引擎根据网页（节点）之间相互的超链接进行计算的技术，用来体现网页（节点）的相关性和重要性。

-   如果一个网页被很多其他网页链接到，说明这个网页比较重要，也就是其PageRank值会相对较高。
-   如果一个PageRank值很高的网页链接到其他网页，那么被链接到的网页的PageRank值会相应地提高。

## 适用场景<a name="section2851136210245"></a>

PageRank算法适用于网页排序、社交网络重点人物挖掘等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  PageRank算法参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="16%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="13%" id="mcps1.2.7.1.4"><p id="p0785183919517"><a name="p0785183919517"></a><a name="p0785183919517"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="24%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.7.1.6"><p id="p8883058175257"><a name="p8883058175257"></a><a name="p8883058175257"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.1 "><p id="p1143990987"><a name="p1143990987"></a><a name="p1143990987"></a>alpha</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.7.1.2 "><p id="p82629131588"><a name="p82629131588"></a><a name="p82629131588"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p443910016812"><a name="p443910016812"></a><a name="p443910016812"></a>权重系数(又称阻尼系数)</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.4 "><p id="p17854397519"><a name="p17854397519"></a><a name="p17854397519"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.7.1.5 "><p id="p1375182054520"><a name="p1375182054520"></a><a name="p1375182054520"></a>0~1，不包括0和1</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.6 "><p id="p48439126175257"><a name="p48439126175257"></a><a name="p48439126175257"></a>0.85</p>
</td>
</tr>
<tr id="row144392001589"><td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.1 "><p id="p543916014814"><a name="p543916014814"></a><a name="p543916014814"></a>convergence</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.7.1.2 "><p id="p11262161310820"><a name="p11262161310820"></a><a name="p11262161310820"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p104392003812"><a name="p104392003812"></a><a name="p104392003812"></a>收敛精度</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.4 "><p id="p67851639451"><a name="p67851639451"></a><a name="p67851639451"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.7.1.5 "><p id="p195910142458"><a name="p195910142458"></a><a name="p195910142458"></a>0~1，不包括0和1</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.6 "><p id="p31255134175257"><a name="p31255134175257"></a><a name="p31255134175257"></a>0.00001</p>
</td>
</tr>
<tr id="row371539495"><td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.1 "><p id="p1871717918920"><a name="p1871717918920"></a><a name="p1871717918920"></a>max_iterations</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.7.1.2 "><p id="p471715910916"><a name="p471715910916"></a><a name="p471715910916"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p1671779594"><a name="p1671779594"></a><a name="p1671779594"></a>最大迭代次数</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.4 "><p id="p17785739658"><a name="p17785739658"></a><a name="p17785739658"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.7.1.5 "><p id="p92561811184518"><a name="p92561811184518"></a><a name="p92561811184518"></a>1~2000</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.6 "><p id="p48637939175257"><a name="p48637939175257"></a><a name="p48637939175257"></a>1000</p>
</td>
</tr>
<tr id="row139901027102910"><td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.1 "><p id="p13753301698"><a name="p13753301698"></a><a name="p13753301698"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.7.1.2 "><p id="p27531901695"><a name="p27531901695"></a><a name="p27531901695"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p1775316016919"><a name="p1775316016919"></a><a name="p1775316016919"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.4 "><p id="p87855391557"><a name="p87855391557"></a><a name="p87855391557"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.7.1.5 "><p id="p13151535595"><a name="p13151535595"></a><a name="p13151535595"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.6 "><p id="p47358972175257"><a name="p47358972175257"></a><a name="p47358972175257"></a>true</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   alpha决定跳转概率系数，也称为阻尼系数，是算法内的计算控制变量。  
>-   convergence定义每次迭代各个点相较于上次迭代变化的绝对值累加和上限，当小于这个值时认为计算收敛，算法停止。  

## 注意事项<a name="section3956161017109"></a>

收敛精度（convergence）设置较大值时，迭代会较快停止。

## 示例<a name="section19388125681119"></a>

输入参数alpha=0.85，coverage=0.00001，max\_iterations=1000，directed=true，计算结果中的top节点组成的子图会展示在绘图区，节点大小根据PageRank值的大小来区别，JSON结果会展示在查询结果区。

