# 共同邻居算法（Common Neighbors）<a name="ges_01_0049"></a>

## 概述<a name="section204471932366"></a>

共同邻居算法（Common Neighbors）是一种常用的基本图分析算法，可以得到两个节点所共有的邻居节点，直观地发现社交场合中的共同好友、以及在消费领域共同感兴趣的商品，进一步推测两个节点之间的潜在关系和相近程度。

## 适用场景<a name="section811037094324"></a>

共同邻居算法（Common Neighbors）适用于电商、社交等多领域的推荐场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  共同邻居参数说明

<a name="table114811369408"></a>
<table><thead align="left"><tr id="row35031336114013"><th class="cellrowborder" valign="top" width="13%" id="mcps1.2.7.1.1"><p id="p1150912369402"><a name="p1150912369402"></a><a name="p1150912369402"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.7.1.2"><p id="p18515163674011"><a name="p18515163674011"></a><a name="p18515163674011"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.2.7.1.3"><p id="p115202036174016"><a name="p115202036174016"></a><a name="p115202036174016"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="11%" id="mcps1.2.7.1.4"><p id="p53945549433"><a name="p53945549433"></a><a name="p53945549433"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.7.1.5"><p id="p1525163617404"><a name="p1525163617404"></a><a name="p1525163617404"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.7.1.6"><p id="p223325910432"><a name="p223325910432"></a><a name="p223325910432"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1753443614018"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.1 "><p id="p17539636134010"><a name="p17539636134010"></a><a name="p17539636134010"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p7545153613405"><a name="p7545153613405"></a><a name="p7545153613405"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.7.1.3 "><p id="p15549936154014"><a name="p15549936154014"></a><a name="p15549936154014"></a>输入起点ID</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.7.1.4 "><p id="p12394205410438"><a name="p12394205410438"></a><a name="p12394205410438"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.5 "><p id="p1455513617408"><a name="p1455513617408"></a><a name="p1455513617408"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p82331591435"><a name="p82331591435"></a><a name="p82331591435"></a>-</p>
</td>
</tr>
<tr id="row15560143684016"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.7.1.1 "><p id="p1056517368409"><a name="p1056517368409"></a><a name="p1056517368409"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.7.1.2 "><p id="p205711636114019"><a name="p205711636114019"></a><a name="p205711636114019"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.7.1.3 "><p id="p1757614364403"><a name="p1757614364403"></a><a name="p1757614364403"></a>输入终点ID</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.7.1.4 "><p id="p239413549438"><a name="p239413549438"></a><a name="p239413549438"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.7.1.5 "><p id="p355917192416"><a name="p355917192416"></a><a name="p355917192416"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.7.1.6 "><p id="p19233125915431"><a name="p19233125915431"></a><a name="p19233125915431"></a>-</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

无。

## 示例<a name="section9539286457"></a>

输入参数source=Lee，target=Alice，计算结果会展示在绘图区，JSON结果会展示在查询结果区。

