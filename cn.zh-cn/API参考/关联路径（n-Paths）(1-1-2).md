# 关联路径（n-Paths）\(1.1.2\)<a name="ges_03_0083"></a>

**表 1**  parameters参数说明

<a name="table12367516203915"></a>
<table><thead align="left"><tr id="row339741616393"><th class="cellrowborder" valign="top" width="14.06930693069307%" id="mcps1.2.7.1.1"><p id="p14400216193916"><a name="p14400216193916"></a><a name="p14400216193916"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.653465346534652%" id="mcps1.2.7.1.2"><p id="p13404181620397"><a name="p13404181620397"></a><a name="p13404181620397"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="25.2970297029703%" id="mcps1.2.7.1.3"><p id="p641051613395"><a name="p641051613395"></a><a name="p641051613395"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="13.108910891089106%" id="mcps1.2.7.1.4"><p id="p4414101613912"><a name="p4414101613912"></a><a name="p4414101613912"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="15.059405940594061%" id="mcps1.2.7.1.5"><p id="p84189166391"><a name="p84189166391"></a><a name="p84189166391"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="18.81188118811881%" id="mcps1.2.7.1.6"><p id="p1642591610399"><a name="p1642591610399"></a><a name="p1642591610399"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row2429181693918"><td class="cellrowborder" valign="top" width="14.06930693069307%" headers="mcps1.2.7.1.1 "><p id="p1243371603914"><a name="p1243371603914"></a><a name="p1243371603914"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="13.653465346534652%" headers="mcps1.2.7.1.2 "><p id="p20438141614394"><a name="p20438141614394"></a><a name="p20438141614394"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.2970297029703%" headers="mcps1.2.7.1.3 "><p id="p1644101613398"><a name="p1644101613398"></a><a name="p1644101613398"></a>输入路径的起点ID。</p>
</td>
<td class="cellrowborder" valign="top" width="13.108910891089106%" headers="mcps1.2.7.1.4 "><p id="p2445131643916"><a name="p2445131643916"></a><a name="p2445131643916"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="15.059405940594061%" headers="mcps1.2.7.1.5 "><p id="p54501216143913"><a name="p54501216143913"></a><a name="p54501216143913"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p1145612169397"><a name="p1145612169397"></a><a name="p1145612169397"></a>-</p>
</td>
</tr>
<tr id="row1354819122815"><td class="cellrowborder" valign="top" width="14.06930693069307%" headers="mcps1.2.7.1.1 "><p id="p7843173202816"><a name="p7843173202816"></a><a name="p7843173202816"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="13.653465346534652%" headers="mcps1.2.7.1.2 "><p id="p2843232152811"><a name="p2843232152811"></a><a name="p2843232152811"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.2970297029703%" headers="mcps1.2.7.1.3 "><p id="p20843332112810"><a name="p20843332112810"></a><a name="p20843332112810"></a>输入路径的终点ID。</p>
</td>
<td class="cellrowborder" valign="top" width="13.108910891089106%" headers="mcps1.2.7.1.4 "><p id="p16843123242820"><a name="p16843123242820"></a><a name="p16843123242820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="15.059405940594061%" headers="mcps1.2.7.1.5 "><p id="p118434321281"><a name="p118434321281"></a><a name="p118434321281"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p4354019192816"><a name="p4354019192816"></a><a name="p4354019192816"></a>-</p>
</td>
</tr>
<tr id="row154931916173919"><td class="cellrowborder" valign="top" width="14.06930693069307%" headers="mcps1.2.7.1.1 "><p id="p12498171613913"><a name="p12498171613913"></a><a name="p12498171613913"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="13.653465346534652%" headers="mcps1.2.7.1.2 "><p id="p7503121617391"><a name="p7503121617391"></a><a name="p7503121617391"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.2970297029703%" headers="mcps1.2.7.1.3 "><p id="p165069165398"><a name="p165069165398"></a><a name="p165069165398"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="13.108910891089106%" headers="mcps1.2.7.1.4 "><p id="p25096169392"><a name="p25096169392"></a><a name="p25096169392"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="15.059405940594061%" headers="mcps1.2.7.1.5 "><p id="p165141916143910"><a name="p165141916143910"></a><a name="p165141916143910"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p152221616393"><a name="p152221616393"></a><a name="p152221616393"></a>false</p>
</td>
</tr>
<tr id="row1442014612715"><td class="cellrowborder" valign="top" width="14.06930693069307%" headers="mcps1.2.7.1.1 "><p id="p16421762277"><a name="p16421762277"></a><a name="p16421762277"></a>n</p>
</td>
<td class="cellrowborder" valign="top" width="13.653465346534652%" headers="mcps1.2.7.1.2 "><p id="p242113652712"><a name="p242113652712"></a><a name="p242113652712"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.2970297029703%" headers="mcps1.2.7.1.3 "><p id="p1942196102713"><a name="p1942196102713"></a><a name="p1942196102713"></a>路径个数。</p>
</td>
<td class="cellrowborder" valign="top" width="13.108910891089106%" headers="mcps1.2.7.1.4 "><p id="p44214613279"><a name="p44214613279"></a><a name="p44214613279"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="15.059405940594061%" headers="mcps1.2.7.1.5 "><p id="p16421176192718"><a name="p16421176192718"></a><a name="p16421176192718"></a>1~100</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p7421136142714"><a name="p7421136142714"></a><a name="p7421136142714"></a>10</p>
</td>
</tr>
<tr id="row962318191744"><td class="cellrowborder" valign="top" width="14.06930693069307%" headers="mcps1.2.7.1.1 "><p id="p3624419047"><a name="p3624419047"></a><a name="p3624419047"></a>upper_check</p>
</td>
<td class="cellrowborder" valign="top" width="13.653465346534652%" headers="mcps1.2.7.1.2 "><p id="p196241195416"><a name="p196241195416"></a><a name="p196241195416"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.2970297029703%" headers="mcps1.2.7.1.3 "><p id="p19624119441"><a name="p19624119441"></a><a name="p19624119441"></a>放松n的限制，当该参数为false时，n无效，不再校验n范围。</p>
</td>
<td class="cellrowborder" valign="top" width="13.108910891089106%" headers="mcps1.2.7.1.4 "><p id="p1862412195417"><a name="p1862412195417"></a><a name="p1862412195417"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="15.059405940594061%" headers="mcps1.2.7.1.5 "><p id="p156243192412"><a name="p156243192412"></a><a name="p156243192412"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p166252192419"><a name="p166252192419"></a><a name="p166252192419"></a>-</p>
</td>
</tr>
<tr id="row042112682720"><td class="cellrowborder" valign="top" width="14.06930693069307%" headers="mcps1.2.7.1.1 "><p id="p042176132710"><a name="p042176132710"></a><a name="p042176132710"></a>k</p>
</td>
<td class="cellrowborder" valign="top" width="13.653465346534652%" headers="mcps1.2.7.1.2 "><p id="p14211463277"><a name="p14211463277"></a><a name="p14211463277"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.2970297029703%" headers="mcps1.2.7.1.3 "><p id="p16421146142718"><a name="p16421146142718"></a><a name="p16421146142718"></a>层数。</p>
</td>
<td class="cellrowborder" valign="top" width="13.108910891089106%" headers="mcps1.2.7.1.4 "><p id="p1642116622714"><a name="p1642116622714"></a><a name="p1642116622714"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="15.059405940594061%" headers="mcps1.2.7.1.5 "><p id="p1421126172715"><a name="p1421126172715"></a><a name="p1421126172715"></a>1~10</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.7.1.6 "><p id="p94211466272"><a name="p94211466272"></a><a name="p94211466272"></a>5</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table32881853474"></a>
<table><thead align="left"><tr id="row9288115114718"><th class="cellrowborder" valign="top" width="22.63%" id="mcps1.2.4.1.1"><p id="p5302353479"><a name="p5302353479"></a><a name="p5302353479"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.35%" id="mcps1.2.4.1.2"><p id="p18302175194717"><a name="p18302175194717"></a><a name="p18302175194717"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="54.02%" id="mcps1.2.4.1.3"><p id="p6302655476"><a name="p6302655476"></a><a name="p6302655476"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row9553165153818"><td class="cellrowborder" valign="top" width="22.63%" headers="mcps1.2.4.1.1 "><p id="p75531651163817"><a name="p75531651163817"></a><a name="p75531651163817"></a>paths</p>
</td>
<td class="cellrowborder" valign="top" width="23.35%" headers="mcps1.2.4.1.2 "><p id="p1553175173812"><a name="p1553175173812"></a><a name="p1553175173812"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="54.02%" headers="mcps1.2.4.1.3 "><p id="p126941653599"><a name="p126941653599"></a><a name="p126941653599"></a>source节点和target节点之间的路径，格式：</p>
<p id="p86944515596"><a name="p86944515596"></a><a name="p86944515596"></a>[[path1],[path2]]</p>
<p id="p13522949115819"><a name="p13522949115819"></a><a name="p13522949115819"></a>其中，</p>
<p id="p9216437572"><a name="p9216437572"></a><a name="p9216437572"></a>路径（path）的格式可参考：<a href="最短路径（Shortest-Path）(1-0-0).md">最短路径（Shortest Path）(1.0.0)</a></p>
</td>
</tr>
<tr id="row198912301083"><td class="cellrowborder" valign="top" width="22.63%" headers="mcps1.2.4.1.1 "><p id="p18891143016810"><a name="p18891143016810"></a><a name="p18891143016810"></a>paths_number</p>
</td>
<td class="cellrowborder" valign="top" width="23.35%" headers="mcps1.2.4.1.2 "><p id="p88910301689"><a name="p88910301689"></a><a name="p88910301689"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="54.02%" headers="mcps1.2.4.1.3 "><p id="p0891113019814"><a name="p0891113019814"></a><a name="p0891113019814"></a>路径个数</p>
</td>
</tr>
<tr id="row630213511479"><td class="cellrowborder" valign="top" width="22.63%" headers="mcps1.2.4.1.1 "><p id="p12302165104716"><a name="p12302165104716"></a><a name="p12302165104716"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="23.35%" headers="mcps1.2.4.1.2 "><p id="p33021755478"><a name="p33021755478"></a><a name="p33021755478"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.02%" headers="mcps1.2.4.1.3 "><p id="p173022514717"><a name="p173022514717"></a><a name="p173022514717"></a>起点ID</p>
</td>
</tr>
<tr id="row63021956479"><td class="cellrowborder" valign="top" width="22.63%" headers="mcps1.2.4.1.1 "><p id="p1330215534715"><a name="p1330215534715"></a><a name="p1330215534715"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="23.35%" headers="mcps1.2.4.1.2 "><p id="p133029519472"><a name="p133029519472"></a><a name="p133029519472"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.02%" headers="mcps1.2.4.1.3 "><p id="p1930215510478"><a name="p1930215510478"></a><a name="p1930215510478"></a>终点ID</p>
</td>
</tr>
</tbody>
</table>

