# Node2vec算法<a name="ges_01_0046"></a>

## 概述<a name="section204471932366"></a>

Node2vec算法通过调用word2vec算法，把网络中的节点映射到欧式空间，用向量表示节点的特征。

Node2vec算法通过回退参数 P 和前进参数 Q 来生成从每个节点出发的随机步，带有BFS和DFS的混合，回退概率正比于1/P，前进概率正比于1/Q。每个节点出发生成多个随机步，反映出网络的结构信息。

## 适用场景<a name="section4610026394558"></a>

Node2vec算法适用于节点功能相似性比较、节点结构相似性比较、社团聚类等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  Node2vec算法参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="13.404040404040405%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.828282828282827%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="23.232323232323232%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="10.1010101010101%" id="mcps1.2.7.1.4"><p id="p530116512247"><a name="p530116512247"></a><a name="p530116512247"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="34.34343434343434%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="9.09090909090909%" id="mcps1.2.7.1.6"><p id="p3066297816429"><a name="p3066297816429"></a><a name="p3066297816429"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="13.404040404040405%" headers="mcps1.2.7.1.1 "><p id="p65023471104"><a name="p65023471104"></a><a name="p65023471104"></a>P</p>
</td>
<td class="cellrowborder" valign="top" width="9.828282828282827%" headers="mcps1.2.7.1.2 "><p id="p3502247181013"><a name="p3502247181013"></a><a name="p3502247181013"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.232323232323232%" headers="mcps1.2.7.1.3 "><p id="p13502347141017"><a name="p13502347141017"></a><a name="p13502347141017"></a>回退参数</p>
</td>
<td class="cellrowborder" valign="top" width="10.1010101010101%" headers="mcps1.2.7.1.4 "><p id="p130113512242"><a name="p130113512242"></a><a name="p130113512242"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="34.34343434343434%" headers="mcps1.2.7.1.5 "><p id="p9723165791010"><a name="p9723165791010"></a><a name="p9723165791010"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.09090909090909%" headers="mcps1.2.7.1.6 "><p id="p67330716429"><a name="p67330716429"></a><a name="p67330716429"></a>1</p>
</td>
</tr>
<tr id="row1592512201673"><td class="cellrowborder" valign="top" width="13.404040404040405%" headers="mcps1.2.7.1.1 "><p id="p15502204721014"><a name="p15502204721014"></a><a name="p15502204721014"></a>Q</p>
</td>
<td class="cellrowborder" valign="top" width="9.828282828282827%" headers="mcps1.2.7.1.2 "><p id="p1250217472102"><a name="p1250217472102"></a><a name="p1250217472102"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.232323232323232%" headers="mcps1.2.7.1.3 "><p id="p125021347111015"><a name="p125021347111015"></a><a name="p125021347111015"></a>前进参数</p>
</td>
<td class="cellrowborder" valign="top" width="10.1010101010101%" headers="mcps1.2.7.1.4 "><p id="p1301155182416"><a name="p1301155182416"></a><a name="p1301155182416"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="34.34343434343434%" headers="mcps1.2.7.1.5 "><p id="p16233193191118"><a name="p16233193191118"></a><a name="p16233193191118"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.09090909090909%" headers="mcps1.2.7.1.6 "><p id="p5453787616429"><a name="p5453787616429"></a><a name="p5453787616429"></a>1</p>
</td>
</tr>
<tr id="row1883311181175"><td class="cellrowborder" valign="top" width="13.404040404040405%" headers="mcps1.2.7.1.1 "><p id="p3504164715102"><a name="p3504164715102"></a><a name="p3504164715102"></a>dim</p>
</td>
<td class="cellrowborder" valign="top" width="9.828282828282827%" headers="mcps1.2.7.1.2 "><p id="p050414761011"><a name="p050414761011"></a><a name="p050414761011"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.232323232323232%" headers="mcps1.2.7.1.3 "><p id="p115043476104"><a name="p115043476104"></a><a name="p115043476104"></a>映射维度</p>
</td>
<td class="cellrowborder" valign="top" width="10.1010101010101%" headers="mcps1.2.7.1.4 "><p id="p173017518249"><a name="p173017518249"></a><a name="p173017518249"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="34.34343434343434%" headers="mcps1.2.7.1.5 "><p id="p2108111061114"><a name="p2108111061114"></a><a name="p2108111061114"></a>1~200，包括1和200</p>
</td>
<td class="cellrowborder" valign="top" width="9.09090909090909%" headers="mcps1.2.7.1.6 "><p id="p5549179716429"><a name="p5549179716429"></a><a name="p5549179716429"></a>50</p>
</td>
</tr>
<tr id="row20365740191015"><td class="cellrowborder" valign="top" width="13.404040404040405%" headers="mcps1.2.7.1.1 "><p id="p12505124718109"><a name="p12505124718109"></a><a name="p12505124718109"></a>walkLength</p>
</td>
<td class="cellrowborder" valign="top" width="9.828282828282827%" headers="mcps1.2.7.1.2 "><p id="p1450594711018"><a name="p1450594711018"></a><a name="p1450594711018"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.232323232323232%" headers="mcps1.2.7.1.3 "><p id="p9505174741010"><a name="p9505174741010"></a><a name="p9505174741010"></a>随机步长</p>
</td>
<td class="cellrowborder" valign="top" width="10.1010101010101%" headers="mcps1.2.7.1.4 "><p id="p1030110542416"><a name="p1030110542416"></a><a name="p1030110542416"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="34.34343434343434%" headers="mcps1.2.7.1.5 "><p id="p7542721141120"><a name="p7542721141120"></a><a name="p7542721141120"></a>建议取1~100，包括1和100</p>
</td>
<td class="cellrowborder" valign="top" width="9.09090909090909%" headers="mcps1.2.7.1.6 "><p id="p6565056716429"><a name="p6565056716429"></a><a name="p6565056716429"></a>40</p>
</td>
</tr>
<tr id="row136122160711"><td class="cellrowborder" valign="top" width="13.404040404040405%" headers="mcps1.2.7.1.1 "><p id="p14505144791016"><a name="p14505144791016"></a><a name="p14505144791016"></a>walkNumber</p>
</td>
<td class="cellrowborder" valign="top" width="9.828282828282827%" headers="mcps1.2.7.1.2 "><p id="p105055472101"><a name="p105055472101"></a><a name="p105055472101"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.232323232323232%" headers="mcps1.2.7.1.3 "><p id="p2505154761018"><a name="p2505154761018"></a><a name="p2505154761018"></a>每个节点的随机步长数</p>
</td>
<td class="cellrowborder" valign="top" width="10.1010101010101%" headers="mcps1.2.7.1.4 "><p id="p630116532418"><a name="p630116532418"></a><a name="p630116532418"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="34.34343434343434%" headers="mcps1.2.7.1.5 "><p id="p1234727111110"><a name="p1234727111110"></a><a name="p1234727111110"></a>建议取1~100，包括1和100</p>
</td>
<td class="cellrowborder" valign="top" width="9.09090909090909%" headers="mcps1.2.7.1.6 "><p id="p1609569716429"><a name="p1609569716429"></a><a name="p1609569716429"></a>10</p>
</td>
</tr>
<tr id="row147071213274"><td class="cellrowborder" valign="top" width="13.404040404040405%" headers="mcps1.2.7.1.1 "><p id="p55051747201018"><a name="p55051747201018"></a><a name="p55051747201018"></a>iterations</p>
</td>
<td class="cellrowborder" valign="top" width="9.828282828282827%" headers="mcps1.2.7.1.2 "><p id="p55056476103"><a name="p55056476103"></a><a name="p55056476103"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.232323232323232%" headers="mcps1.2.7.1.3 "><p id="p850519473102"><a name="p850519473102"></a><a name="p850519473102"></a>迭代次数</p>
</td>
<td class="cellrowborder" valign="top" width="10.1010101010101%" headers="mcps1.2.7.1.4 "><p id="p3301165132414"><a name="p3301165132414"></a><a name="p3301165132414"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="34.34343434343434%" headers="mcps1.2.7.1.5 "><p id="p1139143313118"><a name="p1139143313118"></a><a name="p1139143313118"></a>1~100，包括1和100</p>
</td>
<td class="cellrowborder" valign="top" width="9.09090909090909%" headers="mcps1.2.7.1.6 "><p id="p2868310016429"><a name="p2868310016429"></a><a name="p2868310016429"></a>10</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

无。

## 示例<a name="section9539286457"></a>

输入参数 P=1，Q=0.3，dim=3，walkLength=20，walkNumber=10，iterations=40，得到每个节点的三维向量表示。

