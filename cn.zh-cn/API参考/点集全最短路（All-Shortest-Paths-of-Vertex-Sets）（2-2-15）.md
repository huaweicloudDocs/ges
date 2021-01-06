# 点集全最短路（All Shortest Paths of Vertex Sets）（2.2.15）<a name="ges_03_0208"></a>

**表 1**  All Shortest Paths of Vertex Sets参数说明

<a name="table87375572113"></a>
<table><thead align="left"><tr id="row573718577112"><th class="cellrowborder" valign="top" width="16.666666666666664%" id="mcps1.2.7.1.1"><p id="p43910435419"><a name="p43910435419"></a><a name="p43910435419"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.357928414317136%" id="mcps1.2.7.1.2"><p id="p14398430419"><a name="p14398430419"></a><a name="p14398430419"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.64667066586683%" id="mcps1.2.7.1.3"><p id="p539114319411"><a name="p539114319411"></a><a name="p539114319411"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.658068386322736%" id="mcps1.2.7.1.4"><p id="p12391439418"><a name="p12391439418"></a><a name="p12391439418"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="31.30373925214957%" id="mcps1.2.7.1.5"><p id="p1639043141"><a name="p1639043141"></a><a name="p1639043141"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="15.366926614677064%" id="mcps1.2.7.1.6"><p id="p17391043548"><a name="p17391043548"></a><a name="p17391043548"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row473875714118"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p194711119301"><a name="p194711119301"></a><a name="p194711119301"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="10.357928414317136%" headers="mcps1.2.7.1.2 "><p id="p347171173011"><a name="p347171173011"></a><a name="p347171173011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.64667066586683%" headers="mcps1.2.7.1.3 "><p id="p16471617309"><a name="p16471617309"></a><a name="p16471617309"></a>起点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="9.658068386322736%" headers="mcps1.2.7.1.4 "><p id="p11471616302"><a name="p11471616302"></a><a name="p11471616302"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="31.30373925214957%" headers="mcps1.2.7.1.5 "><p id="p149238343159"><a name="p149238343159"></a><a name="p149238343159"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p1475111309"><a name="p1475111309"></a><a name="p1475111309"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="15.366926614677064%" headers="mcps1.2.7.1.6 "><p id="p9472163013"><a name="p9472163013"></a><a name="p9472163013"></a>-</p>
</td>
</tr>
<tr id="row57387579118"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p3478123014"><a name="p3478123014"></a><a name="p3478123014"></a>targets</p>
</td>
<td class="cellrowborder" valign="top" width="10.357928414317136%" headers="mcps1.2.7.1.2 "><p id="p18474123014"><a name="p18474123014"></a><a name="p18474123014"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.64667066586683%" headers="mcps1.2.7.1.3 "><p id="p8471018308"><a name="p8471018308"></a><a name="p8471018308"></a>终点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="9.658068386322736%" headers="mcps1.2.7.1.4 "><p id="p7472173012"><a name="p7472173012"></a><a name="p7472173012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="31.30373925214957%" headers="mcps1.2.7.1.5 "><p id="p1947111183019"><a name="p1947111183019"></a><a name="p1947111183019"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p34711113017"><a name="p34711113017"></a><a name="p34711113017"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="15.366926614677064%" headers="mcps1.2.7.1.6 "><p id="p44720113013"><a name="p44720113013"></a><a name="p44720113013"></a>-</p>
</td>
</tr>
<tr id="row2792171111190"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p2481110302"><a name="p2481110302"></a><a name="p2481110302"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="10.357928414317136%" headers="mcps1.2.7.1.2 "><p id="p144831123019"><a name="p144831123019"></a><a name="p144831123019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.64667066586683%" headers="mcps1.2.7.1.3 "><p id="p16481614309"><a name="p16481614309"></a><a name="p16481614309"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.658068386322736%" headers="mcps1.2.7.1.4 "><p id="p4489163012"><a name="p4489163012"></a><a name="p4489163012"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="31.30373925214957%" headers="mcps1.2.7.1.5 "><p id="p9485193018"><a name="p9485193018"></a><a name="p9485193018"></a>true 或false，布尔型。</p>
</td>
<td class="cellrowborder" valign="top" width="15.366926614677064%" headers="mcps1.2.7.1.6 "><p id="p1048318302"><a name="p1048318302"></a><a name="p1048318302"></a>false</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table1197558191314"></a>
<table><thead align="left"><tr id="row29761841313"><th class="cellrowborder" valign="top" width="16.301630163016302%" id="mcps1.2.4.1.1"><p id="p68309106137"><a name="p68309106137"></a><a name="p68309106137"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.061106110611062%" id="mcps1.2.4.1.2"><p id="p138301810171318"><a name="p138301810171318"></a><a name="p138301810171318"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="72.63726372637264%" id="mcps1.2.4.1.3"><p id="p10830121081315"><a name="p10830121081315"></a><a name="p10830121081315"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row119768810132"><td class="cellrowborder" valign="top" width="16.301630163016302%" headers="mcps1.2.4.1.1 "><p id="p29509211311"><a name="p29509211311"></a><a name="p29509211311"></a>paths</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.4.1.2 "><p id="p395082113113"><a name="p395082113113"></a><a name="p395082113113"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="72.63726372637264%" headers="mcps1.2.4.1.3 "><p id="p29508212313"><a name="p29508212313"></a><a name="p29508212313"></a>source节点和target节点之间所有的最短路径，格式：</p>
<p id="p179509219314"><a name="p179509219314"></a><a name="p179509219314"></a>[[path1],[path2]]</p>
<p id="p6950221103117"><a name="p6950221103117"></a><a name="p6950221103117"></a>其中，路径（path）的格式可参考：<a href="最短路径（Shortest-Path）(1-0-0).md">最短路径（Shortest Path）</a>。</p>
</td>
</tr>
<tr id="row179766810130"><td class="cellrowborder" valign="top" width="16.301630163016302%" headers="mcps1.2.4.1.1 "><p id="p13950821113111"><a name="p13950821113111"></a><a name="p13950821113111"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.4.1.2 "><p id="p1095017217311"><a name="p1095017217311"></a><a name="p1095017217311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.63726372637264%" headers="mcps1.2.4.1.3 "><p id="p595018211319"><a name="p595018211319"></a><a name="p595018211319"></a>路径的起点ID。</p>
</td>
</tr>
<tr id="row12594111418319"><td class="cellrowborder" valign="top" width="16.301630163016302%" headers="mcps1.2.4.1.1 "><p id="p149502218317"><a name="p149502218317"></a><a name="p149502218317"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.4.1.2 "><p id="p1895014212316"><a name="p1895014212316"></a><a name="p1895014212316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.63726372637264%" headers="mcps1.2.4.1.3 "><p id="p095122110311"><a name="p095122110311"></a><a name="p095122110311"></a>路径的终点ID。</p>
</td>
</tr>
</tbody>
</table>

