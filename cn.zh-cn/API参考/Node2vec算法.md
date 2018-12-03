# Node2vec算法<a name="ges_03_0089"></a>

**表 1**  parameters参数说明

<a name="table1155012388394"></a>
<table><thead align="left"><tr id="row5568338103918"><th class="cellrowborder" valign="top" width="12.000000000000002%" id="mcps1.2.7.1.1"><p id="p95731438163919"><a name="p95731438163919"></a><a name="p95731438163919"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.000000000000002%" id="mcps1.2.7.1.2"><p id="p1757613382393"><a name="p1757613382393"></a><a name="p1757613382393"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="23.000000000000004%" id="mcps1.2.7.1.3"><p id="p3579183873914"><a name="p3579183873914"></a><a name="p3579183873914"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="10.000000000000002%" id="mcps1.2.7.1.4"><p id="p530116512247"><a name="p530116512247"></a><a name="p530116512247"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="29.000000000000004%" id="mcps1.2.7.1.5"><p id="p358973833917"><a name="p358973833917"></a><a name="p358973833917"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="15.000000000000002%" id="mcps1.2.7.1.6"><p id="p3066297816429"><a name="p3066297816429"></a><a name="p3066297816429"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1598113817399"><td class="cellrowborder" valign="top" width="12.000000000000002%" headers="mcps1.2.7.1.1 "><p id="p65023471104"><a name="p65023471104"></a><a name="p65023471104"></a>P</p>
</td>
<td class="cellrowborder" valign="top" width="11.000000000000002%" headers="mcps1.2.7.1.2 "><p id="p3502247181013"><a name="p3502247181013"></a><a name="p3502247181013"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.2.7.1.3 "><p id="p13502347141017"><a name="p13502347141017"></a><a name="p13502347141017"></a>回退参数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.000000000000002%" headers="mcps1.2.7.1.4 "><p id="p130113512242"><a name="p130113512242"></a><a name="p130113512242"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="29.000000000000004%" headers="mcps1.2.7.1.5 "><p id="p9723165791010"><a name="p9723165791010"></a><a name="p9723165791010"></a>大于0</p>
</td>
<td class="cellrowborder" valign="top" width="15.000000000000002%" headers="mcps1.2.7.1.6 "><p id="p67330716429"><a name="p67330716429"></a><a name="p67330716429"></a>1</p>
</td>
</tr>
<tr id="row1262720384395"><td class="cellrowborder" valign="top" width="12.000000000000002%" headers="mcps1.2.7.1.1 "><p id="p15502204721014"><a name="p15502204721014"></a><a name="p15502204721014"></a>Q</p>
</td>
<td class="cellrowborder" valign="top" width="11.000000000000002%" headers="mcps1.2.7.1.2 "><p id="p1250217472102"><a name="p1250217472102"></a><a name="p1250217472102"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.2.7.1.3 "><p id="p125021347111015"><a name="p125021347111015"></a><a name="p125021347111015"></a>前进参数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.000000000000002%" headers="mcps1.2.7.1.4 "><p id="p1301155182416"><a name="p1301155182416"></a><a name="p1301155182416"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="29.000000000000004%" headers="mcps1.2.7.1.5 "><p id="p16233193191118"><a name="p16233193191118"></a><a name="p16233193191118"></a>大于0</p>
</td>
<td class="cellrowborder" valign="top" width="15.000000000000002%" headers="mcps1.2.7.1.6 "><p id="p5453787616429"><a name="p5453787616429"></a><a name="p5453787616429"></a>1</p>
</td>
</tr>
<tr id="row1165813813395"><td class="cellrowborder" valign="top" width="12.000000000000002%" headers="mcps1.2.7.1.1 "><p id="p3504164715102"><a name="p3504164715102"></a><a name="p3504164715102"></a>dim</p>
</td>
<td class="cellrowborder" valign="top" width="11.000000000000002%" headers="mcps1.2.7.1.2 "><p id="p050414761011"><a name="p050414761011"></a><a name="p050414761011"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.2.7.1.3 "><p id="p115043476104"><a name="p115043476104"></a><a name="p115043476104"></a>映射维度。</p>
</td>
<td class="cellrowborder" valign="top" width="10.000000000000002%" headers="mcps1.2.7.1.4 "><p id="p173017518249"><a name="p173017518249"></a><a name="p173017518249"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="29.000000000000004%" headers="mcps1.2.7.1.5 "><p id="p2108111061114"><a name="p2108111061114"></a><a name="p2108111061114"></a>1~200，包括1和200。</p>
</td>
<td class="cellrowborder" valign="top" width="15.000000000000002%" headers="mcps1.2.7.1.6 "><p id="p5549179716429"><a name="p5549179716429"></a><a name="p5549179716429"></a>50</p>
</td>
</tr>
<tr id="row20365740191015"><td class="cellrowborder" valign="top" width="12.000000000000002%" headers="mcps1.2.7.1.1 "><p id="p12505124718109"><a name="p12505124718109"></a><a name="p12505124718109"></a>walkLength</p>
</td>
<td class="cellrowborder" valign="top" width="11.000000000000002%" headers="mcps1.2.7.1.2 "><p id="p1450594711018"><a name="p1450594711018"></a><a name="p1450594711018"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.2.7.1.3 "><p id="p9505174741010"><a name="p9505174741010"></a><a name="p9505174741010"></a>随机步长。</p>
</td>
<td class="cellrowborder" valign="top" width="10.000000000000002%" headers="mcps1.2.7.1.4 "><p id="p1030110542416"><a name="p1030110542416"></a><a name="p1030110542416"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="29.000000000000004%" headers="mcps1.2.7.1.5 "><p id="p7542721141120"><a name="p7542721141120"></a><a name="p7542721141120"></a>建议取1~100，包括1和100。</p>
</td>
<td class="cellrowborder" valign="top" width="15.000000000000002%" headers="mcps1.2.7.1.6 "><p id="p6565056716429"><a name="p6565056716429"></a><a name="p6565056716429"></a>40</p>
</td>
</tr>
<tr id="row07271438103918"><td class="cellrowborder" valign="top" width="12.000000000000002%" headers="mcps1.2.7.1.1 "><p id="p14505144791016"><a name="p14505144791016"></a><a name="p14505144791016"></a>walkNumber</p>
</td>
<td class="cellrowborder" valign="top" width="11.000000000000002%" headers="mcps1.2.7.1.2 "><p id="p105055472101"><a name="p105055472101"></a><a name="p105055472101"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.2.7.1.3 "><p id="p2505154761018"><a name="p2505154761018"></a><a name="p2505154761018"></a>每个节点的随机步长数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.000000000000002%" headers="mcps1.2.7.1.4 "><p id="p630116532418"><a name="p630116532418"></a><a name="p630116532418"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="29.000000000000004%" headers="mcps1.2.7.1.5 "><p id="p1234727111110"><a name="p1234727111110"></a><a name="p1234727111110"></a>建议取1~100，包括1和100。</p>
</td>
<td class="cellrowborder" valign="top" width="15.000000000000002%" headers="mcps1.2.7.1.6 "><p id="p1609569716429"><a name="p1609569716429"></a><a name="p1609569716429"></a>10</p>
</td>
</tr>
<tr id="row19760638173911"><td class="cellrowborder" valign="top" width="12.000000000000002%" headers="mcps1.2.7.1.1 "><p id="p55051747201018"><a name="p55051747201018"></a><a name="p55051747201018"></a>iterations</p>
</td>
<td class="cellrowborder" valign="top" width="11.000000000000002%" headers="mcps1.2.7.1.2 "><p id="p55056476103"><a name="p55056476103"></a><a name="p55056476103"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.2.7.1.3 "><p id="p850519473102"><a name="p850519473102"></a><a name="p850519473102"></a>迭代次数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.000000000000002%" headers="mcps1.2.7.1.4 "><p id="p3301165132414"><a name="p3301165132414"></a><a name="p3301165132414"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="29.000000000000004%" headers="mcps1.2.7.1.5 "><p id="p1139143313118"><a name="p1139143313118"></a><a name="p1139143313118"></a>1~100，包括1和100。</p>
</td>
<td class="cellrowborder" valign="top" width="15.000000000000002%" headers="mcps1.2.7.1.6 "><p id="p2868310016429"><a name="p2868310016429"></a><a name="p2868310016429"></a>10</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table12633111911489"></a>
<table><thead align="left"><tr id="row126331719124814"><th class="cellrowborder" valign="top" width="23.599999999999998%" id="mcps1.2.4.1.1"><p id="p66330194480"><a name="p66330194480"></a><a name="p66330194480"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.54%" id="mcps1.2.4.1.2"><p id="p363351934813"><a name="p363351934813"></a><a name="p363351934813"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.86%" id="mcps1.2.4.1.3"><p id="p17633161964810"><a name="p17633161964810"></a><a name="p17633161964810"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row17633191914480"><td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.1 "><p id="p116331719194817"><a name="p116331719194817"></a><a name="p116331719194817"></a>embedding</p>
</td>
<td class="cellrowborder" valign="top" width="19.54%" headers="mcps1.2.4.1.2 "><p id="p1263317195489"><a name="p1263317195489"></a><a name="p1263317195489"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="56.86%" headers="mcps1.2.4.1.3 "><p id="p263391974811"><a name="p263391974811"></a><a name="p263391974811"></a>各点映射到欧式空间的向量表示，格式：</p>
<p id="p4924111519816"><a name="p4924111519816"></a><a name="p4924111519816"></a>[{vertexId:vectorValue}]</p>
<p id="p1685274318113"><a name="p1685274318113"></a><a name="p1685274318113"></a>其中，</p>
<p id="p18446164720115"><a name="p18446164720115"></a><a name="p18446164720115"></a>vertexId: string类型</p>
<p id="p12981186191319"><a name="p12981186191319"></a><a name="p12981186191319"></a>vectorValue：欧式向量，例如[-0.485,-0.679,0.356]</p>
</td>
</tr>
</tbody>
</table>

