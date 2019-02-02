# 全最短路（All Shortest Paths）<a name="ges_03_0082"></a>

**表 1**  parameters参数说明

<a name="table5824809911026"></a>
<table><thead align="left"><tr id="row6610076011026"><th class="cellrowborder" valign="top" width="15%" id="mcps1.2.7.1.1"><p id="p6032374611422"><a name="p6032374611422"></a><a name="p6032374611422"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.2"><p id="p5438523011422"><a name="p5438523011422"></a><a name="p5438523011422"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.7.1.3"><p id="p4312753511422"><a name="p4312753511422"></a><a name="p4312753511422"></a>说明</p>
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
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p2341763311422"><a name="p2341763311422"></a><a name="p2341763311422"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.3 "><p id="p1778010111422"><a name="p1778010111422"></a><a name="p1778010111422"></a>输入路径的起点ID。</p>
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
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p6118162711422"><a name="p6118162711422"></a><a name="p6118162711422"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.3 "><p id="p5676473911422"><a name="p5676473911422"></a><a name="p5676473911422"></a>输入路径的终点ID。</p>
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
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p94607411422"><a name="p94607411422"></a><a name="p94607411422"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.3 "><p id="p1859947811422"><a name="p1859947811422"></a><a name="p1859947811422"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.4 "><p id="p187631257121913"><a name="p187631257121913"></a><a name="p187631257121913"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.7.1.5 "><p id="p302914011422"><a name="p302914011422"></a><a name="p302914011422"></a>true或false。</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.7.1.6 "><p id="p6075974311422"><a name="p6075974311422"></a><a name="p6075974311422"></a>false</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table32881853474"></a>
<table><thead align="left"><tr id="row9288115114718"><th class="cellrowborder" valign="top" width="15.870000000000001%" id="mcps1.2.4.1.1"><p id="p5302353479"><a name="p5302353479"></a><a name="p5302353479"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.23%" id="mcps1.2.4.1.2"><p id="p18302175194717"><a name="p18302175194717"></a><a name="p18302175194717"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="63.9%" id="mcps1.2.4.1.3"><p id="p6302655476"><a name="p6302655476"></a><a name="p6302655476"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row9553165153818"><td class="cellrowborder" valign="top" width="15.870000000000001%" headers="mcps1.2.4.1.1 "><p id="p75531651163817"><a name="p75531651163817"></a><a name="p75531651163817"></a>paths</p>
</td>
<td class="cellrowborder" valign="top" width="20.23%" headers="mcps1.2.4.1.2 "><p id="p1553175173812"><a name="p1553175173812"></a><a name="p1553175173812"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="63.9%" headers="mcps1.2.4.1.3 "><p id="p1155320514381"><a name="p1155320514381"></a><a name="p1155320514381"></a>source节点和target节点之间所有的最短路径，格式：</p>
<p id="p18167182012413"><a name="p18167182012413"></a><a name="p18167182012413"></a>[[path1],[path2]]</p>
<p id="p13522949115819"><a name="p13522949115819"></a><a name="p13522949115819"></a>其中，</p>
<p id="p9216437572"><a name="p9216437572"></a><a name="p9216437572"></a>路径（path）的格式可参考：<a href="最短路径（Shortest-Path）.md">最短路径（Shortest Path）</a></p>
</td>
</tr>
<tr id="row1691810920714"><td class="cellrowborder" valign="top" width="15.870000000000001%" headers="mcps1.2.4.1.1 "><p id="p0918209275"><a name="p0918209275"></a><a name="p0918209275"></a>paths_number</p>
</td>
<td class="cellrowborder" valign="top" width="20.23%" headers="mcps1.2.4.1.2 "><p id="p79181991976"><a name="p79181991976"></a><a name="p79181991976"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="63.9%" headers="mcps1.2.4.1.3 "><p id="p891815916712"><a name="p891815916712"></a><a name="p891815916712"></a>路径个数</p>
</td>
</tr>
<tr id="row630213511479"><td class="cellrowborder" valign="top" width="15.870000000000001%" headers="mcps1.2.4.1.1 "><p id="p12302165104716"><a name="p12302165104716"></a><a name="p12302165104716"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="20.23%" headers="mcps1.2.4.1.2 "><p id="p33021755478"><a name="p33021755478"></a><a name="p33021755478"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63.9%" headers="mcps1.2.4.1.3 "><p id="p11300102620372"><a name="p11300102620372"></a><a name="p11300102620372"></a>起点ID</p>
</td>
</tr>
<tr id="row63021956479"><td class="cellrowborder" valign="top" width="15.870000000000001%" headers="mcps1.2.4.1.1 "><p id="p1330215534715"><a name="p1330215534715"></a><a name="p1330215534715"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="20.23%" headers="mcps1.2.4.1.2 "><p id="p133029519472"><a name="p133029519472"></a><a name="p133029519472"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63.9%" headers="mcps1.2.4.1.3 "><p id="p1930215510478"><a name="p1930215510478"></a><a name="p1930215510478"></a>终点ID</p>
</td>
</tr>
</tbody>
</table>

