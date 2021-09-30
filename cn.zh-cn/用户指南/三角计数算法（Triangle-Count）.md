# 三角计数算法（Triangle Count）<a name="ges_01_0041"></a>

## 概述<a name="section204471932366"></a>

三角计数算法（Triangle Count）统计图中三角形个数。三角形越多，代表图中节点关联程度越高，组织关系越严密。

## 适用场景<a name="section404680479376"></a>

三角计数算法（Triangle Count）适用于衡量图的结构特性场景。

## 参数说明<a name="section18154105319710"></a>

<a name="table111144815198"></a>
<table><thead align="left"><tr id="row19456482196"><th class="cellrowborder" valign="top" width="13.87138713871387%" id="mcps1.1.6.1.1"><p id="p1645348181915"><a name="p1645348181915"></a><a name="p1645348181915"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12.04120412041204%" id="mcps1.1.6.1.2"><p id="p8451948181914"><a name="p8451948181914"></a><a name="p8451948181914"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="34.49344934493449%" id="mcps1.1.6.1.3"><p id="p1145154851915"><a name="p1145154851915"></a><a name="p1145154851915"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="12.04120412041204%" id="mcps1.1.6.1.4"><p id="p64564810191"><a name="p64564810191"></a><a name="p64564810191"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="27.552755275527556%" id="mcps1.1.6.1.5"><p id="p54564851917"><a name="p54564851917"></a><a name="p54564851917"></a>取值范围</p>
</th>
</tr>
</thead>
<tbody><tr id="row1845248201910"><td class="cellrowborder" valign="top" width="13.87138713871387%" headers="mcps1.1.6.1.1 "><p id="p1345194801912"><a name="p1345194801912"></a><a name="p1345194801912"></a>statistics</p>
</td>
<td class="cellrowborder" valign="top" width="12.04120412041204%" headers="mcps1.1.6.1.2 "><p id="p11457486199"><a name="p11457486199"></a><a name="p11457486199"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="34.49344934493449%" headers="mcps1.1.6.1.3 "><p id="p345748111917"><a name="p345748111917"></a><a name="p345748111917"></a>是否仅输出总的统计量结果：</p>
<a name="ul1383201512204"></a><a name="ul1383201512204"></a><ul id="ul1383201512204"><li>true：仅输出总的统计数量。</li><li>false：输出各点对应三角形数量。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.04120412041204%" headers="mcps1.1.6.1.4 "><p id="p04514483198"><a name="p04514483198"></a><a name="p04514483198"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="27.552755275527556%" headers="mcps1.1.6.1.5 "><p id="p045184816199"><a name="p045184816199"></a><a name="p045184816199"></a>true或false，默认为true。</p>
</td>
</tr>
</tbody>
</table>

## 使用说明<a name="section11263351763"></a>

不考虑边的方向以及多边情况。

## 示例<a name="section9539286457"></a>

输入statistics= true, JSON结果会展示在查询结果区。

