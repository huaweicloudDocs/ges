# k跳算法（k-hop）<a name="ges_03_0080"></a>

**表 1**  parameters参数说明

<a name="table1182814413366"></a>
<table><thead align="left"><tr id="row108379493615"><th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.1"><p id="p10841845364"><a name="p10841845364"></a><a name="p10841845364"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.2"><p id="p1184317420365"><a name="p1184317420365"></a><a name="p1184317420365"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.7.1.3"><p id="p1884714473613"><a name="p1884714473613"></a><a name="p1884714473613"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.7.1.4"><p id="p6151173011175"><a name="p6151173011175"></a><a name="p6151173011175"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="32%" id="mcps1.2.7.1.5"><p id="p1685412415365"><a name="p1685412415365"></a><a name="p1685412415365"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.2.7.1.6"><p id="p29310607141819"><a name="p29310607141819"></a><a name="p29310607141819"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1886084193612"><td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.1 "><p id="p11861164183619"><a name="p11861164183619"></a><a name="p11861164183619"></a>k</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p11864947363"><a name="p11864947363"></a><a name="p11864947363"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p108673415366"><a name="p108673415366"></a><a name="p108673415366"></a>跳数。</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.7.1.4 "><p id="p131511230151712"><a name="p131511230151712"></a><a name="p131511230151712"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.7.1.5 "><p id="p5871114143610"><a name="p5871114143610"></a><a name="p5871114143610"></a>1~10。</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.6 "><p id="p25348953141819"><a name="p25348953141819"></a><a name="p25348953141819"></a>-</p>
</td>
</tr>
<tr id="row1787664183613"><td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.1 "><p id="p6879740367"><a name="p6879740367"></a><a name="p6879740367"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p5882184143619"><a name="p5882184143619"></a><a name="p5882184143619"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p11884144133614"><a name="p11884144133614"></a><a name="p11884144133614"></a>节点的ID。</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.7.1.4 "><p id="p17152163017175"><a name="p17152163017175"></a><a name="p17152163017175"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.7.1.5 "><p id="p143915011811"><a name="p143915011811"></a><a name="p143915011811"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.6 "><p id="p39999332141819"><a name="p39999332141819"></a><a name="p39999332141819"></a>-</p>
</td>
</tr>
<tr id="row10862634141528"><td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.1 "><p id="p7458176141528"><a name="p7458176141528"></a><a name="p7458176141528"></a>mode</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p132526141528"><a name="p132526141528"></a><a name="p132526141528"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.3 "><p id="p10734685141528"><a name="p10734685141528"></a><a name="p10734685141528"></a>方向。</p>
<a name="ul61647365181433"></a><a name="ul61647365181433"></a><ul id="ul61647365181433"><li>OUT：沿出边跳。</li><li>IN：沿入边跳。</li><li>ALL：双向跳。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.7.1.4 "><p id="p515263051719"><a name="p515263051719"></a><a name="p515263051719"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.7.1.5 "><p id="p64203189141528"><a name="p64203189141528"></a><a name="p64203189141528"></a>OUT，IN，ALL。</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.7.1.6 "><p id="p18720472141819"><a name="p18720472141819"></a><a name="p18720472141819"></a>OUT</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table16960162664510"></a>
<table><thead align="left"><tr id="row996092674516"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p169601426144519"><a name="p169601426144519"></a><a name="p169601426144519"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.54%" id="mcps1.2.4.1.2"><p id="p16960112618452"><a name="p16960112618452"></a><a name="p16960112618452"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="59.24%" id="mcps1.2.4.1.3"><p id="p1396002634514"><a name="p1396002634514"></a><a name="p1396002634514"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row10960102611455"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p149601826144520"><a name="p149601826144520"></a><a name="p149601826144520"></a>vertices</p>
</td>
<td class="cellrowborder" valign="top" width="18.54%" headers="mcps1.2.4.1.2 "><p id="p17960112619453"><a name="p17960112619453"></a><a name="p17960112619453"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="59.24%" headers="mcps1.2.4.1.3 "><p id="p39741526114512"><a name="p39741526114512"></a><a name="p39741526114512"></a></p>
<p id="p1044121616425"><a name="p1044121616425"></a><a name="p1044121616425"></a>k跳内的节点id，格式：</p>
<p id="p63161133854"><a name="p63161133854"></a><a name="p63161133854"></a>[vertexId,...],</p>
<p id="p83008413714"><a name="p83008413714"></a><a name="p83008413714"></a>其中,</p>
<p id="p276931513620"><a name="p276931513620"></a><a name="p276931513620"></a>vertexId：string类型</p>
</td>
</tr>
<tr id="row297422674519"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p169745260451"><a name="p169745260451"></a><a name="p169745260451"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="18.54%" headers="mcps1.2.4.1.2 "><p id="p1897432613451"><a name="p1897432613451"></a><a name="p1897432613451"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.24%" headers="mcps1.2.4.1.3 "><p id="p197410262458"><a name="p197410262458"></a><a name="p197410262458"></a>起点id</p>
</td>
</tr>
<tr id="row897422619455"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p9974226164516"><a name="p9974226164516"></a><a name="p9974226164516"></a>k</p>
</td>
<td class="cellrowborder" valign="top" width="18.54%" headers="mcps1.2.4.1.2 "><p id="p3974726114510"><a name="p3974726114510"></a><a name="p3974726114510"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="59.24%" headers="mcps1.2.4.1.3 "><p id="p1974172613451"><a name="p1974172613451"></a><a name="p1974172613451"></a>跳数</p>
</td>
</tr>
<tr id="row1791310197303"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p13913919133010"><a name="p13913919133010"></a><a name="p13913919133010"></a>k_hop_neighbors</p>
</td>
<td class="cellrowborder" valign="top" width="18.54%" headers="mcps1.2.4.1.2 "><p id="p791311194300"><a name="p791311194300"></a><a name="p791311194300"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="59.24%" headers="mcps1.2.4.1.3 "><p id="p79131419173016"><a name="p79131419173016"></a><a name="p79131419173016"></a>k跳内的节点个数（不包含起点）</p>
</td>
</tr>
</tbody>
</table>

