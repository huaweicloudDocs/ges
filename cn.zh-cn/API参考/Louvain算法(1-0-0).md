# Louvain算法\(1.0.0\)<a name="ges_03_0087"></a>

**表 1**  parameters参数说明

<a name="table1780933573819"></a>
<table><thead align="left"><tr id="row68301135173815"><th class="cellrowborder" valign="top" width="15.841584158415841%" id="mcps1.2.7.1.1"><p id="p148352035143820"><a name="p148352035143820"></a><a name="p148352035143820"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.485148514851485%" id="mcps1.2.7.1.2"><p id="p583911351384"><a name="p583911351384"></a><a name="p583911351384"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.247524752475247%" id="mcps1.2.7.1.3"><p id="p1884453514387"><a name="p1884453514387"></a><a name="p1884453514387"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="11.99009900990099%" id="mcps1.2.7.1.4"><p id="p18722191018233"><a name="p18722191018233"></a><a name="p18722191018233"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="27.61386138613861%" id="mcps1.2.7.1.5"><p id="p8852735143813"><a name="p8852735143813"></a><a name="p8852735143813"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.7.1.6"><p id="p38652927163737"><a name="p38652927163737"></a><a name="p38652927163737"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row5858113513810"><td class="cellrowborder" valign="top" width="15.841584158415841%" headers="mcps1.2.7.1.1 "><p id="p15862123523818"><a name="p15862123523818"></a><a name="p15862123523818"></a>convergence</p>
</td>
<td class="cellrowborder" valign="top" width="10.485148514851485%" headers="mcps1.2.7.1.2 "><p id="p4863103515384"><a name="p4863103515384"></a><a name="p4863103515384"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p68677350383"><a name="p68677350383"></a><a name="p68677350383"></a>收敛精度。</p>
</td>
<td class="cellrowborder" valign="top" width="11.99009900990099%" headers="mcps1.2.7.1.4 "><p id="p17722101015239"><a name="p17722101015239"></a><a name="p17722101015239"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="27.61386138613861%" headers="mcps1.2.7.1.5 "><p id="p33609923318"><a name="p33609923318"></a><a name="p33609923318"></a>0~1，不包括0和1。</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.6 "><p id="p43879365163737"><a name="p43879365163737"></a><a name="p43879365163737"></a>0.00001</p>
</td>
</tr>
<tr id="row148801535173815"><td class="cellrowborder" valign="top" width="15.841584158415841%" headers="mcps1.2.7.1.1 "><p id="p138841235173813"><a name="p138841235173813"></a><a name="p138841235173813"></a>max_iterations</p>
</td>
<td class="cellrowborder" valign="top" width="10.485148514851485%" headers="mcps1.2.7.1.2 "><p id="p14890335153810"><a name="p14890335153810"></a><a name="p14890335153810"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p1689403515385"><a name="p1689403515385"></a><a name="p1689403515385"></a>最大迭代次数。</p>
</td>
<td class="cellrowborder" valign="top" width="11.99009900990099%" headers="mcps1.2.7.1.4 "><p id="p14722110202312"><a name="p14722110202312"></a><a name="p14722110202312"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="27.61386138613861%" headers="mcps1.2.7.1.5 "><p id="p1149201253314"><a name="p1149201253314"></a><a name="p1149201253314"></a>1~2000。</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.6 "><p id="p64567713163737"><a name="p64567713163737"></a><a name="p64567713163737"></a>100</p>
</td>
</tr>
</tbody>
</table>

**表 2**  reponse\_data参数说明

<a name="table1094413119474"></a>
<table><thead align="left"><tr id="row169447312472"><th class="cellrowborder" valign="top" width="12.030000000000001%" id="mcps1.2.4.1.1"><p id="p10944153154715"><a name="p10944153154715"></a><a name="p10944153154715"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.340000000000002%" id="mcps1.2.4.1.2"><p id="p10944531134719"><a name="p10944531134719"></a><a name="p10944531134719"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="72.63%" id="mcps1.2.4.1.3"><p id="p109447317478"><a name="p109447317478"></a><a name="p109447317478"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2451218125120"><td class="cellrowborder" valign="top" width="12.030000000000001%" headers="mcps1.2.4.1.1 "><p id="p980181375217"><a name="p980181375217"></a><a name="p980181375217"></a>modularity</p>
</td>
<td class="cellrowborder" valign="top" width="15.340000000000002%" headers="mcps1.2.4.1.2 "><p id="p1180101315529"><a name="p1180101315529"></a><a name="p1180101315529"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="72.63%" headers="mcps1.2.4.1.3 "><p id="p18802101325218"><a name="p18802101325218"></a><a name="p18802101325218"></a>模块度。</p>
</td>
</tr>
<tr id="row9328963524"><td class="cellrowborder" valign="top" width="12.030000000000001%" headers="mcps1.2.4.1.1 "><p id="p845143115210"><a name="p845143115210"></a><a name="p845143115210"></a>community_num</p>
</td>
<td class="cellrowborder" valign="top" width="15.340000000000002%" headers="mcps1.2.4.1.2 "><p id="p245154313528"><a name="p245154313528"></a><a name="p245154313528"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="72.63%" headers="mcps1.2.4.1.3 "><p id="p1645443145211"><a name="p1645443145211"></a><a name="p1645443145211"></a>社团数量。</p>
</td>
</tr>
<tr id="row1694403144717"><td class="cellrowborder" valign="top" width="12.030000000000001%" headers="mcps1.2.4.1.1 "><p id="p16961163104712"><a name="p16961163104712"></a><a name="p16961163104712"></a>community</p>
</td>
<td class="cellrowborder" valign="top" width="15.340000000000002%" headers="mcps1.2.4.1.2 "><p id="p12961193119474"><a name="p12961193119474"></a><a name="p12961193119474"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="72.63%" headers="mcps1.2.4.1.3 "><p id="p112322719550"><a name="p112322719550"></a><a name="p112322719550"></a>各节点对应的社团(commmunity)，格式：</p>
<p id="p101571833403"><a name="p101571833403"></a><a name="p101571833403"></a>[{vertexId:communityId},...]</p>
<p id="p92052134112"><a name="p92052134112"></a><a name="p92052134112"></a>其中,</p>
<p id="p2518181912118"><a name="p2518181912118"></a><a name="p2518181912118"></a>vertexId: string类型</p>
<p id="p1389310292112"><a name="p1389310292112"></a><a name="p1389310292112"></a>communityId: string类型</p>
</td>
</tr>
</tbody>
</table>

