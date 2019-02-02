# Louvain算法<a name="ges_01_0040"></a>

## 概述<a name="section204471932366"></a>

Louvain算法是基于模块度的社区发现算法，该算法在效率和效果上都表现较好，并且能够发现层次性的社区结构，其优化目标是最大化整个社区网络的模块度。

## 适用场景<a name="section383804394850"></a>

Louvain算法适用于社团挖掘、层次化聚类等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  Louvain算法参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="15.841584158415841%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="7.920792079207921%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.81188118811881%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="8.91089108910891%" id="mcps1.2.7.1.4"><p id="p18722191018233"><a name="p18722191018233"></a><a name="p18722191018233"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="30.693069306930692%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.7.1.6"><p id="p38652927163737"><a name="p38652927163737"></a><a name="p38652927163737"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="15.841584158415841%" headers="mcps1.2.7.1.1 "><p id="p1143990987"><a name="p1143990987"></a><a name="p1143990987"></a>coveragence</p>
</td>
<td class="cellrowborder" valign="top" width="7.920792079207921%" headers="mcps1.2.7.1.2 "><p id="p11262161310820"><a name="p11262161310820"></a><a name="p11262161310820"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.3 "><p id="p104392003812"><a name="p104392003812"></a><a name="p104392003812"></a>收敛精度</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p17722101015239"><a name="p17722101015239"></a><a name="p17722101015239"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.7.1.5 "><p id="p33609923318"><a name="p33609923318"></a><a name="p33609923318"></a>0~1，不包括0和1</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.6 "><p id="p43879365163737"><a name="p43879365163737"></a><a name="p43879365163737"></a>0.00001</p>
</td>
</tr>
<tr id="row144392001589"><td class="cellrowborder" valign="top" width="15.841584158415841%" headers="mcps1.2.7.1.1 "><p id="p543916014814"><a name="p543916014814"></a><a name="p543916014814"></a>max_iterations</p>
</td>
<td class="cellrowborder" valign="top" width="7.920792079207921%" headers="mcps1.2.7.1.2 "><p id="p471715910916"><a name="p471715910916"></a><a name="p471715910916"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.3 "><p id="p1671779594"><a name="p1671779594"></a><a name="p1671779594"></a>最大迭代次数</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p14722110202312"><a name="p14722110202312"></a><a name="p14722110202312"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.7.1.5 "><p id="p1149201253314"><a name="p1149201253314"></a><a name="p1149201253314"></a>1~2000</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.6 "><p id="p64567713163737"><a name="p64567713163737"></a><a name="p64567713163737"></a>100</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

Louvain算法只生成最后的社区结果，不保存层次化结果。

## 示例<a name="section9539286457"></a>

输入参数coverage=0.00001，max\_iterations=100，计算得到不同社区的子图会展示在绘图区，节点颜色根据不同社区来区别，JSON结果会展示在查询结果区。

