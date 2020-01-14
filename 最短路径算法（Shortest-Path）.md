# 最短路径算法（Shortest Path）<a name="ges_01_0035"></a>

## 概述<a name="section204471932366"></a>

最短路径算法（Shortest Path）用以解决图论研究中的一个经典算法问题，旨在寻找图中两节点之间的最短路径。

## 适用场景<a name="section2555716895357"></a>

最短路径算法（Shortest Path）适用于路径规划、网络规划等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  最短路径算法（Shortest Path）参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="13.861386138613863%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.564356435643564%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.247524752475247%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.306930693069306%" id="mcps1.2.7.1.4"><p id="p119692498180"><a name="p119692498180"></a><a name="p119692498180"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="38.78217821782178%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="9.237623762376238%" id="mcps1.2.7.1.6"><p id="p19958237181732"><a name="p19958237181732"></a><a name="p19958237181732"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p1143990987"><a name="p1143990987"></a><a name="p1143990987"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p82629131588"><a name="p82629131588"></a><a name="p82629131588"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p443910016812"><a name="p443910016812"></a><a name="p443910016812"></a>输入路径的起点ID</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p19969174991814"><a name="p19969174991814"></a><a name="p19969174991814"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p19637130201011"><a name="p19637130201011"></a><a name="p19637130201011"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p6004471181732"><a name="p6004471181732"></a><a name="p6004471181732"></a>-</p>
</td>
</tr>
<tr id="row144392001589"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p543916014814"><a name="p543916014814"></a><a name="p543916014814"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p11262161310820"><a name="p11262161310820"></a><a name="p11262161310820"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p104392003812"><a name="p104392003812"></a><a name="p104392003812"></a>输入路径的终点ID</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p1896954920183"><a name="p1896954920183"></a><a name="p1896954920183"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p143915011811"><a name="p143915011811"></a><a name="p143915011811"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p16600125181732"><a name="p16600125181732"></a><a name="p16600125181732"></a>-</p>
</td>
</tr>
<tr id="row1098765711187"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p28489604113145"><a name="p28489604113145"></a><a name="p28489604113145"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p25956591113145"><a name="p25956591113145"></a><a name="p25956591113145"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p22109102113145"><a name="p22109102113145"></a><a name="p22109102113145"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p4969649161820"><a name="p4969649161820"></a><a name="p4969649161820"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p46006826113145"><a name="p46006826113145"></a><a name="p46006826113145"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p62848880181732"><a name="p62848880181732"></a><a name="p62848880181732"></a>false</p>
</td>
</tr>
<tr id="row38613385112333"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p40676518112333"><a name="p40676518112333"></a><a name="p40676518112333"></a>weight</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p6463651112333"><a name="p6463651112333"></a><a name="p6463651112333"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p53793704112333"><a name="p53793704112333"></a><a name="p53793704112333"></a>边上权重</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p1496924971820"><a name="p1496924971820"></a><a name="p1496924971820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p1666044011283"><a name="p1666044011283"></a><a name="p1666044011283"></a>空或字符串</p>
<a name="ul27814585182326"></a><a name="ul27814585182326"></a><ul id="ul27814585182326"><li>空：边上的权重、距离默认为<span class="parmname" id="parmname64281841182434"><a name="parmname64281841182434"></a><a name="parmname64281841182434"></a>“1”</span>。</li><li>字符串：对应的边上的属性将作为权重，当某边没有对应属性时，权重将默认为1。<div class="note" id="note1763697295448"><a name="note1763697295448"></a><a name="note1763697295448"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p6598326895457"><a name="p6598326895457"></a><a name="p6598326895457"></a>边上权重应大于0。</p>
</div></div>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p2432921181732"><a name="p2432921181732"></a><a name="p2432921181732"></a>-</p>
</td>
</tr>
<tr id="row18578822113145"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p1124519381417"><a name="p1124519381417"></a><a name="p1124519381417"></a>timeWindow</p>
</td>
<td class="cellrowborder" valign="top" width="9.564356435643564%" headers="mcps1.2.7.1.2 "><p id="p1524603814419"><a name="p1524603814419"></a><a name="p1524603814419"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.247524752475247%" headers="mcps1.2.7.1.3 "><p id="p12246838245"><a name="p12246838245"></a><a name="p12246838245"></a>用于进行时间过滤的时间窗</p>
</td>
<td class="cellrowborder" valign="top" width="9.306930693069306%" headers="mcps1.2.7.1.4 "><p id="p152466381945"><a name="p152466381945"></a><a name="p152466381945"></a>JSON</p>
</td>
<td class="cellrowborder" valign="top" width="38.78217821782178%" headers="mcps1.2.7.1.5 "><p id="p1724620383410"><a name="p1724620383410"></a><a name="p1724620383410"></a>具体请参见<a href="#table98901741873">表2</a>。</p>
<div class="note" id="note426316587192"><a name="note426316587192"></a><a name="note426316587192"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p6265135813195"><a name="p6265135813195"></a><a name="p6265135813195"></a>timeWindow目前不支持带weight的最短路，即timeWindow与weight不可同时输入。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="9.237623762376238%" headers="mcps1.2.7.1.6 "><p id="p162461838948"><a name="p162461838948"></a><a name="p162461838948"></a>-</p>
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
<th class="cellrowborder" valign="top" width="28.64427114577085%" id="mcps1.2.7.1.3"><p id="p4891248712"><a name="p4891248712"></a><a name="p4891248712"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="7.278544291141774%" id="mcps1.2.7.1.4"><p id="p17891541170"><a name="p17891541170"></a><a name="p17891541170"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="33.52329534093182%" id="mcps1.2.7.1.5"><p id="p1789118412716"><a name="p1789118412716"></a><a name="p1789118412716"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="8.558288342331535%" id="mcps1.2.7.1.6"><p id="p98911147719"><a name="p98911147719"></a><a name="p98911147719"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row158918417712"><td class="cellrowborder" valign="top" width="12.337532493501302%" headers="mcps1.2.7.1.1 "><p id="p12891184873"><a name="p12891184873"></a><a name="p12891184873"></a>filterName</p>
</td>
<td class="cellrowborder" valign="top" width="9.658068386322737%" headers="mcps1.2.7.1.2 "><p id="p1189111418716"><a name="p1189111418716"></a><a name="p1189111418716"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="28.64427114577085%" headers="mcps1.2.7.1.3 "><p id="p189114973"><a name="p189114973"></a><a name="p189114973"></a>用于进行时间过滤的时间属性名称</p>
</td>
<td class="cellrowborder" valign="top" width="7.278544291141774%" headers="mcps1.2.7.1.4 "><p id="p108913419719"><a name="p108913419719"></a><a name="p108913419719"></a>String</p>
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
<td class="cellrowborder" valign="top" width="28.64427114577085%" headers="mcps1.2.7.1.3 "><p id="p08916419716"><a name="p08916419716"></a><a name="p08916419716"></a>在点或边上过滤</p>
</td>
<td class="cellrowborder" valign="top" width="7.278544291141774%" headers="mcps1.2.7.1.4 "><p id="p18921941575"><a name="p18921941575"></a><a name="p18921941575"></a>String</p>
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
<td class="cellrowborder" valign="top" width="28.64427114577085%" headers="mcps1.2.7.1.3 "><p id="p11892645717"><a name="p11892645717"></a><a name="p11892645717"></a>起始时间</p>
</td>
<td class="cellrowborder" valign="top" width="7.278544291141774%" headers="mcps1.2.7.1.4 "><p id="p1889210415712"><a name="p1889210415712"></a><a name="p1889210415712"></a>String</p>
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
<td class="cellrowborder" valign="top" width="28.64427114577085%" headers="mcps1.2.7.1.3 "><p id="p3824145201419"><a name="p3824145201419"></a><a name="p3824145201419"></a>终止时间</p>
</td>
<td class="cellrowborder" valign="top" width="7.278544291141774%" headers="mcps1.2.7.1.4 "><p id="p198249581417"><a name="p198249581417"></a><a name="p198249581417"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="33.52329534093182%" headers="mcps1.2.7.1.5 "><p id="p158242510143"><a name="p158242510143"></a><a name="p158242510143"></a>Date型字符串或时间戳</p>
</td>
<td class="cellrowborder" valign="top" width="8.558288342331535%" headers="mcps1.2.7.1.6 "><p id="p4824852145"><a name="p4824852145"></a><a name="p4824852145"></a>-</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

最短路径算法（Shortest Path）只返回一条最短路径。

## 示例<a name="section9539286457"></a>

计算从Lee节点到Alice节点的一条最短路径。

输入参数source=Lee，target=Alice，weight=weights，directed=false。最短路径会展示在绘图区，JSON结果会展示在查询结果区。

