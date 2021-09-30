# GES系统策略<a name="ges_01_0101"></a>

**表 1**  GES系统策略

<a name="zh-cn_topic_0170103498_table89811732529"></a>
<table><thead align="left"><tr id="zh-cn_topic_0170103498_row20673339217"><th class="cellrowborder" valign="top" width="16.88%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0170103498_p18673331822"><a name="zh-cn_topic_0170103498_p18673331822"></a><a name="zh-cn_topic_0170103498_p18673331822"></a>策略名称</p>
</th>
<th class="cellrowborder" valign="top" width="83.12%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0170103498_p3671933625"><a name="zh-cn_topic_0170103498_p3671933625"></a><a name="zh-cn_topic_0170103498_p3671933625"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0170103498_row067933821"><td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0170103498_p126719339214"><a name="zh-cn_topic_0170103498_p126719339214"></a><a name="zh-cn_topic_0170103498_p126719339214"></a>GES&nbsp;FullAccess</p>
</td>
<td class="cellrowborder" valign="top" width="83.12%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0170103498_p56743318218"><a name="zh-cn_topic_0170103498_p56743318218"></a><a name="zh-cn_topic_0170103498_p56743318218"></a>图引擎服务管理员权限，拥有该权限的用户拥有图引擎服务的全部权限，包括创建、删除、访问、升级等操作。</p>
<div class="note" id="note854115394017"><a name="note854115394017"></a><a name="note854115394017"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul521418553407"></a><a name="ul521418553407"></a><ul id="ul521418553407"><li>拥有该权限的用户需要同时拥有Tenant Guest、Server Administrator、VPC Administrator权限。</li><li>如果需要绑定/解绑EIP，则还需要拥有Security Administrator角色用于创建委托。Security Administrator角色权限较大，可以使用如下自定义策略替代："iam:agencies:listAgencies","iam:permissions:listRolesForAgency","iam:permissions:listRolesForAgencyOnProject","iam:permissions:listRolesForAgencyOnDomain"</li><li>资源操作依赖OBS，需要拥有OBS OperateAccess策略。（OBS是全局服务，对应的OBS策略需要在全局服务下查找）。</li></ul>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row9679330211"><td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0170103498_p14674331626"><a name="zh-cn_topic_0170103498_p14674331626"></a><a name="zh-cn_topic_0170103498_p14674331626"></a>GES&nbsp;Development</p>
</td>
<td class="cellrowborder" valign="top" width="83.12%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0170103498_p1367153310212"><a name="zh-cn_topic_0170103498_p1367153310212"></a><a name="zh-cn_topic_0170103498_p1367153310212"></a>图引擎服务使用权限，拥有该权限的用户可以执行除了创建图、删除图以外所有操作。</p>
<div class="note" id="zh-cn_topic_0170103498_note162631031695"><a name="zh-cn_topic_0170103498_note162631031695"></a><a name="zh-cn_topic_0170103498_note162631031695"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0170103498_ul3520140102212"></a><a name="zh-cn_topic_0170103498_ul3520140102212"></a><ul id="zh-cn_topic_0170103498_ul3520140102212"><li>如果需要绑定/解绑EIP，则还需要拥有Security Administrator角色用于创建委托。Security Administrator角色还可以使用自定义策略替代，自定义策略包含："iam:agencies:listAgencies","iam:permissions:listRolesForAgency","iam:permissions:listRolesForAgencyOnProject","iam:permissions:listRolesForAgencyOnDomain"</li><li>资源操作依赖OBS，需要拥有OBS OperateAccess策略。（OBS是全局服务，对应的OBS策略需要在全局服务下查找）。</li></ul>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row5671633026"><td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0170103498_p8676331527"><a name="zh-cn_topic_0170103498_p8676331527"></a><a name="zh-cn_topic_0170103498_p8676331527"></a>GES&nbsp;ReadOnlyAccess</p>
</td>
<td class="cellrowborder" valign="top" width="83.12%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0170103498_p16712339211"><a name="zh-cn_topic_0170103498_p16712339211"></a><a name="zh-cn_topic_0170103498_p16712339211"></a>图引擎服务资源只读权限，拥有该权限的用户只能做一些资源查看类的操作如查看图列表、查看元数据和查看备份等。</p>
<div class="note" id="zh-cn_topic_0170103498_note550211118917"><a name="zh-cn_topic_0170103498_note550211118917"></a><a name="zh-cn_topic_0170103498_note550211118917"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p16319042192511"><a name="p16319042192511"></a><a name="p16319042192511"></a>资源操作依赖OBS，需要拥有OBS OperateAccess策略。（OBS是全局服务，对应的OBS策略需要在全局服务下查找）</p>
</div></div>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>由于缓存的存在，对用户和用户组授予OBS相关的角色后，大概需要等待13分钟角色才能生效；授予策略后，大概需要等待5分钟策略才能生效。

