# 点集最短路（Shortest Path of Vertex Sets）<a name="ges_01_0054"></a>

## 概述<a name="section6298525295951"></a>

点集最短路算法（Shortest Path of Vertex Sets）用于发现两个点集之间的最短路径。

## 适用场景<a name="section1451760010033"></a>

点集最短路算法（Shortest Path of Vertex Sets）适用于互联网社交、金融风控、路网交通、物流配送等场景下的区块之间关系分析。

## 参数说明<a name="section3818483210354"></a>

**表 1**  点集最短路算法（Shortest Path of Vertex Sets）参数说明

<a name="table18500810104111"></a>
<table><thead align="left"><tr id="row18009483104111"><th class="cellrowborder" valign="top" width="11.415841584158416%" id="mcps1.2.7.1.1"><p id="p6644426810425"><a name="p6644426810425"></a><a name="p6644426810425"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.91089108910891%" id="mcps1.2.7.1.2"><p id="p1327662710425"><a name="p1327662710425"></a><a name="p1327662710425"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.86138613861386%" id="mcps1.2.7.1.3"><p id="p166499410425"><a name="p166499410425"></a><a name="p166499410425"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.455445544554456%" id="mcps1.2.7.1.4"><p id="p10389144111270"><a name="p10389144111270"></a><a name="p10389144111270"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="41.15841584158416%" id="mcps1.2.7.1.5"><p id="p64685010425"><a name="p64685010425"></a><a name="p64685010425"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.198019801980198%" id="mcps1.2.7.1.6"><p id="p5239490710425"><a name="p5239490710425"></a><a name="p5239490710425"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row66427667104111"><td class="cellrowborder" valign="top" width="11.415841584158416%" headers="mcps1.2.7.1.1 "><p id="p3138414910425"><a name="p3138414910425"></a><a name="p3138414910425"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="9.91089108910891%" headers="mcps1.2.7.1.2 "><p id="p5908813510425"><a name="p5908813510425"></a><a name="p5908813510425"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.86138613861386%" headers="mcps1.2.7.1.3 "><p id="p2140961710425"><a name="p2140961710425"></a><a name="p2140961710425"></a>起点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="9.455445544554456%" headers="mcps1.2.7.1.4 "><p id="p2445131643916"><a name="p2445131643916"></a><a name="p2445131643916"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="41.15841584158416%" headers="mcps1.2.7.1.5 "><p id="p14473161318277"><a name="p14473161318277"></a><a name="p14473161318277"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p847331310275"><a name="p847331310275"></a><a name="p847331310275"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="10.198019801980198%" headers="mcps1.2.7.1.6 "><p id="p964961610425"><a name="p964961610425"></a><a name="p964961610425"></a>-</p>
</td>
</tr>
<tr id="row1354819122815"><td class="cellrowborder" valign="top" width="11.415841584158416%" headers="mcps1.2.7.1.1 "><p id="p7843173202816"><a name="p7843173202816"></a><a name="p7843173202816"></a>targets</p>
</td>
<td class="cellrowborder" valign="top" width="9.91089108910891%" headers="mcps1.2.7.1.2 "><p id="p2843232152811"><a name="p2843232152811"></a><a name="p2843232152811"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.86138613861386%" headers="mcps1.2.7.1.3 "><p id="p20843332112810"><a name="p20843332112810"></a><a name="p20843332112810"></a>终点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="9.455445544554456%" headers="mcps1.2.7.1.4 "><p id="p16843123242820"><a name="p16843123242820"></a><a name="p16843123242820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="41.15841584158416%" headers="mcps1.2.7.1.5 "><p id="p447461312712"><a name="p447461312712"></a><a name="p447461312712"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p947441318273"><a name="p947441318273"></a><a name="p947441318273"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="10.198019801980198%" headers="mcps1.2.7.1.6 "><p id="p4354019192816"><a name="p4354019192816"></a><a name="p4354019192816"></a>-</p>
</td>
</tr>
<tr id="row44303816104111"><td class="cellrowborder" valign="top" width="11.415841584158416%" headers="mcps1.2.7.1.1 "><p id="p5524824310425"><a name="p5524824310425"></a><a name="p5524824310425"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9.91089108910891%" headers="mcps1.2.7.1.2 "><p id="p4592270710425"><a name="p4592270710425"></a><a name="p4592270710425"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.86138613861386%" headers="mcps1.2.7.1.3 "><p id="p2875176710425"><a name="p2875176710425"></a><a name="p2875176710425"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.455445544554456%" headers="mcps1.2.7.1.4 "><p id="p25096169392"><a name="p25096169392"></a><a name="p25096169392"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="41.15841584158416%" headers="mcps1.2.7.1.5 "><p id="p4719178410425"><a name="p4719178410425"></a><a name="p4719178410425"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="10.198019801980198%" headers="mcps1.2.7.1.6 "><p id="p6443812510425"><a name="p6443812510425"></a><a name="p6443812510425"></a>false</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>当点的ID中含有逗号时，需在此ID上加上双引号，例如：电影“Paris, je taime”以及“Alice”两个ID作为sources时，写做：""Paris, je taime",Alice"  

## 示例<a name="section21511242104337"></a>

输入directed=true，sources= "Alice,Nana"，targets= "Lily,Amy"  ，JSON结果会展示在查询结果区。

