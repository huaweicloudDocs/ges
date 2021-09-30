# 带一般过滤条件环路检测（filtered circle detection）<a name="ges_01_0088"></a>

## 概述<a name="section15370184961812"></a>

带一般过滤条件环路检测（filtered circle detection）目的是寻找图中所有满足过滤条件的环路。

## 适用场景<a name="section112811508199"></a>

带一般过滤条件的环路检测\(filtered circle detection\)算法适用于金融风控中循环转账检测、反洗钱，网络路由中异常链接检测，企业担保圈贷款风险识别等场景。

## 参数说明<a name="section23411131219"></a>

**表 1**  filtered circle detection参数说明

<a name="table247213193014"></a>
<table><thead align="left"><tr id="row247613113018"><th class="cellrowborder" valign="top" width="14.207158568286344%" id="mcps1.2.7.1.1"><p id="p19473134301"><a name="p19473134301"></a><a name="p19473134301"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="7.758448310337933%" id="mcps1.2.7.1.2"><p id="p447161333015"><a name="p447161333015"></a><a name="p447161333015"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="25.624875024995%" id="mcps1.2.7.1.3"><p id="p4471713143017"><a name="p4471713143017"></a><a name="p4471713143017"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.078184363127376%" id="mcps1.2.7.1.4"><p id="p447913163017"><a name="p447913163017"></a><a name="p447913163017"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="26.664667066586684%" id="mcps1.2.7.1.5"><p id="p1047213123015"><a name="p1047213123015"></a><a name="p1047213123015"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="16.666666666666664%" id="mcps1.2.7.1.6"><p id="p154871316304"><a name="p154871316304"></a><a name="p154871316304"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row5483137305"><td class="cellrowborder" valign="top" width="14.207158568286344%" headers="mcps1.2.7.1.1 "><p id="p14831316305"><a name="p14831316305"></a><a name="p14831316305"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="7.758448310337933%" headers="mcps1.2.7.1.2 "><p id="p348313163019"><a name="p348313163019"></a><a name="p348313163019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.624875024995%" headers="mcps1.2.7.1.3 "><p id="p154811315304"><a name="p154811315304"></a><a name="p154811315304"></a>查询的起始节点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="9.078184363127376%" headers="mcps1.2.7.1.4 "><p id="p74851315302"><a name="p74851315302"></a><a name="p74851315302"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="26.664667066586684%" headers="mcps1.2.7.1.5 "><p id="p1848141333012"><a name="p1848141333012"></a><a name="p1848141333012"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p1648161373011"><a name="p1648161373011"></a><a name="p1648161373011"></a>标准csv格式，ID之间以英文逗号分隔，例如:“Alice,Nana”</p>
</td>
</tr>
<tr id="row24861313010"><td class="cellrowborder" valign="top" width="14.207158568286344%" headers="mcps1.2.7.1.1 "><p id="p648313143017"><a name="p648313143017"></a><a name="p648313143017"></a>n</p>
</td>
<td class="cellrowborder" valign="top" width="7.758448310337933%" headers="mcps1.2.7.1.2 "><p id="p848201311301"><a name="p848201311301"></a><a name="p848201311301"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.624875024995%" headers="mcps1.2.7.1.3 "><p id="p14817131301"><a name="p14817131301"></a><a name="p14817131301"></a>枚举满足过滤条件的圈的个数上限</p>
</td>
<td class="cellrowborder" valign="top" width="9.078184363127376%" headers="mcps1.2.7.1.4 "><p id="p84851333018"><a name="p84851333018"></a><a name="p84851333018"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="26.664667066586684%" headers="mcps1.2.7.1.5 "><p id="p648181314308"><a name="p648181314308"></a><a name="p648181314308"></a>[1,100000]</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p54851373013"><a name="p54851373013"></a><a name="p54851373013"></a>100</p>
</td>
</tr>
<tr id="row17487138306"><td class="cellrowborder" valign="top" width="14.207158568286344%" headers="mcps1.2.7.1.1 "><p id="p15488138304"><a name="p15488138304"></a><a name="p15488138304"></a>statistics</p>
</td>
<td class="cellrowborder" valign="top" width="7.758448310337933%" headers="mcps1.2.7.1.2 "><p id="p174801303014"><a name="p174801303014"></a><a name="p174801303014"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.624875024995%" headers="mcps1.2.7.1.3 "><p id="p249111363018"><a name="p249111363018"></a><a name="p249111363018"></a>是否输出所有满足过滤条件的圈的个数</p>
</td>
<td class="cellrowborder" valign="top" width="9.078184363127376%" headers="mcps1.2.7.1.4 "><p id="p6491013153012"><a name="p6491013153012"></a><a name="p6491013153012"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="26.664667066586684%" headers="mcps1.2.7.1.5 "><p id="p12491513123020"><a name="p12491513123020"></a><a name="p12491513123020"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p3491713143018"><a name="p3491713143018"></a><a name="p3491713143018"></a>false</p>
</td>
</tr>
<tr id="row449813113015"><td class="cellrowborder" valign="top" width="14.207158568286344%" headers="mcps1.2.7.1.1 "><p id="p1749513173014"><a name="p1749513173014"></a><a name="p1749513173014"></a>batch_number</p>
</td>
<td class="cellrowborder" valign="top" width="7.758448310337933%" headers="mcps1.2.7.1.2 "><p id="p149111353018"><a name="p149111353018"></a><a name="p149111353018"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.624875024995%" headers="mcps1.2.7.1.3 "><p id="p44911316306"><a name="p44911316306"></a><a name="p44911316306"></a>批量处理的起始节点的个数</p>
</td>
<td class="cellrowborder" valign="top" width="9.078184363127376%" headers="mcps1.2.7.1.4 "><p id="p18491513173017"><a name="p18491513173017"></a><a name="p18491513173017"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="26.664667066586684%" headers="mcps1.2.7.1.5 "><p id="p16491813183019"><a name="p16491813183019"></a><a name="p16491813183019"></a>[1,1000]</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p154981313307"><a name="p154981313307"></a><a name="p154981313307"></a>10</p>
</td>
</tr>
<tr id="row849171343010"><td class="cellrowborder" valign="top" width="14.207158568286344%" headers="mcps1.2.7.1.1 "><p id="p1649171353015"><a name="p1649171353015"></a><a name="p1649171353015"></a>output_format</p>
</td>
<td class="cellrowborder" valign="top" width="7.758448310337933%" headers="mcps1.2.7.1.2 "><p id="p10501213193018"><a name="p10501213193018"></a><a name="p10501213193018"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="25.624875024995%" headers="mcps1.2.7.1.3 "><p id="p1950813103016"><a name="p1950813103016"></a><a name="p1950813103016"></a>输出结果的格式</p>
</td>
<td class="cellrowborder" valign="top" width="9.078184363127376%" headers="mcps1.2.7.1.4 "><p id="p165031343012"><a name="p165031343012"></a><a name="p165031343012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="26.664667066586684%" headers="mcps1.2.7.1.5 "><p id="p15031317308"><a name="p15031317308"></a><a name="p15031317308"></a>vertexId，edgeId或edgeObject</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p550013143016"><a name="p550013143016"></a><a name="p550013143016"></a>edgeObject</p>
</td>
</tr>
<tr id="row1337718395586"><td class="cellrowborder" valign="top" width="14.207158568286344%" headers="mcps1.2.7.1.1 "><p id="p754332411112"><a name="p754332411112"></a><a name="p754332411112"></a>filters</p>
</td>
<td class="cellrowborder" valign="top" width="7.758448310337933%" headers="mcps1.2.7.1.2 "><p id="p5543224121119"><a name="p5543224121119"></a><a name="p5543224121119"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.624875024995%" headers="mcps1.2.7.1.3 "><p id="p174164716386"><a name="p174164716386"></a><a name="p174164716386"></a>过滤条件列表，数组的每个元素分别对应每一层要做的查询和过滤条件。</p>
</td>
<td class="cellrowborder" valign="top" width="9.078184363127376%" headers="mcps1.2.7.1.4 "><p id="p978463893810"><a name="p978463893810"></a><a name="p978463893810"></a>Json</p>
<p id="p9698241104016"><a name="p9698241104016"></a><a name="p9698241104016"></a></p>
</td>
<td class="cellrowborder" valign="top" width="26.664667066586684%" headers="mcps1.2.7.1.5 "><p id="p334221603816"><a name="p334221603816"></a><a name="p334221603816"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p534213161380"><a name="p534213161380"></a><a name="p534213161380"></a>-</p>
</td>
</tr>
</tbody>
</table>

