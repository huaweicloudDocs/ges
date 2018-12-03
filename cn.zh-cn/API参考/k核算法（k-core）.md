# k核算法（k-core）<a name="ges_03_0079"></a>

**表 1**  parameters参数说明

<a name="table1195419507343"></a>
<table><thead align="left"><tr id="row99631850173412"><th class="cellrowborder" valign="top" width="13%" id="mcps1.2.7.1.1"><p id="p109641750203412"><a name="p109641750203412"></a><a name="p109641750203412"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.2"><p id="p8969115063412"><a name="p8969115063412"></a><a name="p8969115063412"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.7.1.3"><p id="p13970150143414"><a name="p13970150143414"></a><a name="p13970150143414"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="7.000000000000001%" id="mcps1.2.7.1.4"><p id="p1193205172815"><a name="p1193205172815"></a><a name="p1193205172815"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.7.1.5"><p id="p797265013410"><a name="p797265013410"></a><a name="p797265013410"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.7.1.6"><p id="p345617411412"><a name="p345617411412"></a><a name="p345617411412"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row11975155043410"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.1 "><p id="p897614501340"><a name="p897614501340"></a><a name="p897614501340"></a>k</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p1598065011341"><a name="p1598065011341"></a><a name="p1598065011341"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.3 "><p id="p3982950203412"><a name="p3982950203412"></a><a name="p3982950203412"></a>核数。</p>
<p id="p20671725172810"><a name="p20671725172810"></a><a name="p20671725172810"></a>算法会返回核数大于等于k的节点。</p>
</td>
<td class="cellrowborder" valign="top" width="7.000000000000001%" headers="mcps1.2.7.1.4 "><p id="p12932517284"><a name="p12932517284"></a><a name="p12932517284"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.5 "><p id="p5439601785"><a name="p5439601785"></a><a name="p5439601785"></a>大于等于0。</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p94561842042"><a name="p94561842042"></a><a name="p94561842042"></a>-</p>
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
<tbody><tr id="row195051655104411"><td class="cellrowborder" valign="top" width="28.89%" headers="mcps1.2.4.1.1 "><p id="p1850545520448"><a name="p1850545520448"></a><a name="p1850545520448"></a>coreness</p>
</td>
<td class="cellrowborder" valign="top" width="15.47%" headers="mcps1.2.4.1.2 "><p id="p450555515442"><a name="p450555515442"></a><a name="p450555515442"></a>List&lt;Map&lt;String,Integer&gt;&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="55.64%" headers="mcps1.2.4.1.3 "><p id="p1044121616425"><a name="p1044121616425"></a><a name="p1044121616425"></a>各节点的coreness值（coreness&gt;=k），格式：</p>
<p id="p63161133854"><a name="p63161133854"></a><a name="p63161133854"></a>[{vertexId:corenessValue},...],</p>
<p id="p83008413714"><a name="p83008413714"></a><a name="p83008413714"></a>其中,</p>
<p id="p276931513620"><a name="p276931513620"></a><a name="p276931513620"></a>vertexId：string类型</p>
<p id="p42531732962"><a name="p42531732962"></a><a name="p42531732962"></a>corenessValue：int类型</p>
</td>
</tr>
</tbody>
</table>

