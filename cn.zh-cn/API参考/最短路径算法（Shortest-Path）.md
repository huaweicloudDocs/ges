# 最短路径算法（Shortest Path）<a name="ges_01_0035"></a>

## 概述<a name="section204471932366"></a>

最短路径算法（Shortest Path）用以解决图论研究中的一个经典算法问题，旨在寻找图中两节点之间的最短路径。

## 适用场景<a name="section2555716895357"></a>

最短路径算法（Shortest Path）适用于路径规划、网络规划等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  最短路径算法（Shortest Path）参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="13.861386138613863%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.564356435643564%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.247524752475247%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.306930693069306%" id="mcps1.2.7.1.4"><p id="p119692498180"><a name="p119692498180"></a><a name="p119692498180"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="38.78217821782178%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="9.237623762376238%" id="mcps1.2.7.1.6"><p id="p19958237181732"><a name="p19958237181732"></a><a name="p19958237181732"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p1143990987"><a name="p1143990987"></a><a name="p1143990987"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p82629131588"><a name="p82629131588"></a><a name="p82629131588"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p443910016812"><a name="p443910016812"></a><a name="p443910016812"></a>输入路径的起点ID</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p19969174991814"><a name="p19969174991814"></a><a name="p19969174991814"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p19637130201011"><a name="p19637130201011"></a><a name="p19637130201011"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p6004471181732"><a name="p6004471181732"></a><a name="p6004471181732"></a>-</p>
</td>
</tr>
<tr id="row144392001589"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p543916014814"><a name="p543916014814"></a><a name="p543916014814"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p11262161310820"><a name="p11262161310820"></a><a name="p11262161310820"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p104392003812"><a name="p104392003812"></a><a name="p104392003812"></a>输入路径的终点ID</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p1896954920183"><a name="p1896954920183"></a><a name="p1896954920183"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p143915011811"><a name="p143915011811"></a><a name="p143915011811"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p16600125181732"><a name="p16600125181732"></a><a name="p16600125181732"></a>-</p>
</td>
</tr>
<tr id="row38613385112333"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p40676518112333"><a name="p40676518112333"></a><a name="p40676518112333"></a>weight</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p6463651112333"><a name="p6463651112333"></a><a name="p6463651112333"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p53793704112333"><a name="p53793704112333"></a><a name="p53793704112333"></a>边上权重</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p1496924971820"><a name="p1496924971820"></a><a name="p1496924971820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p1666044011283"><a name="p1666044011283"></a><a name="p1666044011283"></a>空或字符串</p>
<a name="ul27814585182326"></a><a name="ul27814585182326"></a><ul id="ul27814585182326"><li>空：边上的权重、距离默认为<span class="parmname" id="parmname64281841182434"><a name="parmname64281841182434"></a><a name="parmname64281841182434"></a>“1”</span>。</li><li>字符串：对应的边上的属性将作为权重，当某边没有对应属性时，权重将默认为1。<div class="note" id="note1763697295448"><a name="note1763697295448"></a><a name="note1763697295448"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p6598326895457"><a name="p6598326895457"></a><a name="p6598326895457"></a>边上权重应大于0。</p>
</div></div>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p2432921181732"><a name="p2432921181732"></a><a name="p2432921181732"></a>-</p>
</td>
</tr>
<tr id="row18578822113145"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p28489604113145"><a name="p28489604113145"></a><a name="p28489604113145"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p25956591113145"><a name="p25956591113145"></a><a name="p25956591113145"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p22109102113145"><a name="p22109102113145"></a><a name="p22109102113145"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p4969649161820"><a name="p4969649161820"></a><a name="p4969649161820"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p46006826113145"><a name="p46006826113145"></a><a name="p46006826113145"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p62848880181732"><a name="p62848880181732"></a><a name="p62848880181732"></a>false</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

最短路径算法（Shortest Path）只返回一条最短路径。

## 示例<a name="section9539286457"></a>

计算从Lee节点到Alice节点的一条最短路径。

输入参数source=Lee，target=Alice，weight=weights，directed=false。最短路径会展示在绘图区，JSON结果会展示在查询结果区。

