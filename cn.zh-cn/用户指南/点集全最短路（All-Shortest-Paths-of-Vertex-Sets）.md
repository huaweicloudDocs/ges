# 点集全最短路（All Shortest Paths of Vertex Sets）<a name="ges_01_0086"></a>

## 概述<a name="section15370184961812"></a>

点集全最短路算法（Shortest Path of Vertex Sets）用于发现两个点集之间的所有最短路径。

## 适用场景<a name="section112811508199"></a>

点集最短路算法可应用于互联网社交、金融风控、路网交通、物流配送等场景下的区块之间关系的分析。

## 参数说明<a name="section23411131219"></a>

**表 1**  All Shortest Paths of Vertex Sets参数说明

<a name="table4824123719420"></a>
<table><thead align="left"><tr id="row17825537646"><th class="cellrowborder" valign="top" width="12.11757648470306%" id="mcps1.2.7.1.1"><p id="p43910435419"><a name="p43910435419"></a><a name="p43910435419"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.238152369526095%" id="mcps1.2.7.1.2"><p id="p14398430419"><a name="p14398430419"></a><a name="p14398430419"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.647070585882824%" id="mcps1.2.7.1.3"><p id="p539114319411"><a name="p539114319411"></a><a name="p539114319411"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.588082383523295%" id="mcps1.2.7.1.4"><p id="p12391439418"><a name="p12391439418"></a><a name="p12391439418"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="30.77384523095381%" id="mcps1.2.7.1.5"><p id="p1639043141"><a name="p1639043141"></a><a name="p1639043141"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="23.635272945410918%" id="mcps1.2.7.1.6"><p id="p17391043548"><a name="p17391043548"></a><a name="p17391043548"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1182517371346"><td class="cellrowborder" valign="top" width="12.11757648470306%" headers="mcps1.2.7.1.1 "><p id="p194711119301"><a name="p194711119301"></a><a name="p194711119301"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="9.238152369526095%" headers="mcps1.2.7.1.2 "><p id="p347171173011"><a name="p347171173011"></a><a name="p347171173011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.647070585882824%" headers="mcps1.2.7.1.3 "><p id="p16471617309"><a name="p16471617309"></a><a name="p16471617309"></a>起点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="9.588082383523295%" headers="mcps1.2.7.1.4 "><p id="p11471616302"><a name="p11471616302"></a><a name="p11471616302"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="30.77384523095381%" headers="mcps1.2.7.1.5 "><p id="p1475111309"><a name="p1475111309"></a><a name="p1475111309"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”</p>
<p id="p104761143014"><a name="p104761143014"></a><a name="p104761143014"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="23.635272945410918%" headers="mcps1.2.7.1.6 "><p id="p9472163013"><a name="p9472163013"></a><a name="p9472163013"></a>-</p>
</td>
</tr>
<tr id="row482517371248"><td class="cellrowborder" valign="top" width="12.11757648470306%" headers="mcps1.2.7.1.1 "><p id="p3478123014"><a name="p3478123014"></a><a name="p3478123014"></a>targets</p>
</td>
<td class="cellrowborder" valign="top" width="9.238152369526095%" headers="mcps1.2.7.1.2 "><p id="p18474123014"><a name="p18474123014"></a><a name="p18474123014"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.647070585882824%" headers="mcps1.2.7.1.3 "><p id="p8471018308"><a name="p8471018308"></a><a name="p8471018308"></a>终点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="9.588082383523295%" headers="mcps1.2.7.1.4 "><p id="p7472173012"><a name="p7472173012"></a><a name="p7472173012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="30.77384523095381%" headers="mcps1.2.7.1.5 "><p id="p1947111183019"><a name="p1947111183019"></a><a name="p1947111183019"></a>标准csv格式，ID之间以英文逗号分隔，例如：“Alice,Nana”</p>
<p id="p34711113017"><a name="p34711113017"></a><a name="p34711113017"></a>个数不大于100000。</p>
</td>
<td class="cellrowborder" valign="top" width="23.635272945410918%" headers="mcps1.2.7.1.6 "><p id="p44720113013"><a name="p44720113013"></a><a name="p44720113013"></a>-</p>
</td>
</tr>
<tr id="row328172363914"><td class="cellrowborder" valign="top" width="12.11757648470306%" headers="mcps1.2.7.1.1 "><p id="p2481110302"><a name="p2481110302"></a><a name="p2481110302"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9.238152369526095%" headers="mcps1.2.7.1.2 "><p id="p144831123019"><a name="p144831123019"></a><a name="p144831123019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.647070585882824%" headers="mcps1.2.7.1.3 "><p id="p16481614309"><a name="p16481614309"></a><a name="p16481614309"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.588082383523295%" headers="mcps1.2.7.1.4 "><p id="p4489163012"><a name="p4489163012"></a><a name="p4489163012"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="30.77384523095381%" headers="mcps1.2.7.1.5 "><p id="p9485193018"><a name="p9485193018"></a><a name="p9485193018"></a>true 或false，布尔型。</p>
</td>
<td class="cellrowborder" valign="top" width="23.635272945410918%" headers="mcps1.2.7.1.6 "><p id="p1048318302"><a name="p1048318302"></a><a name="p1048318302"></a>false</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

当点的id中含有逗号时，需在此id上加上双引号，例如：电影Paris, je taime以及Alice两个id作为sources时，写做:"Paris, je taime",Alice"。

## 示例<a name="section923518617196"></a>

输入directed=true, sources= "Alice,Nana", targets= "Lily,Amy"  , JSON结果会展示在结果区。

