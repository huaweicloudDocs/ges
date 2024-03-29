# 点集最短路（Shortest Path of Vertex Sets）<a name="ges_01_0054"></a>

## 概述<a name="section6298525295951"></a>

点集最短路算法（Shortest Path of Vertex Sets）用于发现两个点集之间的最短路径。

## 适用场景<a name="section1451760010033"></a>

点集最短路算法（Shortest Path of Vertex Sets）适用于互联网社交、金融风控、路网交通、物流配送等场景下的区块之间关系分析。

## 参数说明<a name="section3818483210354"></a>

**表 1**  点集最短路算法（Shortest Path of Vertex Sets）参数说明

<a name="table18500810104111"></a>
<table><thead align="left"><tr id="row18009483104111"><th class="cellrowborder" valign="top" width="12.910891089108908%" id="mcps1.2.7.1.1"><p id="p6644426810425"><a name="p6644426810425"></a><a name="p6644426810425"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.336633663366337%" id="mcps1.2.7.1.2"><p id="p1327662710425"><a name="p1327662710425"></a><a name="p1327662710425"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="23.16831683168317%" id="mcps1.2.7.1.3"><p id="p166499410425"><a name="p166499410425"></a><a name="p166499410425"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="7.148514851485148%" id="mcps1.2.7.1.4"><p id="p10389144111270"><a name="p10389144111270"></a><a name="p10389144111270"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.524752475247524%" id="mcps1.2.7.1.5"><p id="p64685010425"><a name="p64685010425"></a><a name="p64685010425"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="7.910891089108911%" id="mcps1.2.7.1.6"><p id="p5239490710425"><a name="p5239490710425"></a><a name="p5239490710425"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row66427667104111"><td class="cellrowborder" valign="top" width="12.910891089108908%" headers="mcps1.2.7.1.1 "><p id="p3138414910425"><a name="p3138414910425"></a><a name="p3138414910425"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="9.336633663366337%" headers="mcps1.2.7.1.2 "><p id="p5908813510425"><a name="p5908813510425"></a><a name="p5908813510425"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.16831683168317%" headers="mcps1.2.7.1.3 "><p id="p2140961710425"><a name="p2140961710425"></a><a name="p2140961710425"></a>起点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="7.148514851485148%" headers="mcps1.2.7.1.4 "><p id="p2445131643916"><a name="p2445131643916"></a><a name="p2445131643916"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.524752475247524%" headers="mcps1.2.7.1.5 "><p id="p14473161318277"><a name="p14473161318277"></a><a name="p14473161318277"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p847331310275"><a name="p847331310275"></a><a name="p847331310275"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="7.910891089108911%" headers="mcps1.2.7.1.6 "><p id="p964961610425"><a name="p964961610425"></a><a name="p964961610425"></a>-</p>
</td>
</tr>
<tr id="row1354819122815"><td class="cellrowborder" valign="top" width="12.910891089108908%" headers="mcps1.2.7.1.1 "><p id="p7843173202816"><a name="p7843173202816"></a><a name="p7843173202816"></a>targets</p>
</td>
<td class="cellrowborder" valign="top" width="9.336633663366337%" headers="mcps1.2.7.1.2 "><p id="p2843232152811"><a name="p2843232152811"></a><a name="p2843232152811"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.16831683168317%" headers="mcps1.2.7.1.3 "><p id="p20843332112810"><a name="p20843332112810"></a><a name="p20843332112810"></a>终点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="7.148514851485148%" headers="mcps1.2.7.1.4 "><p id="p16843123242820"><a name="p16843123242820"></a><a name="p16843123242820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.524752475247524%" headers="mcps1.2.7.1.5 "><p id="p447461312712"><a name="p447461312712"></a><a name="p447461312712"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p947441318273"><a name="p947441318273"></a><a name="p947441318273"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="7.910891089108911%" headers="mcps1.2.7.1.6 "><p id="p4354019192816"><a name="p4354019192816"></a><a name="p4354019192816"></a>-</p>
</td>
</tr>
<tr id="row44303816104111"><td class="cellrowborder" valign="top" width="12.910891089108908%" headers="mcps1.2.7.1.1 "><p id="p5524824310425"><a name="p5524824310425"></a><a name="p5524824310425"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9.336633663366337%" headers="mcps1.2.7.1.2 "><p id="p4592270710425"><a name="p4592270710425"></a><a name="p4592270710425"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.16831683168317%" headers="mcps1.2.7.1.3 "><p id="p2875176710425"><a name="p2875176710425"></a><a name="p2875176710425"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="7.148514851485148%" headers="mcps1.2.7.1.4 "><p id="p25096169392"><a name="p25096169392"></a><a name="p25096169392"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="39.524752475247524%" headers="mcps1.2.7.1.5 "><p id="p4719178410425"><a name="p4719178410425"></a><a name="p4719178410425"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="7.910891089108911%" headers="mcps1.2.7.1.6 "><p id="p6443812510425"><a name="p6443812510425"></a><a name="p6443812510425"></a>false</p>
</td>
</tr>
<tr id="row1924463813413"><td class="cellrowborder" valign="top" width="12.910891089108908%" headers="mcps1.2.7.1.1 "><p id="p1124519381417"><a name="p1124519381417"></a><a name="p1124519381417"></a>timeWindow</p>
</td>
<td class="cellrowborder" valign="top" width="9.336633663366337%" headers="mcps1.2.7.1.2 "><p id="p1524603814419"><a name="p1524603814419"></a><a name="p1524603814419"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="23.16831683168317%" headers="mcps1.2.7.1.3 "><p id="p12246838245"><a name="p12246838245"></a><a name="p12246838245"></a>用于进行时间过滤的时间窗</p>
</td>
<td class="cellrowborder" valign="top" width="7.148514851485148%" headers="mcps1.2.7.1.4 "><p id="p152466381945"><a name="p152466381945"></a><a name="p152466381945"></a>Json</p>
</td>
<td class="cellrowborder" valign="top" width="39.524752475247524%" headers="mcps1.2.7.1.5 "><p id="p1724620383410"><a name="p1724620383410"></a><a name="p1724620383410"></a>具体请参见<a href="#table98901741873">表2</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="7.910891089108911%" headers="mcps1.2.7.1.6 "><p id="p162461838948"><a name="p162461838948"></a><a name="p162461838948"></a>-</p>
</td>
</tr>
</tbody>
</table>

