# PageRank算法\(1.0.0\)<a name="ges_03_0077"></a>

**表 1**  parameters参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="16%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="13%" id="mcps1.2.7.1.4"><p id="p0785183919517"><a name="p0785183919517"></a><a name="p0785183919517"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="24%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.7.1.6"><p id="p8883058175257"><a name="p8883058175257"></a><a name="p8883058175257"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.1 "><p id="p1143990987"><a name="p1143990987"></a><a name="p1143990987"></a>alpha</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.7.1.2 "><p id="p82629131588"><a name="p82629131588"></a><a name="p82629131588"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p32111736192918"><a name="p32111736192918"></a><a name="p32111736192918"></a>权重系数</p>
<p id="p11203113620296"><a name="p11203113620296"></a><a name="p11203113620296"></a>(又称阻尼系数)。</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.4 "><p id="p17854397519"><a name="p17854397519"></a><a name="p17854397519"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.7.1.5 "><p id="p1375182054520"><a name="p1375182054520"></a><a name="p1375182054520"></a>0~1，不包括0和1。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.6 "><p id="p48439126175257"><a name="p48439126175257"></a><a name="p48439126175257"></a>0.85</p>
</td>
</tr>
<tr id="row144392001589"><td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.1 "><p id="p543916014814"><a name="p543916014814"></a><a name="p543916014814"></a>convergence</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.7.1.2 "><p id="p11262161310820"><a name="p11262161310820"></a><a name="p11262161310820"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p104392003812"><a name="p104392003812"></a><a name="p104392003812"></a>收敛精度。</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.4 "><p id="p67851639451"><a name="p67851639451"></a><a name="p67851639451"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.7.1.5 "><p id="p195910142458"><a name="p195910142458"></a><a name="p195910142458"></a>0~1，不包括0和1。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.6 "><p id="p31255134175257"><a name="p31255134175257"></a><a name="p31255134175257"></a>0.00001</p>
</td>
</tr>
<tr id="row371539495"><td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.1 "><p id="p1871717918920"><a name="p1871717918920"></a><a name="p1871717918920"></a>max_iterations</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.7.1.2 "><p id="p471715910916"><a name="p471715910916"></a><a name="p471715910916"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p1671779594"><a name="p1671779594"></a><a name="p1671779594"></a>最大迭代次数。</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.4 "><p id="p17785739658"><a name="p17785739658"></a><a name="p17785739658"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.7.1.5 "><p id="p92561811184518"><a name="p92561811184518"></a><a name="p92561811184518"></a>1~2000。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.6 "><p id="p48637939175257"><a name="p48637939175257"></a><a name="p48637939175257"></a>1000</p>
</td>
</tr>
<tr id="row139901027102910"><td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.1 "><p id="p13753301698"><a name="p13753301698"></a><a name="p13753301698"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.7.1.2 "><p id="p27531901695"><a name="p27531901695"></a><a name="p27531901695"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p1775316016919"><a name="p1775316016919"></a><a name="p1775316016919"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.4 "><p id="p87855391557"><a name="p87855391557"></a><a name="p87855391557"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.7.1.5 "><p id="p13151535595"><a name="p13151535595"></a><a name="p13151535595"></a>true或false。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.6 "><p id="p47358972175257"><a name="p47358972175257"></a><a name="p47358972175257"></a>true</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table04091716174216"></a>
<table><thead align="left"><tr id="row7425316114219"><th class="cellrowborder" valign="top" width="30.19%" id="mcps1.2.4.1.1"><p id="p4425616134219"><a name="p4425616134219"></a><a name="p4425616134219"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.529999999999998%" id="mcps1.2.4.1.2"><p id="p1744131654219"><a name="p1744131654219"></a><a name="p1744131654219"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="45.28%" id="mcps1.2.4.1.3"><p id="p1044115166429"><a name="p1044115166429"></a><a name="p1044115166429"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row044181644210"><td class="cellrowborder" valign="top" width="30.19%" headers="mcps1.2.4.1.1 "><p id="p844101644210"><a name="p844101644210"></a><a name="p844101644210"></a>pagerank</p>
</td>
<td class="cellrowborder" valign="top" width="24.529999999999998%" headers="mcps1.2.4.1.2 "><p id="p04413168426"><a name="p04413168426"></a><a name="p04413168426"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="45.28%" headers="mcps1.2.4.1.3 "><p id="p1044121616425"><a name="p1044121616425"></a><a name="p1044121616425"></a>各节点的pagerank值，格式：</p>
<p id="p63161133854"><a name="p63161133854"></a><a name="p63161133854"></a>[{vertexId:rankValue},...],</p>
<p id="p83008413714"><a name="p83008413714"></a><a name="p83008413714"></a>其中,</p>
<p id="p276931513620"><a name="p276931513620"></a><a name="p276931513620"></a>vertexId：string类型</p>
<p id="p42531732962"><a name="p42531732962"></a><a name="p42531732962"></a>rankValue：double类型</p>
</td>
</tr>
</tbody>
</table>

