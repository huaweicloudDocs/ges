# k跳算法（k-hop）<a name="ges_01_0034"></a>

## 概述<a name="section204471932366"></a>

k跳算法（k-hop）从起点出发，通过宽度优先搜索（BFS），找出k层与之关联的所有节点。找到的子图称为起点的“ego-net“。k跳算法会返回ego-net中节点的个数。

## 适用场景<a name="section5149232895640"></a>

k跳算法（k-hop）适用于关系发现、影响力预测、好友推荐等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  k跳算法（k-hop）参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="25.15%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="12.520000000000001%" id="mcps1.2.7.1.4"><p id="p6151173011175"><a name="p6151173011175"></a><a name="p6151173011175"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="22.33%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.2.7.1.6"><p id="p29310607141819"><a name="p29310607141819"></a><a name="p29310607141819"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.1 "><p id="p1143990987"><a name="p1143990987"></a><a name="p1143990987"></a>k</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p82629131588"><a name="p82629131588"></a><a name="p82629131588"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.15%" headers="mcps1.2.7.1.3 "><p id="p443910016812"><a name="p443910016812"></a><a name="p443910016812"></a>跳数</p>
</td>
<td class="cellrowborder" valign="top" width="12.520000000000001%" headers="mcps1.2.7.1.4 "><p id="p131511230151712"><a name="p131511230151712"></a><a name="p131511230151712"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="22.33%" headers="mcps1.2.7.1.5 "><p id="p5439601785"><a name="p5439601785"></a><a name="p5439601785"></a>1~10</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.6 "><p id="p25348953141819"><a name="p25348953141819"></a><a name="p25348953141819"></a>-</p>
</td>
</tr>
<tr id="row144392001589"><td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.1 "><p id="p543916014814"><a name="p543916014814"></a><a name="p543916014814"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p11262161310820"><a name="p11262161310820"></a><a name="p11262161310820"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.15%" headers="mcps1.2.7.1.3 "><p id="p104392003812"><a name="p104392003812"></a><a name="p104392003812"></a>节点的ID</p>
</td>
<td class="cellrowborder" valign="top" width="12.520000000000001%" headers="mcps1.2.7.1.4 "><p id="p17152163017175"><a name="p17152163017175"></a><a name="p17152163017175"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="22.33%" headers="mcps1.2.7.1.5 "><p id="p143915011811"><a name="p143915011811"></a><a name="p143915011811"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.6 "><p id="p39999332141819"><a name="p39999332141819"></a><a name="p39999332141819"></a>-</p>
</td>
</tr>
<tr id="row10862634141528"><td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.1 "><p id="p7458176141528"><a name="p7458176141528"></a><a name="p7458176141528"></a>mode</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p132526141528"><a name="p132526141528"></a><a name="p132526141528"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.15%" headers="mcps1.2.7.1.3 "><p id="p10734685141528"><a name="p10734685141528"></a><a name="p10734685141528"></a>方向：</p>
<a name="ul61647365181433"></a><a name="ul61647365181433"></a><ul id="ul61647365181433"><li>OUT：沿出边跳</li><li>IN：沿入边跳</li><li>ALL：双向跳</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.520000000000001%" headers="mcps1.2.7.1.4 "><p id="p515263051719"><a name="p515263051719"></a><a name="p515263051719"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="22.33%" headers="mcps1.2.7.1.5 "><p id="p64203189141528"><a name="p64203189141528"></a><a name="p64203189141528"></a>OUT，IN，ALL</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.6 "><p id="p18720472141819"><a name="p18720472141819"></a><a name="p18720472141819"></a>OUT</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

-   k值越大，覆盖的点越广。
-   根据六度空间理论，社交网上6跳可以覆盖到所有人。
-   BFS按边搜索。

## 示例<a name="section9539286457"></a>

计算从Lee节点出发三跳关系组成的子图。

输入参数k=3，source=Lee，mode=OUT。子图会展示在绘图区，JSON结果会展示在查询结果区。

