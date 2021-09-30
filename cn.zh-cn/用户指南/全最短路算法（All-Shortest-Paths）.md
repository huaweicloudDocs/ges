# 全最短路算法（All Shortest Paths）<a name="ges_01_0050"></a>

## 概述<a name="section26129174104558"></a>

全最短路径算法（All Shortest Paths）用以解决图论研究中的一个经典算法问题，旨在寻找图中两节点之间的所有最短路径。

## 适用场景<a name="section2237215295232"></a>

全最短路径算法（All Shortest Paths）适用于路径设计、网络规划等场景。

## 参数说明<a name="section3518149410536"></a>

**表 1**  全最短路径算法（All Shortest Paths）参数说明

<a name="table5824809911026"></a>
<table><thead align="left"><tr id="row6610076011026"><th class="cellrowborder" valign="top" width="15%" id="mcps1.2.7.1.1"><p id="p6032374611422"><a name="p6032374611422"></a><a name="p6032374611422"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.99%" id="mcps1.2.7.1.2"><p id="p5438523011422"><a name="p5438523011422"></a><a name="p5438523011422"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.01%" id="mcps1.2.7.1.3"><p id="p4312753511422"><a name="p4312753511422"></a><a name="p4312753511422"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.4"><p id="p19762155771915"><a name="p19762155771915"></a><a name="p19762155771915"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="22%" id="mcps1.2.7.1.5"><p id="p366948511422"><a name="p366948511422"></a><a name="p366948511422"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.2.7.1.6"><p id="p2879287911422"><a name="p2879287911422"></a><a name="p2879287911422"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row5255330211026"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.7.1.1 "><p id="p6574096111422"><a name="p6574096111422"></a><a name="p6574096111422"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="11.99%" headers="mcps1.2.7.1.2 "><p id="p2341763311422"><a name="p2341763311422"></a><a name="p2341763311422"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.01%" headers="mcps1.2.7.1.3 "><p id="p1778010111422"><a name="p1778010111422"></a><a name="p1778010111422"></a>输入路径的起点ID</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.4 "><p id="p29637115331"><a name="p29637115331"></a><a name="p29637115331"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.7.1.5 "><p id="p3090207011422"><a name="p3090207011422"></a><a name="p3090207011422"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.7.1.6 "><p id="p2003970711422"><a name="p2003970711422"></a><a name="p2003970711422"></a>-</p>
</td>
</tr>
<tr id="row552541311026"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.7.1.1 "><p id="p4632307511422"><a name="p4632307511422"></a><a name="p4632307511422"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="11.99%" headers="mcps1.2.7.1.2 "><p id="p6118162711422"><a name="p6118162711422"></a><a name="p6118162711422"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.01%" headers="mcps1.2.7.1.3 "><p id="p5676473911422"><a name="p5676473911422"></a><a name="p5676473911422"></a>输入路径的终点ID</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.4 "><p id="p996915133317"><a name="p996915133317"></a><a name="p996915133317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.7.1.5 "><p id="p3454112311422"><a name="p3454112311422"></a><a name="p3454112311422"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.7.1.6 "><p id="p4636758811422"><a name="p4636758811422"></a><a name="p4636758811422"></a>-</p>
</td>
</tr>
<tr id="row985243211026"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.7.1.1 "><p id="p4621343711422"><a name="p4621343711422"></a><a name="p4621343711422"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="11.99%" headers="mcps1.2.7.1.2 "><p id="p94607411422"><a name="p94607411422"></a><a name="p94607411422"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.01%" headers="mcps1.2.7.1.3 "><p id="p1859947811422"><a name="p1859947811422"></a><a name="p1859947811422"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.4 "><p id="p187631257121913"><a name="p187631257121913"></a><a name="p187631257121913"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.7.1.5 "><p id="p302914011422"><a name="p302914011422"></a><a name="p302914011422"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.7.1.6 "><p id="p6075974311422"><a name="p6075974311422"></a><a name="p6075974311422"></a>false</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section4706522711554"></a>

无。

## 示例<a name="section5531293611610"></a>

输入参数source =Lee，target =Alice，directed=false。计算结果会展示在绘图区，JSON结果会展示在查询结果区。

