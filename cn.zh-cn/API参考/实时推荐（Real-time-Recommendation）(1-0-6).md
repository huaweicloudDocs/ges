# 实时推荐（Real-time Recommendation）\(1.0.6\)<a name="ges_03_0090"></a>

**表 1**  parameters参数说明

<a name="table2365111514407"></a>
<table><thead align="left"><tr id="row1639618152403"><th class="cellrowborder" valign="top" width="12.112244897959185%" id="mcps1.2.7.1.1"><p id="p114016159405"><a name="p114016159405"></a><a name="p114016159405"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.234693877551022%" id="mcps1.2.7.1.2"><p id="p1640617154404"><a name="p1640617154404"></a><a name="p1640617154404"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="39.31632653061225%" id="mcps1.2.7.1.3"><p id="p84130158408"><a name="p84130158408"></a><a name="p84130158408"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.918367346938776%" id="mcps1.2.7.1.4"><p id="p82715505250"><a name="p82715505250"></a><a name="p82715505250"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="20.673469387755105%" id="mcps1.2.7.1.5"><p id="p64289158405"><a name="p64289158405"></a><a name="p64289158405"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="7.744897959183674%" id="mcps1.2.7.1.6"><p id="p59749194165124"><a name="p59749194165124"></a><a name="p59749194165124"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row114402157409"><td class="cellrowborder" valign="top" width="12.112244897959185%" headers="mcps1.2.7.1.1 "><p id="p167521433132020"><a name="p167521433132020"></a><a name="p167521433132020"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="10.234693877551022%" headers="mcps1.2.7.1.2 "><p id="p17754134012201"><a name="p17754134012201"></a><a name="p17754134012201"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="39.31632653061225%" headers="mcps1.2.7.1.3 "><p id="p1398074842019"><a name="p1398074842019"></a><a name="p1398074842019"></a>节点的ID，可以是多个。</p>
</td>
<td class="cellrowborder" valign="top" width="9.918367346938776%" headers="mcps1.2.7.1.4 "><p id="p192855017259"><a name="p192855017259"></a><a name="p192855017259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.673469387755105%" headers="mcps1.2.7.1.5 "><p id="p18347182714232"><a name="p18347182714232"></a><a name="p18347182714232"></a>source节点的个数不超过30个。</p>
</td>
<td class="cellrowborder" valign="top" width="7.744897959183674%" headers="mcps1.2.7.1.6 "><p id="p7846531165124"><a name="p7846531165124"></a><a name="p7846531165124"></a>-</p>
</td>
</tr>
<tr id="row3473115114014"><td class="cellrowborder" valign="top" width="12.112244897959185%" headers="mcps1.2.7.1.1 "><p id="p275213333204"><a name="p275213333204"></a><a name="p275213333204"></a>alpha</p>
</td>
<td class="cellrowborder" valign="top" width="10.234693877551022%" headers="mcps1.2.7.1.2 "><p id="p67544407208"><a name="p67544407208"></a><a name="p67544407208"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="39.31632653061225%" headers="mcps1.2.7.1.3 "><p id="p189801148182017"><a name="p189801148182017"></a><a name="p189801148182017"></a>权重系数，其值越大，步长越长。</p>
</td>
<td class="cellrowborder" valign="top" width="9.918367346938776%" headers="mcps1.2.7.1.4 "><p id="p228175072519"><a name="p228175072519"></a><a name="p228175072519"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="20.673469387755105%" headers="mcps1.2.7.1.5 "><p id="p19950180162417"><a name="p19950180162417"></a><a name="p19950180162417"></a>0~1，不包括0和1。</p>
</td>
<td class="cellrowborder" valign="top" width="7.744897959183674%" headers="mcps1.2.7.1.6 "><p id="p31589273165124"><a name="p31589273165124"></a><a name="p31589273165124"></a>0.85</p>
</td>
</tr>
<tr id="row10511191515401"><td class="cellrowborder" valign="top" width="12.112244897959185%" headers="mcps1.2.7.1.1 "><p id="p1375213337208"><a name="p1375213337208"></a><a name="p1375213337208"></a>N</p>
</td>
<td class="cellrowborder" valign="top" width="10.234693877551022%" headers="mcps1.2.7.1.2 "><p id="p1375484011202"><a name="p1375484011202"></a><a name="p1375484011202"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="39.31632653061225%" headers="mcps1.2.7.1.3 "><p id="p1398054852016"><a name="p1398054852016"></a><a name="p1398054852016"></a>总的游走步数。</p>
</td>
<td class="cellrowborder" valign="top" width="9.918367346938776%" headers="mcps1.2.7.1.4 "><p id="p528250182513"><a name="p528250182513"></a><a name="p528250182513"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="20.673469387755105%" headers="mcps1.2.7.1.5 "><p id="p186981016142419"><a name="p186981016142419"></a><a name="p186981016142419"></a>1~200000。</p>
</td>
<td class="cellrowborder" valign="top" width="7.744897959183674%" headers="mcps1.2.7.1.6 "><p id="p8594291165124"><a name="p8594291165124"></a><a name="p8594291165124"></a>10000</p>
</td>
</tr>
<tr id="row1754831511408"><td class="cellrowborder" valign="top" width="12.112244897959185%" headers="mcps1.2.7.1.1 "><p id="p97521333192010"><a name="p97521333192010"></a><a name="p97521333192010"></a>nv</p>
</td>
<td class="cellrowborder" valign="top" width="10.234693877551022%" headers="mcps1.2.7.1.2 "><p id="p137543409209"><a name="p137543409209"></a><a name="p137543409209"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="39.31632653061225%" headers="mcps1.2.7.1.3 "><p id="p5451359192727"><a name="p5451359192727"></a><a name="p5451359192727"></a>游走过程提前结束参数：候选推荐节点访问次数的最小值。</p>
<div class="note" id="note476272392727"><a name="note476272392727"></a><a name="note476272392727"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p4523345092742"><a name="p4523345092742"></a><a name="p4523345092742"></a>对于一个节点，如果其在随机游走过程被访问到，且被访问到的次数达到<span class="parmname" id="parmname4979810192743"><a name="parmname4979810192743"></a><a name="parmname4979810192743"></a>“nv”</span>，则该节点将记入候选推荐的节点。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="9.918367346938776%" headers="mcps1.2.7.1.4 "><p id="p132805062513"><a name="p132805062513"></a><a name="p132805062513"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="20.673469387755105%" headers="mcps1.2.7.1.5 "><p id="p11449161112417"><a name="p11449161112417"></a><a name="p11449161112417"></a>1~10。</p>
</td>
<td class="cellrowborder" valign="top" width="7.744897959183674%" headers="mcps1.2.7.1.6 "><p id="p25048953165124"><a name="p25048953165124"></a><a name="p25048953165124"></a>5</p>
</td>
</tr>
<tr id="row75871815164014"><td class="cellrowborder" valign="top" width="12.112244897959185%" headers="mcps1.2.7.1.1 "><p id="p14752103315207"><a name="p14752103315207"></a><a name="p14752103315207"></a>np</p>
</td>
<td class="cellrowborder" valign="top" width="10.234693877551022%" headers="mcps1.2.7.1.2 "><p id="p475454010208"><a name="p475454010208"></a><a name="p475454010208"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="39.31632653061225%" headers="mcps1.2.7.1.3 "><p id="p3663800292927"><a name="p3663800292927"></a><a name="p3663800292927"></a>游走过程提前结束参数：候选推荐节点个数。</p>
<div class="note" id="note3023786192927"><a name="note3023786192927"></a><a name="note3023786192927"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p370529392927"><a name="p370529392927"></a><a name="p370529392927"></a>若某个source节点的候选推荐节点达到<span class="parmname" id="parmname141088329305"><a name="parmname141088329305"></a><a name="parmname141088329305"></a>“np”</span>，对于该source节点的随机游走将提前结束。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="9.918367346938776%" headers="mcps1.2.7.1.4 "><p id="p102865072517"><a name="p102865072517"></a><a name="p102865072517"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="20.673469387755105%" headers="mcps1.2.7.1.5 "><p id="p744711192420"><a name="p744711192420"></a><a name="p744711192420"></a>1~2000。</p>
</td>
<td class="cellrowborder" valign="top" width="7.744897959183674%" headers="mcps1.2.7.1.6 "><p id="p15699349165124"><a name="p15699349165124"></a><a name="p15699349165124"></a>1000</p>
</td>
</tr>
<tr id="row16300158401"><td class="cellrowborder" valign="top" width="12.112244897959185%" headers="mcps1.2.7.1.1 "><p id="p17524336203"><a name="p17524336203"></a><a name="p17524336203"></a>label</p>
</td>
<td class="cellrowborder" valign="top" width="10.234693877551022%" headers="mcps1.2.7.1.2 "><p id="p8754144092019"><a name="p8754144092019"></a><a name="p8754144092019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="39.31632653061225%" headers="mcps1.2.7.1.3 "><p id="p516332493115"><a name="p516332493115"></a><a name="p516332493115"></a>希望输出的点的类型。</p>
<div class="note" id="note2265199293115"><a name="note2265199293115"></a><a name="note2265199293115"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul937663693135"></a><a name="ul937663693135"></a><ul id="ul937663693135"><li>其值为空时，将不考虑点的类型，输出算法原始计算结果。</li><li>对其赋值时，将从计算结果中过滤出具有该<span class="parmname" id="parmname619317093342"><a name="parmname619317093342"></a><a name="parmname619317093342"></a>“label”</span>的点的返回。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="9.918367346938776%" headers="mcps1.2.7.1.4 "><p id="p128250162514"><a name="p128250162514"></a><a name="p128250162514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.673469387755105%" headers="mcps1.2.7.1.5 "><p id="p12444161113248"><a name="p12444161113248"></a><a name="p12444161113248"></a>节点label。</p>
</td>
<td class="cellrowborder" valign="top" width="7.744897959183674%" headers="mcps1.2.7.1.6 "><p id="p63687724165124"><a name="p63687724165124"></a><a name="p63687724165124"></a>-</p>
</td>
</tr>
<tr id="row946422422018"><td class="cellrowborder" valign="top" width="12.112244897959185%" headers="mcps1.2.7.1.1 "><p id="p1752133382015"><a name="p1752133382015"></a><a name="p1752133382015"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="10.234693877551022%" headers="mcps1.2.7.1.2 "><p id="p2754104032013"><a name="p2754104032013"></a><a name="p2754104032013"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="39.31632653061225%" headers="mcps1.2.7.1.3 "><p id="p998110487206"><a name="p998110487206"></a><a name="p998110487206"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="9.918367346938776%" headers="mcps1.2.7.1.4 "><p id="p728050152518"><a name="p728050152518"></a><a name="p728050152518"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="20.673469387755105%" headers="mcps1.2.7.1.5 "><p id="p1944117118247"><a name="p1944117118247"></a><a name="p1944117118247"></a>true 或false。</p>
</td>
<td class="cellrowborder" valign="top" width="7.744897959183674%" headers="mcps1.2.7.1.6 "><p id="p58432040165124"><a name="p58432040165124"></a><a name="p58432040165124"></a>true</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table13711039184819"></a>
<table><thead align="left"><tr id="row157193974815"><th class="cellrowborder" valign="top" width="10.99%" id="mcps1.2.4.1.1"><p id="p9717397488"><a name="p9717397488"></a><a name="p9717397488"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.25%" id="mcps1.2.4.1.2"><p id="p19628563162"><a name="p19628563162"></a><a name="p19628563162"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="77.75999999999999%" id="mcps1.2.4.1.3"><p id="p177114391489"><a name="p177114391489"></a><a name="p177114391489"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row3766194912159"><td class="cellrowborder" valign="top" width="10.99%" headers="mcps1.2.4.1.1 "><p id="p676613495153"><a name="p676613495153"></a><a name="p676613495153"></a>score</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.4.1.2 "><p id="p17628166166"><a name="p17628166166"></a><a name="p17628166166"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="77.75999999999999%" headers="mcps1.2.4.1.3 "><p id="p676694915157"><a name="p676694915157"></a><a name="p676694915157"></a>各节点的得分，反应推荐程度，值越大推荐度越高，格式：</p>
<p id="p42414661812"><a name="p42414661812"></a><a name="p42414661812"></a>[{vertexId：scoreValue},...]</p>
<p id="p6913204711812"><a name="p6913204711812"></a><a name="p6913204711812"></a>其中，</p>
<p id="p204758562189"><a name="p204758562189"></a><a name="p204758562189"></a>vertexId: string类型</p>
<p id="p2461511101913"><a name="p2461511101913"></a><a name="p2461511101913"></a>scoreValue: double类型</p>
</td>
</tr>
<tr id="row15711739134811"><td class="cellrowborder" valign="top" width="10.99%" headers="mcps1.2.4.1.1 "><p id="p1711339114812"><a name="p1711339114812"></a><a name="p1711339114812"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.4.1.2 "><p id="p5628196151611"><a name="p5628196151611"></a><a name="p5628196151611"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="77.75999999999999%" headers="mcps1.2.4.1.3 "><p id="p1371113917485"><a name="p1371113917485"></a><a name="p1371113917485"></a>起始节点的ID。</p>
</td>
</tr>
</tbody>
</table>

