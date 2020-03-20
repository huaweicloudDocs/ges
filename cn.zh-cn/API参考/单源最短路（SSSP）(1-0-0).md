# 单源最短路（SSSP）\(1.0.0\)<a name="ges_03_0092"></a>

**表 1**  parameters参数说明

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
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p2140961710425"><a name="p2140961710425"></a><a name="p2140961710425"></a>节点的ID。</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p5389154132712"><a name="p5389154132712"></a><a name="p5389154132712"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p5645743610425"><a name="p5645743610425"></a><a name="p5645743610425"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p964961610425"><a name="p964961610425"></a><a name="p964961610425"></a>-</p>
</td>
</tr>
<tr id="row44303816104111"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p5524824310425"><a name="p5524824310425"></a><a name="p5524824310425"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p4592270710425"><a name="p4592270710425"></a><a name="p4592270710425"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.2.7.1.3 "><p id="p2875176710425"><a name="p2875176710425"></a><a name="p2875176710425"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.7.1.4 "><p id="p183891241162715"><a name="p183891241162715"></a><a name="p183891241162715"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.5 "><p id="p4719178410425"><a name="p4719178410425"></a><a name="p4719178410425"></a>true或false。</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p6443812510425"><a name="p6443812510425"></a><a name="p6443812510425"></a>true</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table6505145594419"></a>
<table><thead align="left"><tr id="row19505135515442"><th class="cellrowborder" valign="top" width="28.89%" id="mcps1.2.4.1.1"><p id="p7505105544413"><a name="p7505105544413"></a><a name="p7505105544413"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.47%" id="mcps1.2.4.1.2"><p id="p750535534417"><a name="p750535534417"></a><a name="p750535534417"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.64%" id="mcps1.2.4.1.3"><p id="p05051155164417"><a name="p05051155164417"></a><a name="p05051155164417"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row195051655104411"><td class="cellrowborder" valign="top" width="28.89%" headers="mcps1.2.4.1.1 "><p id="p1850545520448"><a name="p1850545520448"></a><a name="p1850545520448"></a>distance</p>
</td>
<td class="cellrowborder" valign="top" width="15.47%" headers="mcps1.2.4.1.2 "><p id="p450555515442"><a name="p450555515442"></a><a name="p450555515442"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="55.64%" headers="mcps1.2.4.1.3 "><p id="p1044121616425"><a name="p1044121616425"></a><a name="p1044121616425"></a>源节点（source）到图中各节点的路径长度：</p>
<p id="p63161133854"><a name="p63161133854"></a><a name="p63161133854"></a>[{vertexId:distanceValue},...],</p>
<p id="p83008413714"><a name="p83008413714"></a><a name="p83008413714"></a>其中,</p>
<p id="p276931513620"><a name="p276931513620"></a><a name="p276931513620"></a>vertexId：string类型</p>
<p id="p42531732962"><a name="p42531732962"></a><a name="p42531732962"></a>distanceValue：double类型</p>
</td>
</tr>
<tr id="row372825615515"><td class="cellrowborder" valign="top" width="28.89%" headers="mcps1.2.4.1.1 "><p id="p1072818562517"><a name="p1072818562517"></a><a name="p1072818562517"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="15.47%" headers="mcps1.2.4.1.2 "><p id="p27281056552"><a name="p27281056552"></a><a name="p27281056552"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.64%" headers="mcps1.2.4.1.3 "><p id="p1072819562513"><a name="p1072819562513"></a><a name="p1072819562513"></a>源节点ID</p>
</td>
</tr>
</tbody>
</table>

