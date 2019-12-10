# 标签传播算法（Label Propagation）<a name="ges_01_0039"></a>

## 概述<a name="section204471932366"></a>

标签传播算法（Label Propagation）是一种基于图的半监督学习方法，其基本思路是用已标记节点的标签信息去预测未标记节点的标签信息。利用样本间的关系建图，节点包括已标注和未标注数据，其边表示两个节点的相似度，节点的标签按相似度传递给其他节点。标签数据就像是一个源头，可以对无标签数据进行标注，节点的相似度越大，标签越容易传播。

## 适用场景<a name="section1103252295014"></a>

标签传播算法（Label Propagation）适用于资讯传播、广告推荐、社区发现等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  标签传播算法（Label Propagation）参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="15.151515151515152%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.090909090909092%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.161616161616163%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="10.101010101010102%" id="mcps1.2.7.1.4"><p id="p3578125211"><a name="p3578125211"></a><a name="p3578125211"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="38.36363636363637%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.131313131313131%" id="mcps1.2.7.1.6"><p id="p2984277163535"><a name="p2984277163535"></a><a name="p2984277163535"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.7.1.1 "><p id="p1143990987"><a name="p1143990987"></a><a name="p1143990987"></a>coveragence</p>
</td>
<td class="cellrowborder" valign="top" width="9.090909090909092%" headers="mcps1.2.7.1.2 "><p id="p11262161310820"><a name="p11262161310820"></a><a name="p11262161310820"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.7.1.3 "><p id="p104392003812"><a name="p104392003812"></a><a name="p104392003812"></a>收敛精度</p>
</td>
<td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.7.1.4 "><p id="p17722101015239"><a name="p17722101015239"></a><a name="p17722101015239"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="38.36363636363637%" headers="mcps1.2.7.1.5 "><p id="p11478162763216"><a name="p11478162763216"></a><a name="p11478162763216"></a>0~1，不包括0和1</p>
</td>
<td class="cellrowborder" valign="top" width="11.131313131313131%" headers="mcps1.2.7.1.6 "><p id="p40399900163535"><a name="p40399900163535"></a><a name="p40399900163535"></a>0.00001</p>
</td>
</tr>
<tr id="row144392001589"><td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.7.1.1 "><p id="p543916014814"><a name="p543916014814"></a><a name="p543916014814"></a>max_iterations</p>
</td>
<td class="cellrowborder" valign="top" width="9.090909090909092%" headers="mcps1.2.7.1.2 "><p id="p471715910916"><a name="p471715910916"></a><a name="p471715910916"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.7.1.3 "><p id="p1671779594"><a name="p1671779594"></a><a name="p1671779594"></a>最大迭代次数</p>
</td>
<td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.7.1.4 "><p id="p14722110202312"><a name="p14722110202312"></a><a name="p14722110202312"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="38.36363636363637%" headers="mcps1.2.7.1.5 "><p id="p12150173373213"><a name="p12150173373213"></a><a name="p12150173373213"></a>1~2000</p>
</td>
<td class="cellrowborder" valign="top" width="11.131313131313131%" headers="mcps1.2.7.1.6 "><p id="p51166496163535"><a name="p51166496163535"></a><a name="p51166496163535"></a>1000</p>
</td>
</tr>
<tr id="row5465953133112"><td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.7.1.1 "><p id="p47379111320"><a name="p47379111320"></a><a name="p47379111320"></a>initial</p>
</td>
<td class="cellrowborder" valign="top" width="9.090909090909092%" headers="mcps1.2.7.1.2 "><p id="p47374115329"><a name="p47374115329"></a><a name="p47374115329"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.7.1.3 "><p id="p177371711103210"><a name="p177371711103210"></a><a name="p177371711103210"></a>点上用作初始化标签的属性名称</p>
</td>
<td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.7.1.4 "><p id="p773741116326"><a name="p773741116326"></a><a name="p773741116326"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.36363636363637%" headers="mcps1.2.7.1.5 "><p id="p673781153220"><a name="p673781153220"></a><a name="p673781153220"></a>空或字符串。</p>
<a name="ul1767372612326"></a><a name="ul1767372612326"></a><ul id="ul1767372612326"><li>空：每个节点各自分配一个特有的初始化标签；适用于事先没有任何节点标注信息的情况。</li><li>字符串：将节点的对应的属性字段取值作为初始化标签（类型为string，对于未知标签的点，初始化标签字段赋空）；适用于已标注部分节点标签，预测未知节点标签的情况。</li></ul>
<div class="note" id="note122561359143216"><a name="note122561359143216"></a><a name="note122561359143216"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1025720593324"><a name="p1025720593324"></a><a name="p1025720593324"></a>当initial取值非空时，对于具有初始化标签的点，其数量应大于0，小于点总数。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="11.131313131313131%" headers="mcps1.2.7.1.6 "><p id="p47371411183216"><a name="p47371411183216"></a><a name="p47371411183216"></a>-</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

标签传播算法（Label Propagation）默认使用ID作为标签。

## 示例<a name="section9539286457"></a>

输入参数coverage=0.00001，max\_iterations=1000，计算得到带有不同标签的子图会展示在绘图区，节点颜色根据不同标签来区别，JSON结果会展示在查询结果区。

