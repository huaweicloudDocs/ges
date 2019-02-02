# k核算法（k-core）<a name="ges_01_0033"></a>

## 概述<a name="section204471932366"></a>

k核算法（k-core）是图算法中的一个经典算法，用以计算每个节点的核数。其计算结果是判断节点重要性最常用的参考值之一，较好的体现了节点的传播能力。

## 适用场景<a name="section601156549586"></a>

k核算法（k-core）适用于社区发现、金融风控等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  k核算法（k-core）参数说明

<a name="table1195419507343"></a>
<table><thead align="left"><tr id="row99631850173412"><th class="cellrowborder" valign="top" width="13%" id="mcps1.2.7.1.1"><p id="p109641750203412"><a name="p109641750203412"></a><a name="p109641750203412"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.2"><p id="p8969115063412"><a name="p8969115063412"></a><a name="p8969115063412"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="30.97%" id="mcps1.2.7.1.3"><p id="p13970150143414"><a name="p13970150143414"></a><a name="p13970150143414"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="6.140000000000001%" id="mcps1.2.7.1.4"><p id="p1193205172815"><a name="p1193205172815"></a><a name="p1193205172815"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="19.89%" id="mcps1.2.7.1.5"><p id="p797265013410"><a name="p797265013410"></a><a name="p797265013410"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.7.1.6"><p id="p345617411412"><a name="p345617411412"></a><a name="p345617411412"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row11975155043410"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.1 "><p id="p897614501340"><a name="p897614501340"></a><a name="p897614501340"></a>k</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p1598065011341"><a name="p1598065011341"></a><a name="p1598065011341"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="30.97%" headers="mcps1.2.7.1.3 "><p id="p3982950203412"><a name="p3982950203412"></a><a name="p3982950203412"></a>核数。</p>
<p id="p20671725172810"><a name="p20671725172810"></a><a name="p20671725172810"></a>算法会返回核数大于等于k的节点。</p>
</td>
<td class="cellrowborder" valign="top" width="6.140000000000001%" headers="mcps1.2.7.1.4 "><p id="p12932517284"><a name="p12932517284"></a><a name="p12932517284"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.89%" headers="mcps1.2.7.1.5 "><p id="p5439601785"><a name="p5439601785"></a><a name="p5439601785"></a>大于等于0</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p94561842042"><a name="p94561842042"></a><a name="p94561842042"></a>-</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

无。

## 示例<a name="section9539286457"></a>

输入参数k=10，计算结果中核数大于等于10的节点组成的子图会展示在绘图区，节点颜色根据核数来区别，JSON结果会展示在查询结果区。

