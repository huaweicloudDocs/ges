# 点集共同邻居（Common Neighbors of Vertex Sets）（2.2.13）<a name="ges_03_0207"></a>

**表 1**  Common Neighbors of Vertex Sets参数说明

<a name="table87375572113"></a>
<table><thead align="left"><tr id="row573718577112"><th class="cellrowborder" valign="top" width="16.666666666666664%" id="mcps1.2.7.1.1"><p id="p43910435419"><a name="p43910435419"></a><a name="p43910435419"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.357928414317136%" id="mcps1.2.7.1.2"><p id="p14398430419"><a name="p14398430419"></a><a name="p14398430419"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.777044591081784%" id="mcps1.2.7.1.3"><p id="p539114319411"><a name="p539114319411"></a><a name="p539114319411"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="11.057788442311537%" id="mcps1.2.7.1.4"><p id="p12391439418"><a name="p12391439418"></a><a name="p12391439418"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="31.773645270945817%" id="mcps1.2.7.1.5"><p id="p1639043141"><a name="p1639043141"></a><a name="p1639043141"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="15.366926614677064%" id="mcps1.2.7.1.6"><p id="p17391043548"><a name="p17391043548"></a><a name="p17391043548"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row473875714118"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p6391343340"><a name="p6391343340"></a><a name="p6391343340"></a>sources（2.2.6）</p>
</td>
<td class="cellrowborder" valign="top" width="10.357928414317136%" headers="mcps1.2.7.1.2 "><p id="p153917435410"><a name="p153917435410"></a><a name="p153917435410"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.777044591081784%" headers="mcps1.2.7.1.3 "><p id="p739144310416"><a name="p739144310416"></a><a name="p739144310416"></a>起点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="11.057788442311537%" headers="mcps1.2.7.1.4 "><p id="p4401435418"><a name="p4401435418"></a><a name="p4401435418"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="31.773645270945817%" headers="mcps1.2.7.1.5 "><p id="p14401643943"><a name="p14401643943"></a><a name="p14401643943"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p13401643049"><a name="p13401643049"></a><a name="p13401643049"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="15.366926614677064%" headers="mcps1.2.7.1.6 "><p id="p34012431944"><a name="p34012431944"></a><a name="p34012431944"></a>-</p>
</td>
</tr>
<tr id="row57387579118"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p140843844"><a name="p140843844"></a><a name="p140843844"></a>targets（2.2.6）</p>
</td>
<td class="cellrowborder" valign="top" width="10.357928414317136%" headers="mcps1.2.7.1.2 "><p id="p13404432419"><a name="p13404432419"></a><a name="p13404432419"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.777044591081784%" headers="mcps1.2.7.1.3 "><p id="p204010430416"><a name="p204010430416"></a><a name="p204010430416"></a>终点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="11.057788442311537%" headers="mcps1.2.7.1.4 "><p id="p8401643846"><a name="p8401643846"></a><a name="p8401643846"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="31.773645270945817%" headers="mcps1.2.7.1.5 "><p id="p34010431540"><a name="p34010431540"></a><a name="p34010431540"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Mike,Amy”。</p>
<p id="p16403439419"><a name="p16403439419"></a><a name="p16403439419"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="15.366926614677064%" headers="mcps1.2.7.1.6 "><p id="p24014431743"><a name="p24014431743"></a><a name="p24014431743"></a>-</p>
</td>
</tr>
<tr id="row2792171111190"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p552241313194"><a name="p552241313194"></a><a name="p552241313194"></a>restricted（2.2.13）</p>
</td>
<td class="cellrowborder" valign="top" width="10.357928414317136%" headers="mcps1.2.7.1.2 "><p id="p0522101311197"><a name="p0522101311197"></a><a name="p0522101311197"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.777044591081784%" headers="mcps1.2.7.1.3 "><p id="p452231391916"><a name="p452231391916"></a><a name="p452231391916"></a>是否带其他约束</p>
</td>
<td class="cellrowborder" valign="top" width="11.057788442311537%" headers="mcps1.2.7.1.4 "><p id="p105221013181918"><a name="p105221013181918"></a><a name="p105221013181918"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="31.773645270945817%" headers="mcps1.2.7.1.5 "><p id="p1052218131199"><a name="p1052218131199"></a><a name="p1052218131199"></a>true或false。</p>
<a name="ul1552216132194"></a><a name="ul1552216132194"></a><ul id="ul1552216132194"><li>false：不带额外约束，即找到的共同邻居为起点集和终点集对应邻域的交集。</li><li>true，带额外约束，这里指找到的共同邻居不仅是起点集和终点集邻域的交集，同时共同邻居集合中的每个点都至少有2个以上邻居节点在起点集和终点集中。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.366926614677064%" headers="mcps1.2.7.1.6 "><p id="p55238131192"><a name="p55238131192"></a><a name="p55238131192"></a>true</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table1197558191314"></a>
<table><thead align="left"><tr id="row29761841313"><th class="cellrowborder" valign="top" width="22.472247224722473%" id="mcps1.2.4.1.1"><p id="p68309106137"><a name="p68309106137"></a><a name="p68309106137"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.152515251525152%" id="mcps1.2.4.1.2"><p id="p138301810171318"><a name="p138301810171318"></a><a name="p138301810171318"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.37523752375238%" id="mcps1.2.4.1.3"><p id="p10830121081315"><a name="p10830121081315"></a><a name="p10830121081315"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row119768810132"><td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.4.1.1 "><p id="p6830410141317"><a name="p6830410141317"></a><a name="p6830410141317"></a>vertices</p>
</td>
<td class="cellrowborder" valign="top" width="25.152515251525152%" headers="mcps1.2.4.1.2 "><p id="p15831710101312"><a name="p15831710101312"></a><a name="p15831710101312"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="52.37523752375238%" headers="mcps1.2.4.1.3 "><p id="p1583121015131"><a name="p1583121015131"></a><a name="p1583121015131"></a>公共邻居节点，格式：</p>
<p id="p15831710111310"><a name="p15831710111310"></a><a name="p15831710111310"></a>[vertexId,...],</p>
<p id="p883113109135"><a name="p883113109135"></a><a name="p883113109135"></a>其中,</p>
<p id="p1831111016131"><a name="p1831111016131"></a><a name="p1831111016131"></a>vertexId：string类型</p>
</td>
</tr>
<tr id="row179766810130"><td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.4.1.1 "><p id="p88315100131"><a name="p88315100131"></a><a name="p88315100131"></a>common_neighbors</p>
</td>
<td class="cellrowborder" valign="top" width="25.152515251525152%" headers="mcps1.2.4.1.2 "><p id="p1183181091314"><a name="p1183181091314"></a><a name="p1183181091314"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="52.37523752375238%" headers="mcps1.2.4.1.3 "><p id="p12831171019139"><a name="p12831171019139"></a><a name="p12831171019139"></a>公共邻居节点个数。</p>
</td>
</tr>
</tbody>
</table>

