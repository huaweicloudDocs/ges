# personalrank算法\(1.0.0\)<a name="ges_03_0078"></a>

**表 1**  parameters参数说明

<a name="table421133013343"></a>
<table><thead align="left"><tr id="row1922415308344"><th class="cellrowborder" valign="top" width="16.03%" id="mcps1.2.7.1.1"><p id="p172271305349"><a name="p172271305349"></a><a name="p172271305349"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.97%" id="mcps1.2.7.1.2"><p id="p102281230113414"><a name="p102281230113414"></a><a name="p102281230113414"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.7.1.3"><p id="p11230143010349"><a name="p11230143010349"></a><a name="p11230143010349"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.7.1.4"><p id="p66074112146"><a name="p66074112146"></a><a name="p66074112146"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.7.1.5"><p id="p323393073410"><a name="p323393073410"></a><a name="p323393073410"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.7.1.6"><p id="p41583960175619"><a name="p41583960175619"></a><a name="p41583960175619"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1923843017347"><td class="cellrowborder" valign="top" width="16.03%" headers="mcps1.2.7.1.1 "><p id="p13751101797"><a name="p13751101797"></a><a name="p13751101797"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.7.1.2 "><p id="p20751701994"><a name="p20751701994"></a><a name="p20751701994"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.3 "><p id="p177515011918"><a name="p177515011918"></a><a name="p177515011918"></a>节点的ID。</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.7.1.4 "><p id="p1960715115144"><a name="p1960715115144"></a><a name="p1960715115144"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.5 "><p id="p17521018916"><a name="p17521018916"></a><a name="p17521018916"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p12857639175619"><a name="p12857639175619"></a><a name="p12857639175619"></a>-</p>
</td>
</tr>
<tr id="row1592512201673"><td class="cellrowborder" valign="top" width="16.03%" headers="mcps1.2.7.1.1 "><p id="p4752150793"><a name="p4752150793"></a><a name="p4752150793"></a>alpha</p>
</td>
<td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.7.1.2 "><p id="p127528012920"><a name="p127528012920"></a><a name="p127528012920"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.3 "><p id="p5752301191"><a name="p5752301191"></a><a name="p5752301191"></a>权重系数。</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.7.1.4 "><p id="p960731119141"><a name="p960731119141"></a><a name="p960731119141"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.5 "><p id="p8569141114913"><a name="p8569141114913"></a><a name="p8569141114913"></a>0~1，不包括0和1。</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p34835871175619"><a name="p34835871175619"></a><a name="p34835871175619"></a>0.85</p>
</td>
</tr>
<tr id="row1883311181175"><td class="cellrowborder" valign="top" width="16.03%" headers="mcps1.2.7.1.1 "><p id="p07521208912"><a name="p07521208912"></a><a name="p07521208912"></a>convergence</p>
</td>
<td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.7.1.2 "><p id="p137529015913"><a name="p137529015913"></a><a name="p137529015913"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.3 "><p id="p87521501194"><a name="p87521501194"></a><a name="p87521501194"></a>收敛精度。</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.7.1.4 "><p id="p10607111121416"><a name="p10607111121416"></a><a name="p10607111121416"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.5 "><p id="p12122017093"><a name="p12122017093"></a><a name="p12122017093"></a>0~1，不包括0和1。</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p3133287175619"><a name="p3133287175619"></a><a name="p3133287175619"></a>0.00001</p>
</td>
</tr>
<tr id="row136122160711"><td class="cellrowborder" valign="top" width="16.03%" headers="mcps1.2.7.1.1 "><p id="p20752001591"><a name="p20752001591"></a><a name="p20752001591"></a>max_iterations</p>
</td>
<td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.7.1.2 "><p id="p475210694"><a name="p475210694"></a><a name="p475210694"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.3 "><p id="p207531801297"><a name="p207531801297"></a><a name="p207531801297"></a>最大迭代次数。</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.7.1.4 "><p id="p126077114147"><a name="p126077114147"></a><a name="p126077114147"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.5 "><p id="p19133729890"><a name="p19133729890"></a><a name="p19133729890"></a>1~2000。</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p52469671175619"><a name="p52469671175619"></a><a name="p52469671175619"></a>1000</p>
</td>
</tr>
<tr id="row147071213274"><td class="cellrowborder" valign="top" width="16.03%" headers="mcps1.2.7.1.1 "><p id="p030083010342"><a name="p030083010342"></a><a name="p030083010342"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.7.1.2 "><p id="p0301193043415"><a name="p0301193043415"></a><a name="p0301193043415"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.7.1.3 "><p id="p4304183013347"><a name="p4304183013347"></a><a name="p4304183013347"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.7.1.4 "><p id="p1360721111420"><a name="p1360721111420"></a><a name="p1360721111420"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.5 "><p id="p1330963023418"><a name="p1330963023418"></a><a name="p1330963023418"></a>true或false。</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p22184968175619"><a name="p22184968175619"></a><a name="p22184968175619"></a>true</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>关于迭代次数（iterations）和收敛精度（convergence）参数如何调节，请参考[迭代次数和收敛精度的关系](pagerank算法(1-0-0).md#li137501137205318)。

**表 2**  response\_data参数说明

<a name="table145211832114419"></a>
<table><thead align="left"><tr id="row452118323447"><th class="cellrowborder" valign="top" width="31.380000000000003%" id="mcps1.2.4.1.1"><p id="p15211632194411"><a name="p15211632194411"></a><a name="p15211632194411"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.2.4.1.2"><p id="p65211732154414"><a name="p65211732154414"></a><a name="p65211732154414"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.1%" id="mcps1.2.4.1.3"><p id="p11521832134411"><a name="p11521832134411"></a><a name="p11521832134411"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2052143218447"><td class="cellrowborder" valign="top" width="31.380000000000003%" headers="mcps1.2.4.1.1 "><p id="p16521932124413"><a name="p16521932124413"></a><a name="p16521932124413"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.2.4.1.2 "><p id="p175211632124419"><a name="p175211632124419"></a><a name="p175211632124419"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.1%" headers="mcps1.2.4.1.3 "><p id="p7521432194413"><a name="p7521432194413"></a><a name="p7521432194413"></a>-</p>
</td>
</tr>
<tr id="row952183218448"><td class="cellrowborder" valign="top" width="31.380000000000003%" headers="mcps1.2.4.1.1 "><p id="p8521932114411"><a name="p8521932114411"></a><a name="p8521932114411"></a>personalrank</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.2.4.1.2 "><p id="p852123254417"><a name="p852123254417"></a><a name="p852123254417"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="49.1%" headers="mcps1.2.4.1.3 "><p id="p1044121616425"><a name="p1044121616425"></a><a name="p1044121616425"></a>各节点的personalrank值，格式：</p>
<p id="p63161133854"><a name="p63161133854"></a><a name="p63161133854"></a>[{vertexId:rankValue},...],</p>
<p id="p83008413714"><a name="p83008413714"></a><a name="p83008413714"></a>其中,</p>
<p id="p276931513620"><a name="p276931513620"></a><a name="p276931513620"></a>vertexId：string类型</p>
<p id="p42531732962"><a name="p42531732962"></a><a name="p42531732962"></a>rankValue：double类型</p>
</td>
</tr>
</tbody>
</table>

