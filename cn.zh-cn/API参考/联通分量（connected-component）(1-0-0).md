# 联通分量（Connected Component）\(1.0.0\)<a name="ges_03_0093"></a>

**表 1**  response\_data参数说明

<a name="table1094413119474"></a>
<table><thead align="left"><tr id="row169447312472"><th class="cellrowborder" valign="top" width="30.016998300169984%" id="mcps1.2.4.1.1"><p id="p10944153154715"><a name="p10944153154715"></a><a name="p10944153154715"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.948005199480054%" id="mcps1.2.4.1.2"><p id="p10944531134719"><a name="p10944531134719"></a><a name="p10944531134719"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.03499650034996%" id="mcps1.2.4.1.3"><p id="p109447317478"><a name="p109447317478"></a><a name="p109447317478"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row11559174543719"><td class="cellrowborder" valign="top" width="30.016998300169984%" headers="mcps1.2.4.1.1 "><p id="p1155916459378"><a name="p1155916459378"></a><a name="p1155916459378"></a>Max_WCC_size</p>
</td>
<td class="cellrowborder" valign="top" width="19.948005199480054%" headers="mcps1.2.4.1.2 "><p id="p555944543714"><a name="p555944543714"></a><a name="p555944543714"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="50.03499650034996%" headers="mcps1.2.4.1.3 "><p id="p05591458371"><a name="p05591458371"></a><a name="p05591458371"></a>最大联通分量中节点的个数</p>
</td>
</tr>
<tr id="row16949238133718"><td class="cellrowborder" valign="top" width="30.016998300169984%" headers="mcps1.2.4.1.1 "><p id="p29491038123720"><a name="p29491038123720"></a><a name="p29491038123720"></a>Max_WCC_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.948005199480054%" headers="mcps1.2.4.1.2 "><p id="p1394963813379"><a name="p1394963813379"></a><a name="p1394963813379"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.03499650034996%" headers="mcps1.2.4.1.3 "><p id="p094933883710"><a name="p094933883710"></a><a name="p094933883710"></a>最大联通分量对应的联通集合ID</p>
</td>
</tr>
<tr id="row1694403144717"><td class="cellrowborder" valign="top" width="30.016998300169984%" headers="mcps1.2.4.1.1 "><p id="p16961163104712"><a name="p16961163104712"></a><a name="p16961163104712"></a>community</p>
</td>
<td class="cellrowborder" valign="top" width="19.948005199480054%" headers="mcps1.2.4.1.2 "><p id="p12961193119474"><a name="p12961193119474"></a><a name="p12961193119474"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="50.03499650034996%" headers="mcps1.2.4.1.3 "><p id="p101571833403"><a name="p101571833403"></a><a name="p101571833403"></a>各节点对应的联通集合(commmunity)，格式：[{vertexId:communityId},...]</p>
<p id="p92052134112"><a name="p92052134112"></a><a name="p92052134112"></a>其中,</p>
<p id="p2518181912118"><a name="p2518181912118"></a><a name="p2518181912118"></a>vertexId: string类型</p>
<p id="p1389310292112"><a name="p1389310292112"></a><a name="p1389310292112"></a>communityId: string类型</p>
</td>
</tr>
</tbody>
</table>

