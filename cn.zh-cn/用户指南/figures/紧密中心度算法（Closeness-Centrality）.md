# 紧密中心度算法（Closeness Centrality）<a name="ges_01_0037"></a>

## 概述<a name="section204471932366"></a>

紧密中心度算法（Closeness Centrality）计算一个节点到所有其他可达节点的最短距离的倒数，进行累积后归一化的值。紧密中心度可以用来衡量信息从该节点传输到其他节点的时间长短。节点的“Closeness Centrality“越大，其在所在图中的位置越靠近中心。

## 适用场景<a name="section3109557795146"></a>

紧密中心度算法（Closeness Centrality）适用于社交网络中关键节点发掘等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  紧密中心度算法（Closeness Centrality）参数说明

<a name="table171541644143718"></a>
<table><thead align="left"><tr id="row161721944123714"><th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.1"><p id="p717674433720"><a name="p717674433720"></a><a name="p717674433720"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.2"><p id="p121811744103714"><a name="p121811744103714"></a><a name="p121811744103714"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="26%" id="mcps1.2.7.1.3"><p id="p12182144413379"><a name="p12182144413379"></a><a name="p12182144413379"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.4"><p id="p956642214335"><a name="p956642214335"></a><a name="p956642214335"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.7.1.5"><p id="p618404493716"><a name="p618404493716"></a><a name="p618404493716"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.7.1.6"><p id="p14684145253314"><a name="p14684145253314"></a><a name="p14684145253314"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1318710443373"><td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.1 "><p id="p17190174423717"><a name="p17190174423717"></a><a name="p17190174423717"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p1519213448374"><a name="p1519213448374"></a><a name="p1519213448374"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.7.1.3 "><p id="p101974442378"><a name="p101974442378"></a><a name="p101974442378"></a>输入需要计算的节点ID</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.4 "><p id="p7566102213338"><a name="p7566102213338"></a><a name="p7566102213338"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.5 "><p id="p1720094418371"><a name="p1720094418371"></a><a name="p1720094418371"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p196854524335"><a name="p196854524335"></a><a name="p196854524335"></a>-</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section3956161017109"></a>

输入参数source=Lee，计算Lee节点的紧密中心度，JSON结果会展示在查询结果区。

