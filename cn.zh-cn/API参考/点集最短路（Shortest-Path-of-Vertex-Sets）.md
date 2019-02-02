# 点集最短路（Shortest Path of Vertex Sets）<a name="ges_03_0105"></a>

**表 1**  Parameter参数说明

<a name="table18500810104111"></a>
<table><thead align="left"><tr id="row18009483104111"><th class="cellrowborder" valign="top" width="7.772277227722772%" id="mcps1.2.7.1.1"><p id="p6644426810425"><a name="p6644426810425"></a><a name="p6644426810425"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="7.772277227722772%" id="mcps1.2.7.1.2"><p id="p1327662710425"><a name="p1327662710425"></a><a name="p1327662710425"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="13.207920792079205%" id="mcps1.2.7.1.3"><p id="p166499410425"><a name="p166499410425"></a><a name="p166499410425"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="8.118811881188119%" id="mcps1.2.7.1.4"><p id="p10389144111270"><a name="p10389144111270"></a><a name="p10389144111270"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="53.14851485148515%" id="mcps1.2.7.1.5"><p id="p64685010425"><a name="p64685010425"></a><a name="p64685010425"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="9.98019801980198%" id="mcps1.2.7.1.6"><p id="p5239490710425"><a name="p5239490710425"></a><a name="p5239490710425"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row66427667104111"><td class="cellrowborder" valign="top" width="7.772277227722772%" headers="mcps1.2.7.1.1 "><p id="p3138414910425"><a name="p3138414910425"></a><a name="p3138414910425"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="7.772277227722772%" headers="mcps1.2.7.1.2 "><p id="p5908813510425"><a name="p5908813510425"></a><a name="p5908813510425"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="13.207920792079205%" headers="mcps1.2.7.1.3 "><p id="p2140961710425"><a name="p2140961710425"></a><a name="p2140961710425"></a>起点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="8.118811881188119%" headers="mcps1.2.7.1.4 "><p id="p2445131643916"><a name="p2445131643916"></a><a name="p2445131643916"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="53.14851485148515%" headers="mcps1.2.7.1.5 "><p id="p14473161318277"><a name="p14473161318277"></a><a name="p14473161318277"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p847331310275"><a name="p847331310275"></a><a name="p847331310275"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="9.98019801980198%" headers="mcps1.2.7.1.6 "><p id="p964961610425"><a name="p964961610425"></a><a name="p964961610425"></a>-</p>
</td>
</tr>
<tr id="row1354819122815"><td class="cellrowborder" valign="top" width="7.772277227722772%" headers="mcps1.2.7.1.1 "><p id="p7843173202816"><a name="p7843173202816"></a><a name="p7843173202816"></a>targets</p>
</td>
<td class="cellrowborder" valign="top" width="7.772277227722772%" headers="mcps1.2.7.1.2 "><p id="p2843232152811"><a name="p2843232152811"></a><a name="p2843232152811"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="13.207920792079205%" headers="mcps1.2.7.1.3 "><p id="p20843332112810"><a name="p20843332112810"></a><a name="p20843332112810"></a>终点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="8.118811881188119%" headers="mcps1.2.7.1.4 "><p id="p16843123242820"><a name="p16843123242820"></a><a name="p16843123242820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="53.14851485148515%" headers="mcps1.2.7.1.5 "><p id="p447461312712"><a name="p447461312712"></a><a name="p447461312712"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p947441318273"><a name="p947441318273"></a><a name="p947441318273"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="9.98019801980198%" headers="mcps1.2.7.1.6 "><p id="p4354019192816"><a name="p4354019192816"></a><a name="p4354019192816"></a>-</p>
</td>
</tr>
<tr id="row44303816104111"><td class="cellrowborder" valign="top" width="7.772277227722772%" headers="mcps1.2.7.1.1 "><p id="p5524824310425"><a name="p5524824310425"></a><a name="p5524824310425"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="7.772277227722772%" headers="mcps1.2.7.1.2 "><p id="p4592270710425"><a name="p4592270710425"></a><a name="p4592270710425"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.207920792079205%" headers="mcps1.2.7.1.3 "><p id="p2875176710425"><a name="p2875176710425"></a><a name="p2875176710425"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="8.118811881188119%" headers="mcps1.2.7.1.4 "><p id="p25096169392"><a name="p25096169392"></a><a name="p25096169392"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="53.14851485148515%" headers="mcps1.2.7.1.5 "><p id="p4719178410425"><a name="p4719178410425"></a><a name="p4719178410425"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="9.98019801980198%" headers="mcps1.2.7.1.6 "><p id="p6443812510425"><a name="p6443812510425"></a><a name="p6443812510425"></a>false</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table32881853474"></a>
<table><thead align="left"><tr id="row9288115114718"><th class="cellrowborder" valign="top" width="17.349999999999998%" id="mcps1.2.4.1.1"><p id="p5302353479"><a name="p5302353479"></a><a name="p5302353479"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.610000000000001%" id="mcps1.2.4.1.2"><p id="p18302175194717"><a name="p18302175194717"></a><a name="p18302175194717"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="68.04%" id="mcps1.2.4.1.3"><p id="p6302655476"><a name="p6302655476"></a><a name="p6302655476"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row9553165153818"><td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.4.1.1 "><p id="p75531651163817"><a name="p75531651163817"></a><a name="p75531651163817"></a>path</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.4.1.2 "><p id="p1553175173812"><a name="p1553175173812"></a><a name="p1553175173812"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="68.04%" headers="mcps1.2.4.1.3 "><p id="p11470316153614"><a name="p11470316153614"></a><a name="p11470316153614"></a>最短路径，格式：</p>
<p id="p751814202362"><a name="p751814202362"></a><a name="p751814202362"></a>[vertexId,...]</p>
<p id="p83008413714"><a name="p83008413714"></a><a name="p83008413714"></a>其中,</p>
<p id="p276931513620"><a name="p276931513620"></a><a name="p276931513620"></a>vertexId：string类型</p>
</td>
</tr>
<tr id="row630213511479"><td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.4.1.1 "><p id="p12302165104716"><a name="p12302165104716"></a><a name="p12302165104716"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.4.1.2 "><p id="p33021755478"><a name="p33021755478"></a><a name="p33021755478"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="68.04%" headers="mcps1.2.4.1.3 "><p id="p173022514717"><a name="p173022514717"></a><a name="p173022514717"></a>起点ID</p>
</td>
</tr>
<tr id="row63021956479"><td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.4.1.1 "><p id="p1330215534715"><a name="p1330215534715"></a><a name="p1330215534715"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.4.1.2 "><p id="p133029519472"><a name="p133029519472"></a><a name="p133029519472"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="68.04%" headers="mcps1.2.4.1.3 "><p id="p1930215510478"><a name="p1930215510478"></a><a name="p1930215510478"></a>终点ID</p>
</td>
</tr>
</tbody>
</table>