**表 2**  timeWindow参数说明

<a name="table98901741873"></a>
<table><thead align="left"><tr id="row38911341370"><th class="cellrowborder" valign="top" width="12.337532493501302%" id="mcps1.2.7.1.1"><p id="p389114873"><a name="p389114873"></a><a name="p389114873"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.658068386322737%" id="mcps1.2.7.1.2"><p id="p11891104674"><a name="p11891104674"></a><a name="p11891104674"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="28.63427314537093%" id="mcps1.2.7.1.3"><p id="p4891248712"><a name="p4891248712"></a><a name="p4891248712"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="7.288542291541694%" id="mcps1.2.7.1.4"><p id="p17891541170"><a name="p17891541170"></a><a name="p17891541170"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="33.52329534093182%" id="mcps1.2.7.1.5"><p id="p1789118412716"><a name="p1789118412716"></a><a name="p1789118412716"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="8.558288342331535%" id="mcps1.2.7.1.6"><p id="p98911147719"><a name="p98911147719"></a><a name="p98911147719"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row158918417712"><td class="cellrowborder" valign="top" width="12.337532493501302%" headers="mcps1.2.7.1.1 "><p id="p12891184873"><a name="p12891184873"></a><a name="p12891184873"></a>filterName</p>
</td>
<td class="cellrowborder" valign="top" width="9.658068386322737%" headers="mcps1.2.7.1.2 "><p id="p1189111418716"><a name="p1189111418716"></a><a name="p1189111418716"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="28.63427314537093%" headers="mcps1.2.7.1.3 "><p id="p189114973"><a name="p189114973"></a><a name="p189114973"></a>用于进行时间过滤的时间属性名称</p>
</td>
<td class="cellrowborder" valign="top" width="7.288542291541694%" headers="mcps1.2.7.1.4 "><p id="p108913419719"><a name="p108913419719"></a><a name="p108913419719"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="33.52329534093182%" headers="mcps1.2.7.1.5 "><p id="p168913412710"><a name="p168913412710"></a><a name="p168913412710"></a>字符串：对应的点/边上的属性作为时间</p>
</td>
<td class="cellrowborder" valign="top" width="8.558288342331535%" headers="mcps1.2.7.1.6 "><p id="p9891204378"><a name="p9891204378"></a><a name="p9891204378"></a>-</p>
</td>
</tr>
<tr id="row13891164873"><td class="cellrowborder" valign="top" width="12.337532493501302%" headers="mcps1.2.7.1.1 "><p id="p118911544711"><a name="p118911544711"></a><a name="p118911544711"></a>filterType</p>
</td>
<td class="cellrowborder" valign="top" width="9.658068386322737%" headers="mcps1.2.7.1.2 "><p id="p158918419716"><a name="p158918419716"></a><a name="p158918419716"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="28.63427314537093%" headers="mcps1.2.7.1.3 "><p id="p08916419716"><a name="p08916419716"></a><a name="p08916419716"></a>在点或边上过滤</p>
</td>
<td class="cellrowborder" valign="top" width="7.288542291541694%" headers="mcps1.2.7.1.4 "><p id="p18921941575"><a name="p18921941575"></a><a name="p18921941575"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="33.52329534093182%" headers="mcps1.2.7.1.5 "><p id="p178921419714"><a name="p178921419714"></a><a name="p178921419714"></a>V：点上</p>
<p id="p10740174331013"><a name="p10740174331013"></a><a name="p10740174331013"></a>E：边上</p>
<p id="p1343645221019"><a name="p1343645221019"></a><a name="p1343645221019"></a>BOTH：点和边上</p>
</td>
<td class="cellrowborder" valign="top" width="8.558288342331535%" headers="mcps1.2.7.1.6 "><p id="p148924419716"><a name="p148924419716"></a><a name="p148924419716"></a>BOTH</p>
</td>
</tr>
<tr id="row10892134475"><td class="cellrowborder" valign="top" width="12.337532493501302%" headers="mcps1.2.7.1.1 "><p id="p108921241276"><a name="p108921241276"></a><a name="p108921241276"></a>startTime</p>
</td>
<td class="cellrowborder" valign="top" width="9.658068386322737%" headers="mcps1.2.7.1.2 "><p id="p48921346711"><a name="p48921346711"></a><a name="p48921346711"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="28.63427314537093%" headers="mcps1.2.7.1.3 "><p id="p11892645717"><a name="p11892645717"></a><a name="p11892645717"></a>起始时间</p>
</td>
<td class="cellrowborder" valign="top" width="7.288542291541694%" headers="mcps1.2.7.1.4 "><p id="p1889210415712"><a name="p1889210415712"></a><a name="p1889210415712"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="33.52329534093182%" headers="mcps1.2.7.1.5 "><p id="p1189234870"><a name="p1189234870"></a><a name="p1189234870"></a>Date型字符串或时间戳</p>
</td>
<td class="cellrowborder" valign="top" width="8.558288342331535%" headers="mcps1.2.7.1.6 "><p id="p88921244720"><a name="p88921244720"></a><a name="p88921244720"></a>-</p>
</td>
</tr>
<tr id="row48921941577"><td class="cellrowborder" valign="top" width="12.337532493501302%" headers="mcps1.2.7.1.1 "><p id="p16824135151412"><a name="p16824135151412"></a><a name="p16824135151412"></a>endTime</p>
</td>
<td class="cellrowborder" valign="top" width="9.658068386322737%" headers="mcps1.2.7.1.2 "><p id="p178241153149"><a name="p178241153149"></a><a name="p178241153149"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="28.63427314537093%" headers="mcps1.2.7.1.3 "><p id="p3824145201419"><a name="p3824145201419"></a><a name="p3824145201419"></a>终止时间</p>
</td>
<td class="cellrowborder" valign="top" width="7.288542291541694%" headers="mcps1.2.7.1.4 "><p id="p198249581417"><a name="p198249581417"></a><a name="p198249581417"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="33.52329534093182%" headers="mcps1.2.7.1.5 "><p id="p158242510143"><a name="p158242510143"></a><a name="p158242510143"></a>Date型字符串或时间戳</p>
</td>
<td class="cellrowborder" valign="top" width="8.558288342331535%" headers="mcps1.2.7.1.6 "><p id="p4824852145"><a name="p4824852145"></a><a name="p4824852145"></a>-</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>当点的ID中含有逗号时，需在此ID上加上双引号，例如：电影“Paris, je taime”以及“Alice”两个ID作为sources时，写做："Paris, je taime",Alice"

## 示例<a name="section21511242104337"></a>

输入directed=true，sources= "Alice,Nana"，targets= "Lily,Amy"  ，JSON结果会展示在查询结果区。

