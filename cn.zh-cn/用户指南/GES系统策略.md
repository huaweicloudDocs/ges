# GES系统策略<a name="ges_01_0073"></a>

## GES系统策略<a name="section8992185412471"></a>

策略是以JSON格式描述的权限集。默认情况下，新建的IAM用户没有任何权限，您需要将其加入用户组，并给用户组授予策略，才能使得该用户组中的用户获得对应策略定义的权限，这一过程称为授权。授权后，用户就可以基于策略对云服务进行操作。IAM系统预置了各服务的常用权限，例如管理员权限、只读权限等，您可以直接使用这些系统策略。

GES部署时通过物理区域划分，为项目级服务，需要在各区域（如华北-北京1）对应的项目（cn-north-1）中设置策略，并且该策略仅对此项目生效，如果需要所有区域都生效，则需要在所有项目都设置策略。访问GES时，需要先切换至授权区域。

-   策略类别：

    策略根据授权精度分为细粒度策略和Role-Based Access Control（RBAC）策略。细粒度策略是RBAC策略的升级版，当前处于公测阶段，推荐您开通细粒度策略，开通后可免费使用，开通方法请参见：[申请细粒度访问控制公测](https://support.huaweicloud.com/usermanual-iam/iam_01_019.html)。

    -   RBAC策略：RBAC策略是将服务作为一个整体进行授权，授权后，用户可以拥有这个服务的所有权限，如访问整个服务、管理整个服务，RBAC策略无法针对服务中的具体操作做权限控制。
    -   细粒度策略：细粒度策略以API接口为粒度进行权限拆分，授权更加精细，可以精确到具体操作。授权后，用户可以对这个服务执行特定的操作，例如不允许某用户组删除图，仅允许对GES资源进行查看操作， GES支持的API授权项请参见《[权限策略和授权项](https://support.huaweicloud.com/api-ges/ges_03_0148.html)》_。_


-   依赖关系：华为云各服务之间存在业务交互关系，因此给用户授予GES的权限时，需要同时授予所依赖的其他云服务的权限，GES的权限才能生效。具体请参考[表1](#zh-cn_topic_0170103498_table79341548182420)和[表2](#zh-cn_topic_0170103498_table89811732529)。

>![](public_sys-resources/icon-note.gif) **说明：**   
>由于缓存的存在，对用户和用户组授予OBS相关的RBAC策略后，大概需要等待13分钟RBAC策略才能生效；授予细粒度策略后，大概需要等待5分钟细粒度策略才能生效。  

**表 1**  GES RBAC策略

<a name="zh-cn_topic_0170103498_table79341548182420"></a>
<table><thead align="left"><tr id="zh-cn_topic_0170103498_row1916124942412"><th class="cellrowborder" valign="top" width="23.057694230576942%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0170103498_p1616154914249"><a name="zh-cn_topic_0170103498_p1616154914249"></a><a name="zh-cn_topic_0170103498_p1616154914249"></a>策略名称</p>
</th>
<th class="cellrowborder" valign="top" width="62.67373262673733%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0170103498_p616194952410"><a name="zh-cn_topic_0170103498_p616194952410"></a><a name="zh-cn_topic_0170103498_p616194952410"></a>描述</p>
</th>
<th class="cellrowborder" valign="top" width="14.268573142685732%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0170103498_p116204916243"><a name="zh-cn_topic_0170103498_p116204916243"></a><a name="zh-cn_topic_0170103498_p116204916243"></a>策略类别</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0170103498_row422521642814"><td class="cellrowborder" valign="top" width="23.057694230576942%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0170103498_p9227181632817"><a name="zh-cn_topic_0170103498_p9227181632817"></a><a name="zh-cn_topic_0170103498_p9227181632817"></a>Tenant Guest</p>
</td>
<td class="cellrowborder" valign="top" width="62.67373262673733%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0170103498_p52271616172811"><a name="zh-cn_topic_0170103498_p52271616172811"></a><a name="zh-cn_topic_0170103498_p52271616172811"></a>普通租户用户。</p>
<a name="zh-cn_topic_0170103498_ul5954175802819"></a><a name="zh-cn_topic_0170103498_ul5954175802819"></a><ul id="zh-cn_topic_0170103498_ul5954175802819"><li>操作权限：可以对GES资源执行查看操作。</li><li>作用范围：项目级服务。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.268573142685732%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0170103498_p422831612819"><a name="zh-cn_topic_0170103498_p422831612819"></a><a name="zh-cn_topic_0170103498_p422831612819"></a>RBAC</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row1917749132415"><td class="cellrowborder" valign="top" width="23.057694230576942%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0170103498_p48121412121718"><a name="zh-cn_topic_0170103498_p48121412121718"></a><a name="zh-cn_topic_0170103498_p48121412121718"></a>GES Administrator</p>
</td>
<td class="cellrowborder" valign="top" width="62.67373262673733%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0170103498_p49787271109"><a name="zh-cn_topic_0170103498_p49787271109"></a><a name="zh-cn_topic_0170103498_p49787271109"></a>GES服务管理员。</p>
<a name="zh-cn_topic_0170103498_ul973112019319"></a><a name="zh-cn_topic_0170103498_ul973112019319"></a><ul id="zh-cn_topic_0170103498_ul973112019319"><li>操作权限：可以对GES资源执行任意操作。</li><li>作用范围：项目级服务。</li></ul>
<div class="note" id="zh-cn_topic_0170103498_note1845915414618"><a name="zh-cn_topic_0170103498_note1845915414618"></a><a name="zh-cn_topic_0170103498_note1845915414618"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0170103498_p1569122021915"><a name="zh-cn_topic_0170103498_p1569122021915"></a><a name="zh-cn_topic_0170103498_p1569122021915"></a>拥有该权限的用户同时拥有Tenant Guest和Server Administrator权限时，可以对GES资源执行任意操作。如果没有Tenant Guest或Server Administrator权限，将无法正常使用GES。</p>
<a name="zh-cn_topic_0170103498_ul183945814185"></a><a name="zh-cn_topic_0170103498_ul183945814185"></a><ul id="zh-cn_topic_0170103498_ul183945814185"><li>如果需要绑定/解绑EIP，则还需要拥有Security Administrator权限用于创建委托。</li><li>如果需要与OBS服务进行交互，例如创建，导入等操作，则还需要拥有OBS服务的权限，具体请参考<a href="#zh-cn_topic_0170103498_table2730121404">表5</a>。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="14.268573142685732%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0170103498_p25788714590"><a name="zh-cn_topic_0170103498_p25788714590"></a><a name="zh-cn_topic_0170103498_p25788714590"></a>RBAC</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row63952155556"><td class="cellrowborder" valign="top" width="23.057694230576942%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0170103498_p75581679415"><a name="zh-cn_topic_0170103498_p75581679415"></a><a name="zh-cn_topic_0170103498_p75581679415"></a>GES Manager</p>
</td>
<td class="cellrowborder" valign="top" width="62.67373262673733%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0170103498_p8451153816018"><a name="zh-cn_topic_0170103498_p8451153816018"></a><a name="zh-cn_topic_0170103498_p8451153816018"></a>GES服务高级用户。</p>
<a name="zh-cn_topic_0170103498_ul127290323"></a><a name="zh-cn_topic_0170103498_ul127290323"></a><ul id="zh-cn_topic_0170103498_ul127290323"><li>操作权限：可以对GES资源执行除创建图和删除图以外的任意操作。</li><li>作用范围：项目级服务。</li></ul>
<div class="note" id="zh-cn_topic_0170103498_note102491254473"><a name="zh-cn_topic_0170103498_note102491254473"></a><a name="zh-cn_topic_0170103498_note102491254473"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0170103498_p699511335455"><a name="zh-cn_topic_0170103498_p699511335455"></a><a name="zh-cn_topic_0170103498_p699511335455"></a>拥有该权限的用户同时拥有Tenant Guest权限时，可以对GES资源执行除创建图和删除图以外的任意操作。如果没有Tenant Guest权限，将无法正常使用GES。</p>
<a name="zh-cn_topic_0170103498_ul121461135192211"></a><a name="zh-cn_topic_0170103498_ul121461135192211"></a><ul id="zh-cn_topic_0170103498_ul121461135192211"><li>如果需要绑定/解绑EIP，则还需要拥有Security Administrator和Server Administrator权限。</li><li>如果需要与OBS服务进行交互，例如导入操作，则还需要拥有OBS服务的权限，具体请参考<a href="#zh-cn_topic_0170103498_table2730121404">表5</a>。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="14.268573142685732%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0170103498_p589231565912"><a name="zh-cn_topic_0170103498_p589231565912"></a><a name="zh-cn_topic_0170103498_p589231565912"></a>RBAC</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row1351942132810"><td class="cellrowborder" valign="top" width="23.057694230576942%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0170103498_p088820101216"><a name="zh-cn_topic_0170103498_p088820101216"></a><a name="zh-cn_topic_0170103498_p088820101216"></a>GES Operator</p>
</td>
<td class="cellrowborder" valign="top" width="62.67373262673733%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0170103498_p143612421287"><a name="zh-cn_topic_0170103498_p143612421287"></a><a name="zh-cn_topic_0170103498_p143612421287"></a>GES服务普通用户。</p>
<a name="zh-cn_topic_0170103498_ul1849117823211"></a><a name="zh-cn_topic_0170103498_ul1849117823211"></a><ul id="zh-cn_topic_0170103498_ul1849117823211"><li>操作权限：可以对GES资源执行查看操作和访问图。</li><li>作用范围：项目级服务。</li></ul>
<div class="note" id="zh-cn_topic_0170103498_note174521214285"><a name="zh-cn_topic_0170103498_note174521214285"></a><a name="zh-cn_topic_0170103498_note174521214285"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0170103498_p04541143812"><a name="zh-cn_topic_0170103498_p04541143812"></a><a name="zh-cn_topic_0170103498_p04541143812"></a>拥有该权限的用户同时拥有Tenant Guest权限时，可以对GES资源执行查看操作和访问图。如果没有Tenant Guest，则无法执行查看类操作或者访问图。</p>
<p id="zh-cn_topic_0170103498_p1884237102911"><a name="zh-cn_topic_0170103498_p1884237102911"></a><a name="zh-cn_topic_0170103498_p1884237102911"></a>如果需要与OBS服务进行交互，例如查看元数据，则还需要拥有OBS服务的权限，具体请参考<a href="#zh-cn_topic_0170103498_table2730121404">表5</a>。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="14.268573142685732%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0170103498_p10296102412595"><a name="zh-cn_topic_0170103498_p10296102412595"></a><a name="zh-cn_topic_0170103498_p10296102412595"></a>RBAC</p>
</td>
</tr>
</tbody>
</table>

**表 2**  GES细粒度策略

<a name="zh-cn_topic_0170103498_table89811732529"></a>
<table><thead align="left"><tr id="zh-cn_topic_0170103498_row20673339217"><th class="cellrowborder" valign="top" width="13.26%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0170103498_p18673331822"><a name="zh-cn_topic_0170103498_p18673331822"></a><a name="zh-cn_topic_0170103498_p18673331822"></a>策略名称</p>
</th>
<th class="cellrowborder" valign="top" width="68.78%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0170103498_p3671933625"><a name="zh-cn_topic_0170103498_p3671933625"></a><a name="zh-cn_topic_0170103498_p3671933625"></a>描述</p>
</th>
<th class="cellrowborder" valign="top" width="17.96%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0170103498_p166718331426"><a name="zh-cn_topic_0170103498_p166718331426"></a><a name="zh-cn_topic_0170103498_p166718331426"></a>策略类别</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0170103498_row067933821"><td class="cellrowborder" valign="top" width="13.26%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0170103498_p126719339214"><a name="zh-cn_topic_0170103498_p126719339214"></a><a name="zh-cn_topic_0170103498_p126719339214"></a>GES Admin</p>
</td>
<td class="cellrowborder" valign="top" width="68.78%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0170103498_p56743318218"><a name="zh-cn_topic_0170103498_p56743318218"></a><a name="zh-cn_topic_0170103498_p56743318218"></a>图引擎服务管理员权限，拥有该权限的用户拥有图引擎服务的全部权限，包括创建、删除、访问、升级等操作。</p>
<div class="note" id="zh-cn_topic_0170103498_note108516537814"><a name="zh-cn_topic_0170103498_note108516537814"></a><a name="zh-cn_topic_0170103498_note108516537814"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0170103498_ul173871836893"></a><a name="zh-cn_topic_0170103498_ul173871836893"></a><ul id="zh-cn_topic_0170103498_ul173871836893"><li>如果需要绑定/解绑EIP，则还需要拥有Security Administrator权限用于创建委托。</li><li>如果需要与OBS服务进行交互，例如创建，导入等操作，则还需要拥有OBS服务的权限，具体请参考<a href="#zh-cn_topic_0170103498_table2730121404">表5</a>。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="17.96%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0170103498_p6671833923"><a name="zh-cn_topic_0170103498_p6671833923"></a><a name="zh-cn_topic_0170103498_p6671833923"></a>细粒度策略</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row9679330211"><td class="cellrowborder" valign="top" width="13.26%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0170103498_p14674331626"><a name="zh-cn_topic_0170103498_p14674331626"></a><a name="zh-cn_topic_0170103498_p14674331626"></a>GES User</p>
</td>
<td class="cellrowborder" valign="top" width="68.78%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0170103498_p1367153310212"><a name="zh-cn_topic_0170103498_p1367153310212"></a><a name="zh-cn_topic_0170103498_p1367153310212"></a>图引擎服务使用权限，拥有该权限的用户可以执行除了创建图、删除图以外所有操作。</p>
<div class="note" id="zh-cn_topic_0170103498_note162631031695"><a name="zh-cn_topic_0170103498_note162631031695"></a><a name="zh-cn_topic_0170103498_note162631031695"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0170103498_ul3520140102212"></a><a name="zh-cn_topic_0170103498_ul3520140102212"></a><ul id="zh-cn_topic_0170103498_ul3520140102212"><li>如果需要绑定/解绑EIP，则还需要拥有Security Administrator和Server Administrator权限。</li><li>如果需要与OBS服务进行交互，例如创建，导入等操作，则还需要拥有OBS服务的权限，具体请参考<a href="#zh-cn_topic_0170103498_table2730121404">表5</a>。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="17.96%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0170103498_p1767123312213"><a name="zh-cn_topic_0170103498_p1767123312213"></a><a name="zh-cn_topic_0170103498_p1767123312213"></a>细粒度策略</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row5671633026"><td class="cellrowborder" valign="top" width="13.26%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0170103498_p8676331527"><a name="zh-cn_topic_0170103498_p8676331527"></a><a name="zh-cn_topic_0170103498_p8676331527"></a>GES Viewer</p>
</td>
<td class="cellrowborder" valign="top" width="68.78%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0170103498_p16712339211"><a name="zh-cn_topic_0170103498_p16712339211"></a><a name="zh-cn_topic_0170103498_p16712339211"></a>图引擎服务资源只读权限，拥有该权限的用户只能做一些资源查看类的操作如查看图列表、查看元数据和查看备份等。</p>
<div class="note" id="zh-cn_topic_0170103498_note550211118917"><a name="zh-cn_topic_0170103498_note550211118917"></a><a name="zh-cn_topic_0170103498_note550211118917"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0170103498_p1350471114914"><a name="zh-cn_topic_0170103498_p1350471114914"></a><a name="zh-cn_topic_0170103498_p1350471114914"></a>如果需要与OBS服务进行交互，例如查看元数据，则还需要拥有OBS服务的权限，具体请参考<a href="#zh-cn_topic_0170103498_table2730121404">表5</a>。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="17.96%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0170103498_p3687331527"><a name="zh-cn_topic_0170103498_p3687331527"></a><a name="zh-cn_topic_0170103498_p3687331527"></a>细粒度策略</p>
</td>
</tr>
</tbody>
</table>

**表 3**  GES常用操作与RBAC策略关系

<a name="zh-cn_topic_0170103498_table168060107500"></a>
<table><thead align="left"><tr id="zh-cn_topic_0170103498_row167851710165011"><th class="cellrowborder" valign="top" width="19.7%" id="mcps1.2.6.1.1"><p id="zh-cn_topic_0170103498_p187834107502"><a name="zh-cn_topic_0170103498_p187834107502"></a><a name="zh-cn_topic_0170103498_p187834107502"></a>操作</p>
</th>
<th class="cellrowborder" valign="top" width="22.68%" id="mcps1.2.6.1.2"><p id="zh-cn_topic_0170103498_p95088211430"><a name="zh-cn_topic_0170103498_p95088211430"></a><a name="zh-cn_topic_0170103498_p95088211430"></a>GES Administrator</p>
</th>
<th class="cellrowborder" valign="top" width="20.150000000000002%" id="mcps1.2.6.1.3"><p id="zh-cn_topic_0170103498_p1018116305435"><a name="zh-cn_topic_0170103498_p1018116305435"></a><a name="zh-cn_topic_0170103498_p1018116305435"></a>GES Manager</p>
</th>
<th class="cellrowborder" valign="top" width="18.509999999999998%" id="mcps1.2.6.1.4"><p id="zh-cn_topic_0170103498_p1785410145012"><a name="zh-cn_topic_0170103498_p1785410145012"></a><a name="zh-cn_topic_0170103498_p1785410145012"></a>GES Operator</p>
</th>
<th class="cellrowborder" valign="top" width="18.96%" id="mcps1.2.6.1.5"><p id="zh-cn_topic_0170103498_p88621525185820"><a name="zh-cn_topic_0170103498_p88621525185820"></a><a name="zh-cn_topic_0170103498_p88621525185820"></a>Tenant Guest</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0170103498_row7785101014504"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p14402135316428"><a name="zh-cn_topic_0170103498_p14402135316428"></a><a name="zh-cn_topic_0170103498_p14402135316428"></a>创建图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p147852010195013"><a name="zh-cn_topic_0170103498_p147852010195013"></a><a name="zh-cn_topic_0170103498_p147852010195013"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p4576161618453"><a name="zh-cn_topic_0170103498_p4576161618453"></a><a name="zh-cn_topic_0170103498_p4576161618453"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p17785151045016"><a name="zh-cn_topic_0170103498_p17785151045016"></a><a name="zh-cn_topic_0170103498_p17785151045016"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p286215251586"><a name="zh-cn_topic_0170103498_p286215251586"></a><a name="zh-cn_topic_0170103498_p286215251586"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row278612108509"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p240015534426"><a name="zh-cn_topic_0170103498_p240015534426"></a><a name="zh-cn_topic_0170103498_p240015534426"></a>删除图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p1178641011508"><a name="zh-cn_topic_0170103498_p1178641011508"></a><a name="zh-cn_topic_0170103498_p1178641011508"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p1657621616459"><a name="zh-cn_topic_0170103498_p1657621616459"></a><a name="zh-cn_topic_0170103498_p1657621616459"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p177861210175011"><a name="zh-cn_topic_0170103498_p177861210175011"></a><a name="zh-cn_topic_0170103498_p177861210175011"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p88622025115813"><a name="zh-cn_topic_0170103498_p88622025115813"></a><a name="zh-cn_topic_0170103498_p88622025115813"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row8381828185418"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p19363553124215"><a name="zh-cn_topic_0170103498_p19363553124215"></a><a name="zh-cn_topic_0170103498_p19363553124215"></a>查看图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p12713226417"><a name="zh-cn_topic_0170103498_p12713226417"></a><a name="zh-cn_topic_0170103498_p12713226417"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p07212027418"><a name="zh-cn_topic_0170103498_p07212027418"></a><a name="zh-cn_topic_0170103498_p07212027418"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p197826357459"><a name="zh-cn_topic_0170103498_p197826357459"></a><a name="zh-cn_topic_0170103498_p197826357459"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p686212535812"><a name="zh-cn_topic_0170103498_p686212535812"></a><a name="zh-cn_topic_0170103498_p686212535812"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row133826283545"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p4362353114216"><a name="zh-cn_topic_0170103498_p4362353114216"></a><a name="zh-cn_topic_0170103498_p4362353114216"></a>访问图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p17421421946"><a name="zh-cn_topic_0170103498_p17421421946"></a><a name="zh-cn_topic_0170103498_p17421421946"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p167471221442"><a name="zh-cn_topic_0170103498_p167471221442"></a><a name="zh-cn_topic_0170103498_p167471221442"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p678203515453"><a name="zh-cn_topic_0170103498_p678203515453"></a><a name="zh-cn_topic_0170103498_p678203515453"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1486272512588"><a name="zh-cn_topic_0170103498_p1486272512588"></a><a name="zh-cn_topic_0170103498_p1486272512588"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row19786121016507"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p13399125324211"><a name="zh-cn_topic_0170103498_p13399125324211"></a><a name="zh-cn_topic_0170103498_p13399125324211"></a>导入数据</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p27862104506"><a name="zh-cn_topic_0170103498_p27862104506"></a><a name="zh-cn_topic_0170103498_p27862104506"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p6786111012507"><a name="zh-cn_topic_0170103498_p6786111012507"></a><a name="zh-cn_topic_0170103498_p6786111012507"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p7786141045010"><a name="zh-cn_topic_0170103498_p7786141045010"></a><a name="zh-cn_topic_0170103498_p7786141045010"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p0862142515589"><a name="zh-cn_topic_0170103498_p0862142515589"></a><a name="zh-cn_topic_0170103498_p0862142515589"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row162631344716"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p333227185116"><a name="zh-cn_topic_0170103498_p333227185116"></a><a name="zh-cn_topic_0170103498_p333227185116"></a>创建元数据</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p1631239220"><a name="zh-cn_topic_0170103498_p1631239220"></a><a name="zh-cn_topic_0170103498_p1631239220"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p86361339218"><a name="zh-cn_topic_0170103498_p86361339218"></a><a name="zh-cn_topic_0170103498_p86361339218"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p18641337219"><a name="zh-cn_topic_0170103498_p18641337219"></a><a name="zh-cn_topic_0170103498_p18641337219"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p286317251581"><a name="zh-cn_topic_0170103498_p286317251581"></a><a name="zh-cn_topic_0170103498_p286317251581"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row1226315441210"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p733327115117"><a name="zh-cn_topic_0170103498_p733327115117"></a><a name="zh-cn_topic_0170103498_p733327115117"></a>查看元数据</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p2657531825"><a name="zh-cn_topic_0170103498_p2657531825"></a><a name="zh-cn_topic_0170103498_p2657531825"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p26611731126"><a name="zh-cn_topic_0170103498_p26611731126"></a><a name="zh-cn_topic_0170103498_p26611731126"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p7667631213"><a name="zh-cn_topic_0170103498_p7667631213"></a><a name="zh-cn_topic_0170103498_p7667631213"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1086311252581"><a name="zh-cn_topic_0170103498_p1086311252581"></a><a name="zh-cn_topic_0170103498_p1086311252581"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row20264104410118"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p123202710519"><a name="zh-cn_topic_0170103498_p123202710519"></a><a name="zh-cn_topic_0170103498_p123202710519"></a>复制元数据</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p468017310219"><a name="zh-cn_topic_0170103498_p468017310219"></a><a name="zh-cn_topic_0170103498_p468017310219"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p8686133326"><a name="zh-cn_topic_0170103498_p8686133326"></a><a name="zh-cn_topic_0170103498_p8686133326"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p4691631626"><a name="zh-cn_topic_0170103498_p4691631626"></a><a name="zh-cn_topic_0170103498_p4691631626"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p10863102585816"><a name="zh-cn_topic_0170103498_p10863102585816"></a><a name="zh-cn_topic_0170103498_p10863102585816"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row207871710145013"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p2240184118539"><a name="zh-cn_topic_0170103498_p2240184118539"></a><a name="zh-cn_topic_0170103498_p2240184118539"></a>编辑元数据</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p1978720106507"><a name="zh-cn_topic_0170103498_p1978720106507"></a><a name="zh-cn_topic_0170103498_p1978720106507"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p278761017503"><a name="zh-cn_topic_0170103498_p278761017503"></a><a name="zh-cn_topic_0170103498_p278761017503"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p4787161011501"><a name="zh-cn_topic_0170103498_p4787161011501"></a><a name="zh-cn_topic_0170103498_p4787161011501"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p68631725125816"><a name="zh-cn_topic_0170103498_p68631725125816"></a><a name="zh-cn_topic_0170103498_p68631725125816"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row2078811018502"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p19301627165113"><a name="zh-cn_topic_0170103498_p19301627165113"></a><a name="zh-cn_topic_0170103498_p19301627165113"></a>删除元数据</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p6788151020508"><a name="zh-cn_topic_0170103498_p6788151020508"></a><a name="zh-cn_topic_0170103498_p6788151020508"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p117885104502"><a name="zh-cn_topic_0170103498_p117885104502"></a><a name="zh-cn_topic_0170103498_p117885104502"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p167881510105010"><a name="zh-cn_topic_0170103498_p167881510105010"></a><a name="zh-cn_topic_0170103498_p167881510105010"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p286312256585"><a name="zh-cn_topic_0170103498_p286312256585"></a><a name="zh-cn_topic_0170103498_p286312256585"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row478831005013"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p102016114482"><a name="zh-cn_topic_0170103498_p102016114482"></a><a name="zh-cn_topic_0170103498_p102016114482"></a>清空数据</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p17788191025020"><a name="zh-cn_topic_0170103498_p17788191025020"></a><a name="zh-cn_topic_0170103498_p17788191025020"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p1378861016502"><a name="zh-cn_topic_0170103498_p1378861016502"></a><a name="zh-cn_topic_0170103498_p1378861016502"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p3788141014504"><a name="zh-cn_topic_0170103498_p3788141014504"></a><a name="zh-cn_topic_0170103498_p3788141014504"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p7863152518588"><a name="zh-cn_topic_0170103498_p7863152518588"></a><a name="zh-cn_topic_0170103498_p7863152518588"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row144701652142415"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p739805311429"><a name="zh-cn_topic_0170103498_p739805311429"></a><a name="zh-cn_topic_0170103498_p739805311429"></a>备份图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p3972311182513"><a name="zh-cn_topic_0170103498_p3972311182513"></a><a name="zh-cn_topic_0170103498_p3972311182513"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p09783115257"><a name="zh-cn_topic_0170103498_p09783115257"></a><a name="zh-cn_topic_0170103498_p09783115257"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1985511102511"><a name="zh-cn_topic_0170103498_p1985511102511"></a><a name="zh-cn_topic_0170103498_p1985511102511"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p10863625155818"><a name="zh-cn_topic_0170103498_p10863625155818"></a><a name="zh-cn_topic_0170103498_p10863625155818"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row1179020106509"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p121011551503"><a name="zh-cn_topic_0170103498_p121011551503"></a><a name="zh-cn_topic_0170103498_p121011551503"></a>载入备份</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p13790161013508"><a name="zh-cn_topic_0170103498_p13790161013508"></a><a name="zh-cn_topic_0170103498_p13790161013508"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p1879071085016"><a name="zh-cn_topic_0170103498_p1879071085016"></a><a name="zh-cn_topic_0170103498_p1879071085016"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p157909109501"><a name="zh-cn_topic_0170103498_p157909109501"></a><a name="zh-cn_topic_0170103498_p157909109501"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p486314251588"><a name="zh-cn_topic_0170103498_p486314251588"></a><a name="zh-cn_topic_0170103498_p486314251588"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row107921010195018"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p010011515013"><a name="zh-cn_topic_0170103498_p010011515013"></a><a name="zh-cn_topic_0170103498_p010011515013"></a>删除备份</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p12792131045011"><a name="zh-cn_topic_0170103498_p12792131045011"></a><a name="zh-cn_topic_0170103498_p12792131045011"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p179261015501"><a name="zh-cn_topic_0170103498_p179261015501"></a><a name="zh-cn_topic_0170103498_p179261015501"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p16792171018502"><a name="zh-cn_topic_0170103498_p16792171018502"></a><a name="zh-cn_topic_0170103498_p16792171018502"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1886313258585"><a name="zh-cn_topic_0170103498_p1886313258585"></a><a name="zh-cn_topic_0170103498_p1886313258585"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row993619553214"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p19937255322"><a name="zh-cn_topic_0170103498_p19937255322"></a><a name="zh-cn_topic_0170103498_p19937255322"></a>查看备份</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p176787471633"><a name="zh-cn_topic_0170103498_p176787471633"></a><a name="zh-cn_topic_0170103498_p176787471633"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p56795474319"><a name="zh-cn_topic_0170103498_p56795474319"></a><a name="zh-cn_topic_0170103498_p56795474319"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p467911471339"><a name="zh-cn_topic_0170103498_p467911471339"></a><a name="zh-cn_topic_0170103498_p467911471339"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p86792476317"><a name="zh-cn_topic_0170103498_p86792476317"></a><a name="zh-cn_topic_0170103498_p86792476317"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row179310103506"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p139712530421"><a name="zh-cn_topic_0170103498_p139712530421"></a><a name="zh-cn_topic_0170103498_p139712530421"></a>启动图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p97920106508"><a name="zh-cn_topic_0170103498_p97920106508"></a><a name="zh-cn_topic_0170103498_p97920106508"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p67931410175019"><a name="zh-cn_topic_0170103498_p67931410175019"></a><a name="zh-cn_topic_0170103498_p67931410175019"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p77932010155017"><a name="zh-cn_topic_0170103498_p77932010155017"></a><a name="zh-cn_topic_0170103498_p77932010155017"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p12863825165817"><a name="zh-cn_topic_0170103498_p12863825165817"></a><a name="zh-cn_topic_0170103498_p12863825165817"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row1879381010500"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p16396195324213"><a name="zh-cn_topic_0170103498_p16396195324213"></a><a name="zh-cn_topic_0170103498_p16396195324213"></a>停止图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p1793131019503"><a name="zh-cn_topic_0170103498_p1793131019503"></a><a name="zh-cn_topic_0170103498_p1793131019503"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p979361095010"><a name="zh-cn_topic_0170103498_p979361095010"></a><a name="zh-cn_topic_0170103498_p979361095010"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p1979313105504"><a name="zh-cn_topic_0170103498_p1979313105504"></a><a name="zh-cn_topic_0170103498_p1979313105504"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p88632259586"><a name="zh-cn_topic_0170103498_p88632259586"></a><a name="zh-cn_topic_0170103498_p88632259586"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row37931810125019"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p203937534423"><a name="zh-cn_topic_0170103498_p203937534423"></a><a name="zh-cn_topic_0170103498_p203937534423"></a>升级图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p37931210155015"><a name="zh-cn_topic_0170103498_p37931210155015"></a><a name="zh-cn_topic_0170103498_p37931210155015"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p37932108509"><a name="zh-cn_topic_0170103498_p37932108509"></a><a name="zh-cn_topic_0170103498_p37932108509"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p3793910175014"><a name="zh-cn_topic_0170103498_p3793910175014"></a><a name="zh-cn_topic_0170103498_p3793910175014"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p16863325135811"><a name="zh-cn_topic_0170103498_p16863325135811"></a><a name="zh-cn_topic_0170103498_p16863325135811"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row9795121014500"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p13924538423"><a name="zh-cn_topic_0170103498_p13924538423"></a><a name="zh-cn_topic_0170103498_p13924538423"></a>导出图</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p179520104503"><a name="zh-cn_topic_0170103498_p179520104503"></a><a name="zh-cn_topic_0170103498_p179520104503"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p1579501012507"><a name="zh-cn_topic_0170103498_p1579501012507"></a><a name="zh-cn_topic_0170103498_p1579501012507"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p379591019507"><a name="zh-cn_topic_0170103498_p379591019507"></a><a name="zh-cn_topic_0170103498_p379591019507"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1986312514586"><a name="zh-cn_topic_0170103498_p1986312514586"></a><a name="zh-cn_topic_0170103498_p1986312514586"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row12151143912215"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p0391135354215"><a name="zh-cn_topic_0170103498_p0391135354215"></a><a name="zh-cn_topic_0170103498_p0391135354215"></a>绑定EIP</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p184863212316"><a name="zh-cn_topic_0170103498_p184863212316"></a><a name="zh-cn_topic_0170103498_p184863212316"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p105733214313"><a name="zh-cn_topic_0170103498_p105733214313"></a><a name="zh-cn_topic_0170103498_p105733214313"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p156314323315"><a name="zh-cn_topic_0170103498_p156314323315"></a><a name="zh-cn_topic_0170103498_p156314323315"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p19863172514582"><a name="zh-cn_topic_0170103498_p19863172514582"></a><a name="zh-cn_topic_0170103498_p19863172514582"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row1615214391725"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p2390145314216"><a name="zh-cn_topic_0170103498_p2390145314216"></a><a name="zh-cn_topic_0170103498_p2390145314216"></a>解绑EIP</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p17771932230"><a name="zh-cn_topic_0170103498_p17771932230"></a><a name="zh-cn_topic_0170103498_p17771932230"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p2821632436"><a name="zh-cn_topic_0170103498_p2821632436"></a><a name="zh-cn_topic_0170103498_p2821632436"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p3907326317"><a name="zh-cn_topic_0170103498_p3907326317"></a><a name="zh-cn_topic_0170103498_p3907326317"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1863162516581"><a name="zh-cn_topic_0170103498_p1863162516581"></a><a name="zh-cn_topic_0170103498_p1863162516581"></a>×</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row2024417919314"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0170103498_p4244991634"><a name="zh-cn_topic_0170103498_p4244991634"></a><a name="zh-cn_topic_0170103498_p4244991634"></a>查看任务中心</p>
</td>
<td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0170103498_p9100150730"><a name="zh-cn_topic_0170103498_p9100150730"></a><a name="zh-cn_topic_0170103498_p9100150730"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.150000000000002%" headers="mcps1.2.6.1.3 "><p id="zh-cn_topic_0170103498_p610017501032"><a name="zh-cn_topic_0170103498_p610017501032"></a><a name="zh-cn_topic_0170103498_p610017501032"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0170103498_p01011550939"><a name="zh-cn_topic_0170103498_p01011550939"></a><a name="zh-cn_topic_0170103498_p01011550939"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.6.1.5 "><p id="zh-cn_topic_0170103498_p1110117501739"><a name="zh-cn_topic_0170103498_p1110117501739"></a><a name="zh-cn_topic_0170103498_p1110117501739"></a>√</p>
</td>
</tr>
</tbody>
</table>

**表 4**  GES常用操作与细粒度策略关系

<a name="zh-cn_topic_0170103498_table06491545446"></a>
<table><thead align="left"><tr id="zh-cn_topic_0170103498_row22015461048"><th class="cellrowborder" valign="top" width="30.693069306930692%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0170103498_p152015461246"><a name="zh-cn_topic_0170103498_p152015461246"></a><a name="zh-cn_topic_0170103498_p152015461246"></a>操作</p>
</th>
<th class="cellrowborder" valign="top" width="23.102310231023104%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0170103498_p1020116461641"><a name="zh-cn_topic_0170103498_p1020116461641"></a><a name="zh-cn_topic_0170103498_p1020116461641"></a>GES Admin</p>
</th>
<th class="cellrowborder" valign="top" width="23.102310231023104%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0170103498_p32011646546"><a name="zh-cn_topic_0170103498_p32011646546"></a><a name="zh-cn_topic_0170103498_p32011646546"></a>GES User</p>
</th>
<th class="cellrowborder" valign="top" width="23.102310231023104%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0170103498_p220111460418"><a name="zh-cn_topic_0170103498_p220111460418"></a><a name="zh-cn_topic_0170103498_p220111460418"></a>GES Viewer</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0170103498_row1420112461642"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p5201546648"><a name="zh-cn_topic_0170103498_p5201546648"></a><a name="zh-cn_topic_0170103498_p5201546648"></a>查询图列表</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p1420119463417"><a name="zh-cn_topic_0170103498_p1420119463417"></a><a name="zh-cn_topic_0170103498_p1420119463417"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p22019461641"><a name="zh-cn_topic_0170103498_p22019461641"></a><a name="zh-cn_topic_0170103498_p22019461641"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p1320114618415"><a name="zh-cn_topic_0170103498_p1320114618415"></a><a name="zh-cn_topic_0170103498_p1320114618415"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row620113461749"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p420274618415"><a name="zh-cn_topic_0170103498_p420274618415"></a><a name="zh-cn_topic_0170103498_p420274618415"></a>查看图详情</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p12021846040"><a name="zh-cn_topic_0170103498_p12021846040"></a><a name="zh-cn_topic_0170103498_p12021846040"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p122029466415"><a name="zh-cn_topic_0170103498_p122029466415"></a><a name="zh-cn_topic_0170103498_p122029466415"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p1020216462413"><a name="zh-cn_topic_0170103498_p1020216462413"></a><a name="zh-cn_topic_0170103498_p1020216462413"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row10202124610411"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p72029461546"><a name="zh-cn_topic_0170103498_p72029461546"></a><a name="zh-cn_topic_0170103498_p72029461546"></a>创建图</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p14202144620411"><a name="zh-cn_topic_0170103498_p14202144620411"></a><a name="zh-cn_topic_0170103498_p14202144620411"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p02027462417"><a name="zh-cn_topic_0170103498_p02027462417"></a><a name="zh-cn_topic_0170103498_p02027462417"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p9202164615416"><a name="zh-cn_topic_0170103498_p9202164615416"></a><a name="zh-cn_topic_0170103498_p9202164615416"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row10202174610413"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p182021546541"><a name="zh-cn_topic_0170103498_p182021546541"></a><a name="zh-cn_topic_0170103498_p182021546541"></a>关闭图</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p13202246446"><a name="zh-cn_topic_0170103498_p13202246446"></a><a name="zh-cn_topic_0170103498_p13202246446"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p19202154613418"><a name="zh-cn_topic_0170103498_p19202154613418"></a><a name="zh-cn_topic_0170103498_p19202154613418"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p202034461741"><a name="zh-cn_topic_0170103498_p202034461741"></a><a name="zh-cn_topic_0170103498_p202034461741"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row62036465412"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p152033462047"><a name="zh-cn_topic_0170103498_p152033462047"></a><a name="zh-cn_topic_0170103498_p152033462047"></a>启动图</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p1720313468414"><a name="zh-cn_topic_0170103498_p1720313468414"></a><a name="zh-cn_topic_0170103498_p1720313468414"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p0203846749"><a name="zh-cn_topic_0170103498_p0203846749"></a><a name="zh-cn_topic_0170103498_p0203846749"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p1920316466411"><a name="zh-cn_topic_0170103498_p1920316466411"></a><a name="zh-cn_topic_0170103498_p1920316466411"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row520315461040"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p720311463412"><a name="zh-cn_topic_0170103498_p720311463412"></a><a name="zh-cn_topic_0170103498_p720311463412"></a>删除图</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p42039461845"><a name="zh-cn_topic_0170103498_p42039461845"></a><a name="zh-cn_topic_0170103498_p42039461845"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p120313465416"><a name="zh-cn_topic_0170103498_p120313465416"></a><a name="zh-cn_topic_0170103498_p120313465416"></a>x</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p82036467418"><a name="zh-cn_topic_0170103498_p82036467418"></a><a name="zh-cn_topic_0170103498_p82036467418"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row10203144614411"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p62031246444"><a name="zh-cn_topic_0170103498_p62031246444"></a><a name="zh-cn_topic_0170103498_p62031246444"></a>增量导入图</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p16204346442"><a name="zh-cn_topic_0170103498_p16204346442"></a><a name="zh-cn_topic_0170103498_p16204346442"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p142041046445"><a name="zh-cn_topic_0170103498_p142041046445"></a><a name="zh-cn_topic_0170103498_p142041046445"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p182042467411"><a name="zh-cn_topic_0170103498_p182042467411"></a><a name="zh-cn_topic_0170103498_p182042467411"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row17204114618413"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p620420462041"><a name="zh-cn_topic_0170103498_p620420462041"></a><a name="zh-cn_topic_0170103498_p620420462041"></a>导出图</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p12204646544"><a name="zh-cn_topic_0170103498_p12204646544"></a><a name="zh-cn_topic_0170103498_p12204646544"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p1220464615410"><a name="zh-cn_topic_0170103498_p1220464615410"></a><a name="zh-cn_topic_0170103498_p1220464615410"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p10204246841"><a name="zh-cn_topic_0170103498_p10204246841"></a><a name="zh-cn_topic_0170103498_p10204246841"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row320417465412"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p112042046842"><a name="zh-cn_topic_0170103498_p112042046842"></a><a name="zh-cn_topic_0170103498_p112042046842"></a>清空图</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p102041046147"><a name="zh-cn_topic_0170103498_p102041046147"></a><a name="zh-cn_topic_0170103498_p102041046147"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p620415463420"><a name="zh-cn_topic_0170103498_p620415463420"></a><a name="zh-cn_topic_0170103498_p620415463420"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p52054466414"><a name="zh-cn_topic_0170103498_p52054466414"></a><a name="zh-cn_topic_0170103498_p52054466414"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row420519469413"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p3205134616415"><a name="zh-cn_topic_0170103498_p3205134616415"></a><a name="zh-cn_topic_0170103498_p3205134616415"></a>升级图</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p2205134618415"><a name="zh-cn_topic_0170103498_p2205134618415"></a><a name="zh-cn_topic_0170103498_p2205134618415"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p152056467420"><a name="zh-cn_topic_0170103498_p152056467420"></a><a name="zh-cn_topic_0170103498_p152056467420"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p12057464415"><a name="zh-cn_topic_0170103498_p12057464415"></a><a name="zh-cn_topic_0170103498_p12057464415"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row11205946645"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p420520467420"><a name="zh-cn_topic_0170103498_p420520467420"></a><a name="zh-cn_topic_0170103498_p420520467420"></a>绑定EIP</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p420518461147"><a name="zh-cn_topic_0170103498_p420518461147"></a><a name="zh-cn_topic_0170103498_p420518461147"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p4205124613419"><a name="zh-cn_topic_0170103498_p4205124613419"></a><a name="zh-cn_topic_0170103498_p4205124613419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p82058465420"><a name="zh-cn_topic_0170103498_p82058465420"></a><a name="zh-cn_topic_0170103498_p82058465420"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row72051846743"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p420619468414"><a name="zh-cn_topic_0170103498_p420619468414"></a><a name="zh-cn_topic_0170103498_p420619468414"></a>解绑EIP</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p10206174611412"><a name="zh-cn_topic_0170103498_p10206174611412"></a><a name="zh-cn_topic_0170103498_p10206174611412"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p14206174615419"><a name="zh-cn_topic_0170103498_p14206174615419"></a><a name="zh-cn_topic_0170103498_p14206174615419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p1220619461049"><a name="zh-cn_topic_0170103498_p1220619461049"></a><a name="zh-cn_topic_0170103498_p1220619461049"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row42065461741"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p1620615468419"><a name="zh-cn_topic_0170103498_p1620615468419"></a><a name="zh-cn_topic_0170103498_p1620615468419"></a>查看所有备份列表</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p72062468414"><a name="zh-cn_topic_0170103498_p72062468414"></a><a name="zh-cn_topic_0170103498_p72062468414"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p192068461349"><a name="zh-cn_topic_0170103498_p192068461349"></a><a name="zh-cn_topic_0170103498_p192068461349"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p1920620462410"><a name="zh-cn_topic_0170103498_p1920620462410"></a><a name="zh-cn_topic_0170103498_p1920620462410"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row14206546344"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p2020617466410"><a name="zh-cn_topic_0170103498_p2020617466410"></a><a name="zh-cn_topic_0170103498_p2020617466410"></a>查看某个图的备份列表</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p42061462411"><a name="zh-cn_topic_0170103498_p42061462411"></a><a name="zh-cn_topic_0170103498_p42061462411"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p9206146342"><a name="zh-cn_topic_0170103498_p9206146342"></a><a name="zh-cn_topic_0170103498_p9206146342"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p0206154614413"><a name="zh-cn_topic_0170103498_p0206154614413"></a><a name="zh-cn_topic_0170103498_p0206154614413"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row3206146149"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p192074462414"><a name="zh-cn_topic_0170103498_p192074462414"></a><a name="zh-cn_topic_0170103498_p192074462414"></a>新增备份</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p920711461648"><a name="zh-cn_topic_0170103498_p920711461648"></a><a name="zh-cn_topic_0170103498_p920711461648"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p14207114612416"><a name="zh-cn_topic_0170103498_p14207114612416"></a><a name="zh-cn_topic_0170103498_p14207114612416"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p122071546449"><a name="zh-cn_topic_0170103498_p122071546449"></a><a name="zh-cn_topic_0170103498_p122071546449"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row182078461343"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p18207346849"><a name="zh-cn_topic_0170103498_p18207346849"></a><a name="zh-cn_topic_0170103498_p18207346849"></a>删除备份</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p920717461643"><a name="zh-cn_topic_0170103498_p920717461643"></a><a name="zh-cn_topic_0170103498_p920717461643"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p132079461245"><a name="zh-cn_topic_0170103498_p132079461245"></a><a name="zh-cn_topic_0170103498_p132079461245"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p16207144617413"><a name="zh-cn_topic_0170103498_p16207144617413"></a><a name="zh-cn_topic_0170103498_p16207144617413"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row1207946448"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p52076467413"><a name="zh-cn_topic_0170103498_p52076467413"></a><a name="zh-cn_topic_0170103498_p52076467413"></a>查询元数据列表</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p42071246142"><a name="zh-cn_topic_0170103498_p42071246142"></a><a name="zh-cn_topic_0170103498_p42071246142"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p14207154611413"><a name="zh-cn_topic_0170103498_p14207154611413"></a><a name="zh-cn_topic_0170103498_p14207154611413"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p6207144615412"><a name="zh-cn_topic_0170103498_p6207144615412"></a><a name="zh-cn_topic_0170103498_p6207144615412"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row2020794615412"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p32071046947"><a name="zh-cn_topic_0170103498_p32071046947"></a><a name="zh-cn_topic_0170103498_p32071046947"></a>查询元数据</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p1020704611410"><a name="zh-cn_topic_0170103498_p1020704611410"></a><a name="zh-cn_topic_0170103498_p1020704611410"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p182076461341"><a name="zh-cn_topic_0170103498_p182076461341"></a><a name="zh-cn_topic_0170103498_p182076461341"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p112084469412"><a name="zh-cn_topic_0170103498_p112084469412"></a><a name="zh-cn_topic_0170103498_p112084469412"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row220814614413"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p1420817462419"><a name="zh-cn_topic_0170103498_p1420817462419"></a><a name="zh-cn_topic_0170103498_p1420817462419"></a>校验元数据</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p172084467416"><a name="zh-cn_topic_0170103498_p172084467416"></a><a name="zh-cn_topic_0170103498_p172084467416"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p920813463413"><a name="zh-cn_topic_0170103498_p920813463413"></a><a name="zh-cn_topic_0170103498_p920813463413"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p1820811461243"><a name="zh-cn_topic_0170103498_p1820811461243"></a><a name="zh-cn_topic_0170103498_p1820811461243"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row5208246648"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p92084461145"><a name="zh-cn_topic_0170103498_p92084461145"></a><a name="zh-cn_topic_0170103498_p92084461145"></a>新增元数据</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p7208174613419"><a name="zh-cn_topic_0170103498_p7208174613419"></a><a name="zh-cn_topic_0170103498_p7208174613419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p1320815467419"><a name="zh-cn_topic_0170103498_p1320815467419"></a><a name="zh-cn_topic_0170103498_p1320815467419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p220814469420"><a name="zh-cn_topic_0170103498_p220814469420"></a><a name="zh-cn_topic_0170103498_p220814469420"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row72089467419"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p1920816467412"><a name="zh-cn_topic_0170103498_p1920816467412"></a><a name="zh-cn_topic_0170103498_p1920816467412"></a>删除元数据</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p52081446342"><a name="zh-cn_topic_0170103498_p52081446342"></a><a name="zh-cn_topic_0170103498_p52081446342"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p17208346844"><a name="zh-cn_topic_0170103498_p17208346844"></a><a name="zh-cn_topic_0170103498_p17208346844"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p1920819461747"><a name="zh-cn_topic_0170103498_p1920819461747"></a><a name="zh-cn_topic_0170103498_p1920819461747"></a>x</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row520814461741"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p12208144618413"><a name="zh-cn_topic_0170103498_p12208144618413"></a><a name="zh-cn_topic_0170103498_p12208144618413"></a>查询任务状态</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p1520918464420"><a name="zh-cn_topic_0170103498_p1520918464420"></a><a name="zh-cn_topic_0170103498_p1520918464420"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p020914461848"><a name="zh-cn_topic_0170103498_p020914461848"></a><a name="zh-cn_topic_0170103498_p020914461848"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p3209134619414"><a name="zh-cn_topic_0170103498_p3209134619414"></a><a name="zh-cn_topic_0170103498_p3209134619414"></a>√</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row112093461418"><td class="cellrowborder" valign="top" width="30.693069306930692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0170103498_p1320915461547"><a name="zh-cn_topic_0170103498_p1320915461547"></a><a name="zh-cn_topic_0170103498_p1320915461547"></a>查询任务列表</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0170103498_p4209746946"><a name="zh-cn_topic_0170103498_p4209746946"></a><a name="zh-cn_topic_0170103498_p4209746946"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0170103498_p1920914461543"><a name="zh-cn_topic_0170103498_p1920914461543"></a><a name="zh-cn_topic_0170103498_p1920914461543"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="23.102310231023104%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0170103498_p1320924619418"><a name="zh-cn_topic_0170103498_p1320924619418"></a><a name="zh-cn_topic_0170103498_p1320924619418"></a>√</p>
</td>
</tr>
</tbody>
</table>

**表 5**  GES常用操作对OBS权限的依赖关系

<a name="zh-cn_topic_0170103498_table2730121404"></a>
<table><thead align="left"><tr id="zh-cn_topic_0170103498_row073110214012"><th class="cellrowborder" valign="top" width="34.93%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0170103498_p47311121602"><a name="zh-cn_topic_0170103498_p47311121602"></a><a name="zh-cn_topic_0170103498_p47311121602"></a>GES操作</p>
</th>
<th class="cellrowborder" valign="top" width="65.07%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0170103498_p7731427016"><a name="zh-cn_topic_0170103498_p7731427016"></a><a name="zh-cn_topic_0170103498_p7731427016"></a>依赖的OBS权限</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0170103498_row673116215018"><td class="cellrowborder" valign="top" width="34.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0170103498_p595402212115"><a name="zh-cn_topic_0170103498_p595402212115"></a><a name="zh-cn_topic_0170103498_p595402212115"></a>查看元数据</p>
</td>
<td class="cellrowborder" valign="top" width="65.07%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0170103498_p29551022215"><a name="zh-cn_topic_0170103498_p29551022215"></a><a name="zh-cn_topic_0170103498_p29551022215"></a>OBS Viewer细粒度策略或者OBS Buckets Viewer RBAC策略</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row88216135114"><td class="cellrowborder" valign="top" width="34.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0170103498_p695592210115"><a name="zh-cn_topic_0170103498_p695592210115"></a><a name="zh-cn_topic_0170103498_p695592210115"></a>创建/导入/复制/编辑/删除元数据</p>
</td>
<td class="cellrowborder" valign="top" width="65.07%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0170103498_p13955022019"><a name="zh-cn_topic_0170103498_p13955022019"></a><a name="zh-cn_topic_0170103498_p13955022019"></a>OBS Operator细粒度策略或者Tenant Administrator RBAC策略</p>
</td>
</tr>
<tr id="zh-cn_topic_0170103498_row0558220217"><td class="cellrowborder" valign="top" width="34.93%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0170103498_p1495520221613"><a name="zh-cn_topic_0170103498_p1495520221613"></a><a name="zh-cn_topic_0170103498_p1495520221613"></a>创建图（带初始数据），导入图/导出图</p>
</td>
<td class="cellrowborder" valign="top" width="65.07%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0170103498_p19955022211"><a name="zh-cn_topic_0170103498_p19955022211"></a><a name="zh-cn_topic_0170103498_p19955022211"></a>OBS Operator细粒度策略或者Tenant Administrator RBAC策略</p>
</td>
</tr>
</tbody>
</table>

