# 标签传播（Label Propagation）\(1.0.0\)<a name="ges_03_0086"></a>

**表 1**  parameters参数说明

<a name="table14391151773820"></a>
<table><thead align="left"><tr id="row4405317183812"><th class="cellrowborder" valign="top" width="15.151515151515152%" id="mcps1.2.7.1.1"><p id="p340818176382"><a name="p340818176382"></a><a name="p340818176382"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.090909090909092%" id="mcps1.2.7.1.2"><p id="p341212174381"><a name="p341212174381"></a><a name="p341212174381"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.161616161616163%" id="mcps1.2.7.1.3"><p id="p3417161716388"><a name="p3417161716388"></a><a name="p3417161716388"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="10.101010101010102%" id="mcps1.2.7.1.4"><p id="p3578125211"><a name="p3578125211"></a><a name="p3578125211"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="25.252525252525253%" id="mcps1.2.7.1.5"><p id="p7425131718384"><a name="p7425131718384"></a><a name="p7425131718384"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="24.242424242424242%" id="mcps1.2.7.1.6"><p id="p2984277163535"><a name="p2984277163535"></a><a name="p2984277163535"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row743311173382"><td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.7.1.1 "><p id="p6437217173813"><a name="p6437217173813"></a><a name="p6437217173813"></a>coveragence</p>
</td>
<td class="cellrowborder" valign="top" width="9.090909090909092%" headers="mcps1.2.7.1.2 "><p id="p174411017163819"><a name="p174411017163819"></a><a name="p174411017163819"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.7.1.3 "><p id="p2446317193811"><a name="p2446317193811"></a><a name="p2446317193811"></a>收敛精度。</p>
</td>
<td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.7.1.4 "><p id="p45785262119"><a name="p45785262119"></a><a name="p45785262119"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="25.252525252525253%" headers="mcps1.2.7.1.5 "><p id="p11478162763216"><a name="p11478162763216"></a><a name="p11478162763216"></a>0~1，不包括0和1。</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.7.1.6 "><p id="p40399900163535"><a name="p40399900163535"></a><a name="p40399900163535"></a>0.00001</p>
</td>
</tr>
<tr id="row20467111716385"><td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.7.1.1 "><p id="p1647181793819"><a name="p1647181793819"></a><a name="p1647181793819"></a>max_iterations</p>
</td>
<td class="cellrowborder" valign="top" width="9.090909090909092%" headers="mcps1.2.7.1.2 "><p id="p1147681753817"><a name="p1147681753817"></a><a name="p1147681753817"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.7.1.3 "><p id="p16480217163818"><a name="p16480217163818"></a><a name="p16480217163818"></a>最大迭代次数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.7.1.4 "><p id="p135781420216"><a name="p135781420216"></a><a name="p135781420216"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="25.252525252525253%" headers="mcps1.2.7.1.5 "><p id="p12150173373213"><a name="p12150173373213"></a><a name="p12150173373213"></a>1~2000。</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.7.1.6 "><p id="p51166496163535"><a name="p51166496163535"></a><a name="p51166496163535"></a>1000</p>
</td>
</tr>
</tbody>
</table>

**表 2**  reponse\_data参数说明

<a name="table1094413119474"></a>
<table><thead align="left"><tr id="row169447312472"><th class="cellrowborder" valign="top" width="16.13%" id="mcps1.2.4.1.1"><p id="p10944153154715"><a name="p10944153154715"></a><a name="p10944153154715"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.68%" id="mcps1.2.4.1.2"><p id="p10944531134719"><a name="p10944531134719"></a><a name="p10944531134719"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="72.19%" id="mcps1.2.4.1.3"><p id="p109447317478"><a name="p109447317478"></a><a name="p109447317478"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1694403144717"><td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.1 "><p id="p16961163104712"><a name="p16961163104712"></a><a name="p16961163104712"></a>community</p>
</td>
<td class="cellrowborder" valign="top" width="11.68%" headers="mcps1.2.4.1.2 "><p id="p12961193119474"><a name="p12961193119474"></a><a name="p12961193119474"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.2.4.1.3 "><p id="p2062771214554"><a name="p2062771214554"></a><a name="p2062771214554"></a>各节点对应的社团(commmunity)，格式：</p>
<p id="p101571833403"><a name="p101571833403"></a><a name="p101571833403"></a>[{vertexId:communityId},...]</p>
<p id="p92052134112"><a name="p92052134112"></a><a name="p92052134112"></a>其中,</p>
<p id="p2518181912118"><a name="p2518181912118"></a><a name="p2518181912118"></a>vertexId: string类型</p>
<p id="p1389310292112"><a name="p1389310292112"></a><a name="p1389310292112"></a>communityId: string类型</p>
</td>
</tr>
</tbody>
</table>

