# 关联路径算法（n-Paths）<a name="ges_01_0052"></a>

## 概述<a name="section6298525295951"></a>

关联路径算法（n-Paths）用于寻找图中两节点之间在层关系内的n条路径。

## 适用场景<a name="section1451760010033"></a>

关联路径算法（n-Paths）适用于关系分析、路径规划、网络规划等场景。

## 参数说明<a name="section3818483210354"></a>

**表 1**  关联路径算法（n-Paths）参数说明

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
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p2140961710425"><a name="p2140961710425"></a><a name="p2140961710425"></a>输入路径的起点ID</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p2445131643916"><a name="p2445131643916"></a><a name="p2445131643916"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p5645743610425"><a name="p5645743610425"></a><a name="p5645743610425"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p964961610425"><a name="p964961610425"></a><a name="p964961610425"></a>-</p>
</td>
</tr>
<tr id="row1354819122815"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p7843173202816"><a name="p7843173202816"></a><a name="p7843173202816"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p2843232152811"><a name="p2843232152811"></a><a name="p2843232152811"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p20843332112810"><a name="p20843332112810"></a><a name="p20843332112810"></a>输入路径的终点ID</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p16843123242820"><a name="p16843123242820"></a><a name="p16843123242820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p118434321281"><a name="p118434321281"></a><a name="p118434321281"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p4354019192816"><a name="p4354019192816"></a><a name="p4354019192816"></a>-</p>
</td>
</tr>
<tr id="row44303816104111"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p5524824310425"><a name="p5524824310425"></a><a name="p5524824310425"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p4592270710425"><a name="p4592270710425"></a><a name="p4592270710425"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p2875176710425"><a name="p2875176710425"></a><a name="p2875176710425"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p25096169392"><a name="p25096169392"></a><a name="p25096169392"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p4719178410425"><a name="p4719178410425"></a><a name="p4719178410425"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p6443812510425"><a name="p6443812510425"></a><a name="p6443812510425"></a>false</p>
</td>
</tr>
<tr id="row1442014612715"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p16421762277"><a name="p16421762277"></a><a name="p16421762277"></a>n</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p242113652712"><a name="p242113652712"></a><a name="p242113652712"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p1942196102713"><a name="p1942196102713"></a><a name="p1942196102713"></a>路径个数</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p44214613279"><a name="p44214613279"></a><a name="p44214613279"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p16421176192718"><a name="p16421176192718"></a><a name="p16421176192718"></a>1~100</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p7421136142714"><a name="p7421136142714"></a><a name="p7421136142714"></a>10</p>
</td>
</tr>
<tr id="row042112682720"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p042176132710"><a name="p042176132710"></a><a name="p042176132710"></a>k</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p14211463277"><a name="p14211463277"></a><a name="p14211463277"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p16421146142718"><a name="p16421146142718"></a><a name="p16421146142718"></a>层数</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p1642116622714"><a name="p1642116622714"></a><a name="p1642116622714"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p1421126172715"><a name="p1421126172715"></a><a name="p1421126172715"></a>1~10</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p94211466272"><a name="p94211466272"></a><a name="p94211466272"></a>5</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section21511242104337"></a>

输入参数source=Lee，target=Alice，n=10，k=5，directed=false，计算结果会展示在绘图区，JSON结果会展示在查询结果区。