**表 2**  GES常用操作与系统策略的关系

<a name="zh-cn_topic_0170103498_table06491545446"></a>
<table><thead align="left"><tr id="zh-cn_topic_0170103498_row22015461048"><th class="cellrowborder" valign="top" width="23.977602239776026%" id="mcps1.2.6.1.1"><p id="zh-cn_topic_0170103498_p152015461246"><a name="zh-cn_topic_0170103498_p152015461246"></a><a name="zh-cn_topic_0170103498_p152015461246"></a>操作</p>
</th>
<th class="cellrowborder" valign="top" width="17.578242175782425%" id="mcps1.2.6.1.2"><p id="zh-cn_topic_0170103498_p1020116461641"><a name="zh-cn_topic_0170103498_p1020116461641"></a><a name="zh-cn_topic_0170103498_p1020116461641"></a>GES&nbsp;FullAccess</p>
</th>
<th class="cellrowborder" valign="top" width="19.908009199080094%" id="mcps1.2.6.1.3"><p id="zh-cn_topic_0170103498_p32011646546"><a name="zh-cn_topic_0170103498_p32011646546"></a><a name="zh-cn_topic_0170103498_p32011646546"></a>GES&nbsp;Development</p>
</th>
<th class="cellrowborder" valign="top" width="19.668033196680334%" id="mcps1.2.6.1.4"><p id="zh-cn_topic_0170103498_p220111460418"><a name="zh-cn_topic_0170103498_p220111460418"></a><a name="zh-cn_topic_0170103498_p220111460418"></a>GES&nbsp;ReadOnlyAccess</p>
</th>
<th class="cellrowborder" valign="top" width="18.868113188681132%" id="mcps1.2.6.1.5"><p id="zh-cn_topic_0170103498_p1259892818417"><a name="zh-cn_topic_0170103498_p1259892818417"></a><a name="zh-cn_topic_0170103498_p1259892818417"></a>对应资源</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0170103498_row1420112461642"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p5201546648"><a name="zh-cn_topic_0170103498_p5201546648"></a><a name="zh-cn_topic_0170103498_p5201546648"></a>查询图列表</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p1420119463417"><a name="zh-cn_topic_0170103498_p1420119463417"></a><a name="zh-cn_topic_0170103498_p1420119463417"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p22019461641"><a name="zh-cn_topic_0170103498_p22019461641"></a><a name="zh-cn_topic_0170103498_p22019461641"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1320114618415"><a name="zh-cn_topic_0170103498_p1320114618415"></a><a name="zh-cn_topic_0170103498_p1320114618415"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p7599528134117"><a name="zh-cn_topic_0170103498_p7599528134117"></a><a name="zh-cn_topic_0170103498_p7599528134117"></a>-</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row620113461749"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p420274618415"><a name="zh-cn_topic_0170103498_p420274618415"></a><a name="zh-cn_topic_0170103498_p420274618415"></a>查看图详情</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p12021846040"><a name="zh-cn_topic_0170103498_p12021846040"></a><a name="zh-cn_topic_0170103498_p12021846040"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p122029466415"><a name="zh-cn_topic_0170103498_p122029466415"></a><a name="zh-cn_topic_0170103498_p122029466415"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1020216462413"><a name="zh-cn_topic_0170103498_p1020216462413"></a><a name="zh-cn_topic_0170103498_p1020216462413"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p059932834113"><a name="zh-cn_topic_0170103498_p059932834113"></a><a name="zh-cn_topic_0170103498_p059932834113"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row10202124610411"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p72029461546"><a name="zh-cn_topic_0170103498_p72029461546"></a><a name="zh-cn_topic_0170103498_p72029461546"></a>创建图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p14202144620411"><a name="zh-cn_topic_0170103498_p14202144620411"></a><a name="zh-cn_topic_0170103498_p14202144620411"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p02027462417"><a name="zh-cn_topic_0170103498_p02027462417"></a><a name="zh-cn_topic_0170103498_p02027462417"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p9202164615416"><a name="zh-cn_topic_0170103498_p9202164615416"></a><a name="zh-cn_topic_0170103498_p9202164615416"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1359992844114"><a name="zh-cn_topic_0170103498_p1359992844114"></a><a name="zh-cn_topic_0170103498_p1359992844114"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row17836101064512"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p13836141018451"><a name="zh-cn_topic_0170103498_p13836141018451"></a><a name="zh-cn_topic_0170103498_p13836141018451"></a>访问图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p586515718468"><a name="zh-cn_topic_0170103498_p586515718468"></a><a name="zh-cn_topic_0170103498_p586515718468"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p17865474462"><a name="zh-cn_topic_0170103498_p17865474462"></a><a name="zh-cn_topic_0170103498_p17865474462"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p186511724619"><a name="zh-cn_topic_0170103498_p186511724619"></a><a name="zh-cn_topic_0170103498_p186511724619"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p18837410154515"><a name="zh-cn_topic_0170103498_p18837410154515"></a><a name="zh-cn_topic_0170103498_p18837410154515"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row10202174610413"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p182021546541"><a name="zh-cn_topic_0170103498_p182021546541"></a><a name="zh-cn_topic_0170103498_p182021546541"></a>关闭图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p13202246446"><a name="zh-cn_topic_0170103498_p13202246446"></a><a name="zh-cn_topic_0170103498_p13202246446"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p19202154613418"><a name="zh-cn_topic_0170103498_p19202154613418"></a><a name="zh-cn_topic_0170103498_p19202154613418"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p202034461741"><a name="zh-cn_topic_0170103498_p202034461741"></a><a name="zh-cn_topic_0170103498_p202034461741"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p15599162816417"><a name="zh-cn_topic_0170103498_p15599162816417"></a><a name="zh-cn_topic_0170103498_p15599162816417"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row62036465412"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p152033462047"><a name="zh-cn_topic_0170103498_p152033462047"></a><a name="zh-cn_topic_0170103498_p152033462047"></a>启动图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p1720313468414"><a name="zh-cn_topic_0170103498_p1720313468414"></a><a name="zh-cn_topic_0170103498_p1720313468414"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p0203846749"><a name="zh-cn_topic_0170103498_p0203846749"></a><a name="zh-cn_topic_0170103498_p0203846749"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1920316466411"><a name="zh-cn_topic_0170103498_p1920316466411"></a><a name="zh-cn_topic_0170103498_p1920316466411"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p115991128194112"><a name="zh-cn_topic_0170103498_p115991128194112"></a><a name="zh-cn_topic_0170103498_p115991128194112"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row520315461040"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p720311463412"><a name="zh-cn_topic_0170103498_p720311463412"></a><a name="zh-cn_topic_0170103498_p720311463412"></a>删除图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p42039461845"><a name="zh-cn_topic_0170103498_p42039461845"></a><a name="zh-cn_topic_0170103498_p42039461845"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p120313465416"><a name="zh-cn_topic_0170103498_p120313465416"></a><a name="zh-cn_topic_0170103498_p120313465416"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p82036467418"><a name="zh-cn_topic_0170103498_p82036467418"></a><a name="zh-cn_topic_0170103498_p82036467418"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p125991828124115"><a name="zh-cn_topic_0170103498_p125991828124115"></a><a name="zh-cn_topic_0170103498_p125991828124115"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row10203144614411"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p62031246444"><a name="zh-cn_topic_0170103498_p62031246444"></a><a name="zh-cn_topic_0170103498_p62031246444"></a>增量导入图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p16204346442"><a name="zh-cn_topic_0170103498_p16204346442"></a><a name="zh-cn_topic_0170103498_p16204346442"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p142041046445"><a name="zh-cn_topic_0170103498_p142041046445"></a><a name="zh-cn_topic_0170103498_p142041046445"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p182042467411"><a name="zh-cn_topic_0170103498_p182042467411"></a><a name="zh-cn_topic_0170103498_p182042467411"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p0599182844119"><a name="zh-cn_topic_0170103498_p0599182844119"></a><a name="zh-cn_topic_0170103498_p0599182844119"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row17204114618413"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p620420462041"><a name="zh-cn_topic_0170103498_p620420462041"></a><a name="zh-cn_topic_0170103498_p620420462041"></a>导出图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p12204646544"><a name="zh-cn_topic_0170103498_p12204646544"></a><a name="zh-cn_topic_0170103498_p12204646544"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p1220464615410"><a name="zh-cn_topic_0170103498_p1220464615410"></a><a name="zh-cn_topic_0170103498_p1220464615410"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p10204246841"><a name="zh-cn_topic_0170103498_p10204246841"></a><a name="zh-cn_topic_0170103498_p10204246841"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p105999282413"><a name="zh-cn_topic_0170103498_p105999282413"></a><a name="zh-cn_topic_0170103498_p105999282413"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row320417465412"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p112042046842"><a name="zh-cn_topic_0170103498_p112042046842"></a><a name="zh-cn_topic_0170103498_p112042046842"></a>清空图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p102041046147"><a name="zh-cn_topic_0170103498_p102041046147"></a><a name="zh-cn_topic_0170103498_p102041046147"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p620415463420"><a name="zh-cn_topic_0170103498_p620415463420"></a><a name="zh-cn_topic_0170103498_p620415463420"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p52054466414"><a name="zh-cn_topic_0170103498_p52054466414"></a><a name="zh-cn_topic_0170103498_p52054466414"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p8599142824119"><a name="zh-cn_topic_0170103498_p8599142824119"></a><a name="zh-cn_topic_0170103498_p8599142824119"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row420519469413"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p3205134616415"><a name="zh-cn_topic_0170103498_p3205134616415"></a><a name="zh-cn_topic_0170103498_p3205134616415"></a>升级图</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p2205134618415"><a name="zh-cn_topic_0170103498_p2205134618415"></a><a name="zh-cn_topic_0170103498_p2205134618415"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p152056467420"><a name="zh-cn_topic_0170103498_p152056467420"></a><a name="zh-cn_topic_0170103498_p152056467420"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p12057464415"><a name="zh-cn_topic_0170103498_p12057464415"></a><a name="zh-cn_topic_0170103498_p12057464415"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1159952810414"><a name="zh-cn_topic_0170103498_p1159952810414"></a><a name="zh-cn_topic_0170103498_p1159952810414"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row11205946645"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p420520467420"><a name="zh-cn_topic_0170103498_p420520467420"></a><a name="zh-cn_topic_0170103498_p420520467420"></a>绑定EIP</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p420518461147"><a name="zh-cn_topic_0170103498_p420518461147"></a><a name="zh-cn_topic_0170103498_p420518461147"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p4205124613419"><a name="zh-cn_topic_0170103498_p4205124613419"></a><a name="zh-cn_topic_0170103498_p4205124613419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p82058465420"><a name="zh-cn_topic_0170103498_p82058465420"></a><a name="zh-cn_topic_0170103498_p82058465420"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p3426182420411"><a name="zh-cn_topic_0170103498_p3426182420411"></a><a name="zh-cn_topic_0170103498_p3426182420411"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row72051846743"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p420619468414"><a name="zh-cn_topic_0170103498_p420619468414"></a><a name="zh-cn_topic_0170103498_p420619468414"></a>解绑EIP</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p10206174611412"><a name="zh-cn_topic_0170103498_p10206174611412"></a><a name="zh-cn_topic_0170103498_p10206174611412"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p14206174615419"><a name="zh-cn_topic_0170103498_p14206174615419"></a><a name="zh-cn_topic_0170103498_p14206174615419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1220619461049"><a name="zh-cn_topic_0170103498_p1220619461049"></a><a name="zh-cn_topic_0170103498_p1220619461049"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p528092718412"><a name="zh-cn_topic_0170103498_p528092718412"></a><a name="zh-cn_topic_0170103498_p528092718412"></a>graphName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row42065461741"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p1620615468419"><a name="zh-cn_topic_0170103498_p1620615468419"></a><a name="zh-cn_topic_0170103498_p1620615468419"></a>查看所有备份列表</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p72062468414"><a name="zh-cn_topic_0170103498_p72062468414"></a><a name="zh-cn_topic_0170103498_p72062468414"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p192068461349"><a name="zh-cn_topic_0170103498_p192068461349"></a><a name="zh-cn_topic_0170103498_p192068461349"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1920620462410"><a name="zh-cn_topic_0170103498_p1920620462410"></a><a name="zh-cn_topic_0170103498_p1920620462410"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p7600102854111"><a name="zh-cn_topic_0170103498_p7600102854111"></a><a name="zh-cn_topic_0170103498_p7600102854111"></a>-</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row14206546344"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p2020617466410"><a name="zh-cn_topic_0170103498_p2020617466410"></a><a name="zh-cn_topic_0170103498_p2020617466410"></a>查看某个图的备份列表</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p42061462411"><a name="zh-cn_topic_0170103498_p42061462411"></a><a name="zh-cn_topic_0170103498_p42061462411"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p9206146342"><a name="zh-cn_topic_0170103498_p9206146342"></a><a name="zh-cn_topic_0170103498_p9206146342"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p0206154614413"><a name="zh-cn_topic_0170103498_p0206154614413"></a><a name="zh-cn_topic_0170103498_p0206154614413"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p126005287417"><a name="zh-cn_topic_0170103498_p126005287417"></a><a name="zh-cn_topic_0170103498_p126005287417"></a>-</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row3206146149"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p192074462414"><a name="zh-cn_topic_0170103498_p192074462414"></a><a name="zh-cn_topic_0170103498_p192074462414"></a>新增备份</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p920711461648"><a name="zh-cn_topic_0170103498_p920711461648"></a><a name="zh-cn_topic_0170103498_p920711461648"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p14207114612416"><a name="zh-cn_topic_0170103498_p14207114612416"></a><a name="zh-cn_topic_0170103498_p14207114612416"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p122071546449"><a name="zh-cn_topic_0170103498_p122071546449"></a><a name="zh-cn_topic_0170103498_p122071546449"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p960022819418"><a name="zh-cn_topic_0170103498_p960022819418"></a><a name="zh-cn_topic_0170103498_p960022819418"></a>backupName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row182078461343"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p18207346849"><a name="zh-cn_topic_0170103498_p18207346849"></a><a name="zh-cn_topic_0170103498_p18207346849"></a>删除备份</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p920717461643"><a name="zh-cn_topic_0170103498_p920717461643"></a><a name="zh-cn_topic_0170103498_p920717461643"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p132079461245"><a name="zh-cn_topic_0170103498_p132079461245"></a><a name="zh-cn_topic_0170103498_p132079461245"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p16207144617413"><a name="zh-cn_topic_0170103498_p16207144617413"></a><a name="zh-cn_topic_0170103498_p16207144617413"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p3600172816416"><a name="zh-cn_topic_0170103498_p3600172816416"></a><a name="zh-cn_topic_0170103498_p3600172816416"></a>backupName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row1207946448"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p52076467413"><a name="zh-cn_topic_0170103498_p52076467413"></a><a name="zh-cn_topic_0170103498_p52076467413"></a>查询元数据列表</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p42071246142"><a name="zh-cn_topic_0170103498_p42071246142"></a><a name="zh-cn_topic_0170103498_p42071246142"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p14207154611413"><a name="zh-cn_topic_0170103498_p14207154611413"></a><a name="zh-cn_topic_0170103498_p14207154611413"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p6207144615412"><a name="zh-cn_topic_0170103498_p6207144615412"></a><a name="zh-cn_topic_0170103498_p6207144615412"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p360013289412"><a name="zh-cn_topic_0170103498_p360013289412"></a><a name="zh-cn_topic_0170103498_p360013289412"></a>-</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row2020794615412"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p32071046947"><a name="zh-cn_topic_0170103498_p32071046947"></a><a name="zh-cn_topic_0170103498_p32071046947"></a>查询元数据</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p1020704611410"><a name="zh-cn_topic_0170103498_p1020704611410"></a><a name="zh-cn_topic_0170103498_p1020704611410"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p182076461341"><a name="zh-cn_topic_0170103498_p182076461341"></a><a name="zh-cn_topic_0170103498_p182076461341"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p112084469412"><a name="zh-cn_topic_0170103498_p112084469412"></a><a name="zh-cn_topic_0170103498_p112084469412"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p11600102824119"><a name="zh-cn_topic_0170103498_p11600102824119"></a><a name="zh-cn_topic_0170103498_p11600102824119"></a>metadataName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row220814614413"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p1420817462419"><a name="zh-cn_topic_0170103498_p1420817462419"></a><a name="zh-cn_topic_0170103498_p1420817462419"></a>校验元数据</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p172084467416"><a name="zh-cn_topic_0170103498_p172084467416"></a><a name="zh-cn_topic_0170103498_p172084467416"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p920813463413"><a name="zh-cn_topic_0170103498_p920813463413"></a><a name="zh-cn_topic_0170103498_p920813463413"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1820811461243"><a name="zh-cn_topic_0170103498_p1820811461243"></a><a name="zh-cn_topic_0170103498_p1820811461243"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1660019282413"><a name="zh-cn_topic_0170103498_p1660019282413"></a><a name="zh-cn_topic_0170103498_p1660019282413"></a>-</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row5208246648"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p92084461145"><a name="zh-cn_topic_0170103498_p92084461145"></a><a name="zh-cn_topic_0170103498_p92084461145"></a>新增元数据</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p7208174613419"><a name="zh-cn_topic_0170103498_p7208174613419"></a><a name="zh-cn_topic_0170103498_p7208174613419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p1320815467419"><a name="zh-cn_topic_0170103498_p1320815467419"></a><a name="zh-cn_topic_0170103498_p1320815467419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p220814469420"><a name="zh-cn_topic_0170103498_p220814469420"></a><a name="zh-cn_topic_0170103498_p220814469420"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1460012289413"><a name="zh-cn_topic_0170103498_p1460012289413"></a><a name="zh-cn_topic_0170103498_p1460012289413"></a>metadataName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row72089467419"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p1920816467412"><a name="zh-cn_topic_0170103498_p1920816467412"></a><a name="zh-cn_topic_0170103498_p1920816467412"></a>删除元数据</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p52081446342"><a name="zh-cn_topic_0170103498_p52081446342"></a><a name="zh-cn_topic_0170103498_p52081446342"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p17208346844"><a name="zh-cn_topic_0170103498_p17208346844"></a><a name="zh-cn_topic_0170103498_p17208346844"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1920819461747"><a name="zh-cn_topic_0170103498_p1920819461747"></a><a name="zh-cn_topic_0170103498_p1920819461747"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1660032814416"><a name="zh-cn_topic_0170103498_p1660032814416"></a><a name="zh-cn_topic_0170103498_p1660032814416"></a>metadataName</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row520814461741"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p12208144618413"><a name="zh-cn_topic_0170103498_p12208144618413"></a><a name="zh-cn_topic_0170103498_p12208144618413"></a>查询任务状态</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p1520918464420"><a name="zh-cn_topic_0170103498_p1520918464420"></a><a name="zh-cn_topic_0170103498_p1520918464420"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p020914461848"><a name="zh-cn_topic_0170103498_p020914461848"></a><a name="zh-cn_topic_0170103498_p020914461848"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p3209134619414"><a name="zh-cn_topic_0170103498_p3209134619414"></a><a name="zh-cn_topic_0170103498_p3209134619414"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p56005288419"><a name="zh-cn_topic_0170103498_p56005288419"></a><a name="zh-cn_topic_0170103498_p56005288419"></a>-</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row112093461418"><td class="cellrowborder" valign="top" width="23.977602239776026%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p1320915461547"><a name="zh-cn_topic_0170103498_p1320915461547"></a><a name="zh-cn_topic_0170103498_p1320915461547"></a>查询任务列表</p>
</td>
<td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p4209746946"><a name="zh-cn_topic_0170103498_p4209746946"></a><a name="zh-cn_topic_0170103498_p4209746946"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.908009199080094%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p1920914461543"><a name="zh-cn_topic_0170103498_p1920914461543"></a><a name="zh-cn_topic_0170103498_p1920914461543"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="19.668033196680334%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1320924619418"><a name="zh-cn_topic_0170103498_p1320924619418"></a><a name="zh-cn_topic_0170103498_p1320924619418"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p76001828124119"><a name="zh-cn_topic_0170103498_p76001828124119"></a><a name="zh-cn_topic_0170103498_p76001828124119"></a>-</p>
</td>
</tr>
</tbody>
</table>

