# 点集共同邻居（Common Neighbors of Vertex Sets）<a name="ges_01_0087"></a>

## 概述<a name="section15370184961812"></a>

点集共同邻居（Common Neighbors of Vertex Sets）可以得到两个点集合（群体集合）所共有的邻居（即两个群体临域的交集），直观的发现与两个群体共同联系的对象，如发现社交场合中的共同好友、消费领域共同感兴趣的商品、社区群体共同接触过的人，进一步推测两点集合之间的潜在关系和联系程度。

## 适用场景<a name="section112811508199"></a>

点集共同邻居算法适用于进行关系发掘、产品/好友推荐等图分析技术。

## 参数说明<a name="section23411131219"></a>

**表 1**  Common Neighbors of Vertex Sets参数说明

<a name="table4824123719420"></a>
<table><thead align="left"><tr id="row17825537646"><th class="cellrowborder" valign="top" width="16.666666666666664%" id="mcps1.2.7.1.1"><p id="p43910435419"><a name="p43910435419"></a><a name="p43910435419"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.407718456308737%" id="mcps1.2.7.1.2"><p id="p14398430419"><a name="p14398430419"></a><a name="p14398430419"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.437112577484504%" id="mcps1.2.7.1.3"><p id="p539114319411"><a name="p539114319411"></a><a name="p539114319411"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="13.3873225354929%" id="mcps1.2.7.1.4"><p id="p12391439418"><a name="p12391439418"></a><a name="p12391439418"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="27.43451309738052%" id="mcps1.2.7.1.5"><p id="p1639043141"><a name="p1639043141"></a><a name="p1639043141"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="16.666666666666664%" id="mcps1.2.7.1.6"><p id="p17391043548"><a name="p17391043548"></a><a name="p17391043548"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1182517371346"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p6391343340"><a name="p6391343340"></a><a name="p6391343340"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="11.407718456308737%" headers="mcps1.2.7.1.2 "><p id="p153917435410"><a name="p153917435410"></a><a name="p153917435410"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.437112577484504%" headers="mcps1.2.7.1.3 "><p id="p739144310416"><a name="p739144310416"></a><a name="p739144310416"></a>起点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="13.3873225354929%" headers="mcps1.2.7.1.4 "><p id="p4401435418"><a name="p4401435418"></a><a name="p4401435418"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="27.43451309738052%" headers="mcps1.2.7.1.5 "><p id="p14401643943"><a name="p14401643943"></a><a name="p14401643943"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”。</p>
<p id="p13401643049"><a name="p13401643049"></a><a name="p13401643049"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p34012431944"><a name="p34012431944"></a><a name="p34012431944"></a>-</p>
</td>
</tr>
<tr id="row482517371248"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p140843844"><a name="p140843844"></a><a name="p140843844"></a>targets</p>
</td>
<td class="cellrowborder" valign="top" width="11.407718456308737%" headers="mcps1.2.7.1.2 "><p id="p13404432419"><a name="p13404432419"></a><a name="p13404432419"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.437112577484504%" headers="mcps1.2.7.1.3 "><p id="p204010430416"><a name="p204010430416"></a><a name="p204010430416"></a>终点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="13.3873225354929%" headers="mcps1.2.7.1.4 "><p id="p8401643846"><a name="p8401643846"></a><a name="p8401643846"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="27.43451309738052%" headers="mcps1.2.7.1.5 "><p id="p34010431540"><a name="p34010431540"></a><a name="p34010431540"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Mike,Amy”。</p>
<p id="p16403439419"><a name="p16403439419"></a><a name="p16403439419"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p24014431743"><a name="p24014431743"></a><a name="p24014431743"></a>-</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

无。

## 示例<a name="section923518617196"></a>

输入参数sources=Alice,Nana，targets=Mike,Amy，计算结果会展示在绘图区，JSON结果会展示在查询结果区。

