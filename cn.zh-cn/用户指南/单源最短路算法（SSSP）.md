# 单源最短路算法（SSSP）<a name="ges_01_0051"></a>

## 概述<a name="section6298525295951"></a>

单源最短路算法（SSSP）计算了图论中的一个经典问题，给出从给定的一个节点（称为源节点）出发到其余各节点的最短路径长度。

## 适用场景<a name="section1451760010033"></a>

单源最短路算法（SSSP）适用于网络路由、路径规划等场景。

## 参数说明<a name="section3818483210354"></a>

**表 1**  单源最短路算法（SSSP）参数说明

<a name="table18500810104111"></a>
<table><thead align="left"><tr id="row18009483104111"><th class="cellrowborder" valign="top" width="13.861386138613863%" id="mcps1.2.7.1.1"><p id="p6644426810425"><a name="p6644426810425"></a><a name="p6644426810425"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.861386138613863%" id="mcps1.2.7.1.2"><p id="p1327662710425"><a name="p1327662710425"></a><a name="p1327662710425"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="25.742574257425744%" id="mcps1.2.7.1.3"><p id="p166499410425"><a name="p166499410425"></a><a name="p166499410425"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="8.91089108910891%" id="mcps1.2.7.1.4"><p id="p10389144111270"><a name="p10389144111270"></a><a name="p10389144111270"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="18.81188118811881%" id="mcps1.2.7.1.5"><p id="p64685010425"><a name="p64685010425"></a><a name="p64685010425"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="18.81188118811881%" id="mcps1.2.7.1.6"><p id="p5239490710425"><a name="p5239490710425"></a><a name="p5239490710425"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row66427667104111"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p3138414910425"><a name="p3138414910425"></a><a name="p3138414910425"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p5908813510425"><a name="p5908813510425"></a><a name="p5908813510425"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p2140961710425"><a name="p2140961710425"></a><a name="p2140961710425"></a>节点的ID。</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p5389154132712"><a name="p5389154132712"></a><a name="p5389154132712"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p5645743610425"><a name="p5645743610425"></a><a name="p5645743610425"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p964961610425"><a name="p964961610425"></a><a name="p964961610425"></a>-</p>
</td>
</tr>
<tr id="row44303816104111"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p5524824310425"><a name="p5524824310425"></a><a name="p5524824310425"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p4592270710425"><a name="p4592270710425"></a><a name="p4592270710425"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p2875176710425"><a name="p2875176710425"></a><a name="p2875176710425"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p183891241162715"><a name="p183891241162715"></a><a name="p183891241162715"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p4719178410425"><a name="p4719178410425"></a><a name="p4719178410425"></a>true或false。</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p6443812510425"><a name="p6443812510425"></a><a name="p6443812510425"></a>true</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section21511242104337"></a>

计算从Lee节点出发，到其余各节点的最短路径长度。

输入参数source=Lee，directed=true。

