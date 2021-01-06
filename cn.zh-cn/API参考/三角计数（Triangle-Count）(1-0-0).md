# 三角计数（Triangle Count）\(1.0.0\)<a name="ges_03_0095"></a>

**表 1**  triangle count参数说明

<a name="table111144815198"></a>
<table><thead align="left"><tr id="row19456482196"><th class="cellrowborder" valign="top" width="13.87138713871387%" id="mcps1.2.6.1.1"><p id="p1645348181915"><a name="p1645348181915"></a><a name="p1645348181915"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12.04120412041204%" id="mcps1.2.6.1.2"><p id="p8451948181914"><a name="p8451948181914"></a><a name="p8451948181914"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="34.49344934493449%" id="mcps1.2.6.1.3"><p id="p1145154851915"><a name="p1145154851915"></a><a name="p1145154851915"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="12.04120412041204%" id="mcps1.2.6.1.4"><p id="p64564810191"><a name="p64564810191"></a><a name="p64564810191"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="27.552755275527556%" id="mcps1.2.6.1.5"><p id="p54564851917"><a name="p54564851917"></a><a name="p54564851917"></a>取值范围</p>
</th>
</tr>
</thead>
<tbody><tr id="row1845248201910"><td class="cellrowborder" valign="top" width="13.87138713871387%" headers="mcps1.2.6.1.1 "><p id="p1345194801912"><a name="p1345194801912"></a><a name="p1345194801912"></a>statistics</p>
</td>
<td class="cellrowborder" valign="top" width="12.04120412041204%" headers="mcps1.2.6.1.2 "><p id="p11457486199"><a name="p11457486199"></a><a name="p11457486199"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="34.49344934493449%" headers="mcps1.2.6.1.3 "><p id="p345748111917"><a name="p345748111917"></a><a name="p345748111917"></a>是否仅输出总的统计量结果：</p>
<a name="ul1383201512204"></a><a name="ul1383201512204"></a><ul id="ul1383201512204"><li>true：仅输出总的统计数量。</li><li>false：输出各点对应三角形数量。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.04120412041204%" headers="mcps1.2.6.1.4 "><p id="p04514483198"><a name="p04514483198"></a><a name="p04514483198"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="27.552755275527556%" headers="mcps1.2.6.1.5 "><p id="p045184816199"><a name="p045184816199"></a><a name="p045184816199"></a>true或false，默认为true。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table1094413119474"></a>
<table><thead align="left"><tr id="row169447312472"><th class="cellrowborder" valign="top" width="20.69%" id="mcps1.2.4.1.1"><p id="p10944153154715"><a name="p10944153154715"></a><a name="p10944153154715"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.79%" id="mcps1.2.4.1.2"><p id="p10944531134719"><a name="p10944531134719"></a><a name="p10944531134719"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.52%" id="mcps1.2.4.1.3"><p id="p109447317478"><a name="p109447317478"></a><a name="p109447317478"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row11559174543719"><td class="cellrowborder" valign="top" width="20.69%" headers="mcps1.2.4.1.1 "><p id="p1155916459378"><a name="p1155916459378"></a><a name="p1155916459378"></a>triangle_count</p>
</td>
<td class="cellrowborder" valign="top" width="23.79%" headers="mcps1.2.4.1.2 "><p id="p555944543714"><a name="p555944543714"></a><a name="p555944543714"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.52%" headers="mcps1.2.4.1.3 "><p id="p05591458371"><a name="p05591458371"></a><a name="p05591458371"></a>三角形个数</p>
</td>
</tr>
<tr id="row2051122720229"><td class="cellrowborder" valign="top" width="20.69%" headers="mcps1.2.4.1.1 "><p id="p034212166375"><a name="p034212166375"></a><a name="p034212166375"></a>vertex_triangles</p>
</td>
<td class="cellrowborder" valign="top" width="23.79%" headers="mcps1.2.4.1.2 "><p id="p63428161375"><a name="p63428161375"></a><a name="p63428161375"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="55.52%" headers="mcps1.2.4.1.3 "><p id="p193421716103717"><a name="p193421716103717"></a><a name="p193421716103717"></a>各节点的三角形个数，格式：</p>
<p id="p2034214164372"><a name="p2034214164372"></a><a name="p2034214164372"></a>[{vertexId : vertexTriangleCount},...],</p>
<p id="p1034271615372"><a name="p1034271615372"></a><a name="p1034271615372"></a>其中,</p>
<p id="p834251603719"><a name="p834251603719"></a><a name="p834251603719"></a>vertexId：string类型</p>
<p id="p133421816113710"><a name="p133421816113710"></a><a name="p133421816113710"></a>vertexTriangleCount：integer类型</p>
</td>
</tr>
</tbody>
</table>

