# 实时推荐算法（Real-time Recommendation）<a name="ges_01_0047"></a>

## 概述<a name="section204471932366"></a>

实时推荐算法（Real-time Recommendation）是一种基于随机游走模型的实时推荐算法，能够推荐与输入节点相近程度高、关系或喜好相近的节点。

## 适用场景<a name="section3659039393823"></a>

实时推荐算法（Real-time Recommendation）可以基于历史购买和浏览数据进行相近商品推荐，也可以为用户进行相近喜好的潜在好友推荐。

适用于电商、社交等多领域的推荐场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  实时推荐算法（Real-time Recommendation）参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="9.525252525252524%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.05050505050505%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="43.04040404040404%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="8.93939393939394%" id="mcps1.2.7.1.4"><p id="p82715505250"><a name="p82715505250"></a><a name="p82715505250"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="21.363636363636363%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="8.080808080808081%" id="mcps1.2.7.1.6"><p id="p59749194165124"><a name="p59749194165124"></a><a name="p59749194165124"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="9.525252525252524%" headers="mcps1.2.7.1.1 "><p id="p167521433132020"><a name="p167521433132020"></a><a name="p167521433132020"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.2 "><p id="p17754134012201"><a name="p17754134012201"></a><a name="p17754134012201"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="43.04040404040404%" headers="mcps1.2.7.1.3 "><p id="p1398074842019"><a name="p1398074842019"></a><a name="p1398074842019"></a>节点的ID，可以是多个。</p>
</td>
<td class="cellrowborder" valign="top" width="8.93939393939394%" headers="mcps1.2.7.1.4 "><p id="p192855017259"><a name="p192855017259"></a><a name="p192855017259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="21.363636363636363%" headers="mcps1.2.7.1.5 "><p id="p18347182714232"><a name="p18347182714232"></a><a name="p18347182714232"></a>source节点的个数不超过30个</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.7.1.6 "><p id="p7846531165124"><a name="p7846531165124"></a><a name="p7846531165124"></a>-</p>
</td>
</tr>
<tr id="row1592512201673"><td class="cellrowborder" valign="top" width="9.525252525252524%" headers="mcps1.2.7.1.1 "><p id="p275213333204"><a name="p275213333204"></a><a name="p275213333204"></a>alpha</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.2 "><p id="p67544407208"><a name="p67544407208"></a><a name="p67544407208"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="43.04040404040404%" headers="mcps1.2.7.1.3 "><p id="p189801148182017"><a name="p189801148182017"></a><a name="p189801148182017"></a>权重系数，其值越大，步长越长。</p>
</td>
<td class="cellrowborder" valign="top" width="8.93939393939394%" headers="mcps1.2.7.1.4 "><p id="p228175072519"><a name="p228175072519"></a><a name="p228175072519"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="21.363636363636363%" headers="mcps1.2.7.1.5 "><p id="p19950180162417"><a name="p19950180162417"></a><a name="p19950180162417"></a>0~1，不包括0和1</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.7.1.6 "><p id="p31589273165124"><a name="p31589273165124"></a><a name="p31589273165124"></a>0.85</p>
</td>
</tr>
<tr id="row1883311181175"><td class="cellrowborder" valign="top" width="9.525252525252524%" headers="mcps1.2.7.1.1 "><p id="p1375213337208"><a name="p1375213337208"></a><a name="p1375213337208"></a>N</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.2 "><p id="p1375484011202"><a name="p1375484011202"></a><a name="p1375484011202"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="43.04040404040404%" headers="mcps1.2.7.1.3 "><p id="p1398054852016"><a name="p1398054852016"></a><a name="p1398054852016"></a>总的游走步数。</p>
</td>
<td class="cellrowborder" valign="top" width="8.93939393939394%" headers="mcps1.2.7.1.4 "><p id="p528250182513"><a name="p528250182513"></a><a name="p528250182513"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="21.363636363636363%" headers="mcps1.2.7.1.5 "><p id="p186981016142419"><a name="p186981016142419"></a><a name="p186981016142419"></a>1~200000</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.7.1.6 "><p id="p8594291165124"><a name="p8594291165124"></a><a name="p8594291165124"></a>10000</p>
</td>
</tr>
<tr id="row20365740191015"><td class="cellrowborder" valign="top" width="9.525252525252524%" headers="mcps1.2.7.1.1 "><p id="p97521333192010"><a name="p97521333192010"></a><a name="p97521333192010"></a>nv</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.2 "><p id="p137543409209"><a name="p137543409209"></a><a name="p137543409209"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="43.04040404040404%" headers="mcps1.2.7.1.3 "><p id="p5451359192727"><a name="p5451359192727"></a><a name="p5451359192727"></a>游走过程提前结束参数：候选推荐节点访问次数的最小值。</p>
<div class="note" id="note476272392727"><a name="note476272392727"></a><a name="note476272392727"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p4523345092742"><a name="p4523345092742"></a><a name="p4523345092742"></a>对于一个节点，如果其在随机游走过程被访问到，且被访问到的次数达到<span class="parmname" id="parmname4979810192743"><a name="parmname4979810192743"></a><a name="parmname4979810192743"></a>“nv”</span>，则该节点将记入候选推荐的节点。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="8.93939393939394%" headers="mcps1.2.7.1.4 "><p id="p132805062513"><a name="p132805062513"></a><a name="p132805062513"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="21.363636363636363%" headers="mcps1.2.7.1.5 "><p id="p11449161112417"><a name="p11449161112417"></a><a name="p11449161112417"></a>1~10</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.7.1.6 "><p id="p25048953165124"><a name="p25048953165124"></a><a name="p25048953165124"></a>5</p>
</td>
</tr>
<tr id="row136122160711"><td class="cellrowborder" valign="top" width="9.525252525252524%" headers="mcps1.2.7.1.1 "><p id="p14752103315207"><a name="p14752103315207"></a><a name="p14752103315207"></a>np</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.2 "><p id="p475454010208"><a name="p475454010208"></a><a name="p475454010208"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="43.04040404040404%" headers="mcps1.2.7.1.3 "><p id="p3663800292927"><a name="p3663800292927"></a><a name="p3663800292927"></a>游走过程提前结束参数：候选推荐节点个数。</p>
<div class="note" id="note3023786192927"><a name="note3023786192927"></a><a name="note3023786192927"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p370529392927"><a name="p370529392927"></a><a name="p370529392927"></a>若某个source节点的候选推荐节点达到<span class="parmname" id="parmname141088329305"><a name="parmname141088329305"></a><a name="parmname141088329305"></a>“np”</span>，对于该source节点的随机游走将提前结束。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="8.93939393939394%" headers="mcps1.2.7.1.4 "><p id="p102865072517"><a name="p102865072517"></a><a name="p102865072517"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="21.363636363636363%" headers="mcps1.2.7.1.5 "><p id="p744711192420"><a name="p744711192420"></a><a name="p744711192420"></a>1~2000</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.7.1.6 "><p id="p15699349165124"><a name="p15699349165124"></a><a name="p15699349165124"></a>1000</p>
</td>
</tr>
<tr id="row147071213274"><td class="cellrowborder" valign="top" width="9.525252525252524%" headers="mcps1.2.7.1.1 "><p id="p17524336203"><a name="p17524336203"></a><a name="p17524336203"></a>label</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.2 "><p id="p8754144092019"><a name="p8754144092019"></a><a name="p8754144092019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="43.04040404040404%" headers="mcps1.2.7.1.3 "><p id="p516332493115"><a name="p516332493115"></a><a name="p516332493115"></a>希望输出的点的类型。</p>
<div class="note" id="note2265199293115"><a name="note2265199293115"></a><a name="note2265199293115"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul937663693135"></a><a name="ul937663693135"></a><ul id="ul937663693135"><li>其值为空时，将不考虑点的类型，输出算法原始计算结果。</li><li>对其赋值时，将从计算结果中过滤出具有该<span class="parmname" id="parmname619317093342"><a name="parmname619317093342"></a><a name="parmname619317093342"></a>“label”</span>的点的返回。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="8.93939393939394%" headers="mcps1.2.7.1.4 "><p id="p128250162514"><a name="p128250162514"></a><a name="p128250162514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="21.363636363636363%" headers="mcps1.2.7.1.5 "><p id="p12444161113248"><a name="p12444161113248"></a><a name="p12444161113248"></a>节点label</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.7.1.6 "><p id="p63687724165124"><a name="p63687724165124"></a><a name="p63687724165124"></a>-</p>
</td>
</tr>
<tr id="row946422422018"><td class="cellrowborder" valign="top" width="9.525252525252524%" headers="mcps1.2.7.1.1 "><p id="p1752133382015"><a name="p1752133382015"></a><a name="p1752133382015"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.2 "><p id="p2754104032013"><a name="p2754104032013"></a><a name="p2754104032013"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="43.04040404040404%" headers="mcps1.2.7.1.3 "><p id="p998110487206"><a name="p998110487206"></a><a name="p998110487206"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="8.93939393939394%" headers="mcps1.2.7.1.4 "><p id="p728050152518"><a name="p728050152518"></a><a name="p728050152518"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="21.363636363636363%" headers="mcps1.2.7.1.5 "><p id="p1944117118247"><a name="p1944117118247"></a><a name="p1944117118247"></a>true 或false</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.7.1.6 "><p id="p58432040165124"><a name="p58432040165124"></a><a name="p58432040165124"></a>true</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

结束条件中，nv和np越小，实时推荐算法（Real-time Recommendation）提前结束越快。

## 示例<a name="section9539286457"></a>

输入参数sources =Lee，alpha=0.85，N=10000，nv=5，np=1000，label为空，directed=true。

计算结果中的top节点组成的子图会展示在绘图区，节点大小根据最终的score值的大小来区别，JSON结果会展示在查询结果区。

