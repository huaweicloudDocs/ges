# 带一般过滤条件最短路径（Filtered Shortest Path）<a name="ges_01_0080"></a>

## 概述<a name="section204471932366"></a>

带一般过滤条件最短路径算法（Filtered Shortest Path）寻找两点间满足过滤条件的最短路径，如有多条，返回任意一条最短路径。

## 适用场景<a name="section2555716895357"></a>

带一般过滤条件的最短路径算法（Filtered Shortest Path）适用于路径设计、网络规划等场景，通过对点边条件的过滤，控制最短路径的生成。

## 参数说明<a name="section18154105319710"></a>

**表 1**  带一般过滤条件最短路径算法（Filtered Shortest Path）参数说明

<a name="table17821619194012"></a>
<table><thead align="left"><tr id="row54821619124013"><th class="cellrowborder" valign="top" width="13.81%" id="mcps1.2.5.1.1"><p id="p9482619164019"><a name="p9482619164019"></a><a name="p9482619164019"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12.75%" id="mcps1.2.5.1.2"><p id="p64829198405"><a name="p64829198405"></a><a name="p64829198405"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10.86%" id="mcps1.2.5.1.3"><p id="p125411734205314"><a name="p125411734205314"></a><a name="p125411734205314"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="62.580000000000005%" id="mcps1.2.5.1.4"><p id="p24821019134018"><a name="p24821019134018"></a><a name="p24821019134018"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row64821819164014"><td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.5.1.1 "><p id="p1648331904019"><a name="p1648331904019"></a><a name="p1648331904019"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="12.75%" headers="mcps1.2.5.1.2 "><p id="p17483161910409"><a name="p17483161910409"></a><a name="p17483161910409"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.86%" headers="mcps1.2.5.1.3 "><p id="p668885655513"><a name="p668885655513"></a><a name="p668885655513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="62.580000000000005%" headers="mcps1.2.5.1.4 "><p id="p44831319164018"><a name="p44831319164018"></a><a name="p44831319164018"></a>输入路径的起点ID。</p>
</td>
</tr>
<tr id="row648311944016"><td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.5.1.1 "><p id="p94831119154017"><a name="p94831119154017"></a><a name="p94831119154017"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="12.75%" headers="mcps1.2.5.1.2 "><p id="p1948381994010"><a name="p1948381994010"></a><a name="p1948381994010"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.86%" headers="mcps1.2.5.1.3 "><p id="p7689756145514"><a name="p7689756145514"></a><a name="p7689756145514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="62.580000000000005%" headers="mcps1.2.5.1.4 "><p id="p18483151994016"><a name="p18483151994016"></a><a name="p18483151994016"></a>输入路径的终点ID。</p>
</td>
</tr>
<tr id="row5483919104014"><td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.5.1.1 "><p id="p154831619114017"><a name="p154831619114017"></a><a name="p154831619114017"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="12.75%" headers="mcps1.2.5.1.2 "><p id="p19483181944014"><a name="p19483181944014"></a><a name="p19483181944014"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10.86%" headers="mcps1.2.5.1.3 "><p id="p12689165695516"><a name="p12689165695516"></a><a name="p12689165695516"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="62.580000000000005%" headers="mcps1.2.5.1.4 "><p id="p1483161914015"><a name="p1483161914015"></a><a name="p1483161914015"></a>是否考虑边的方向。默认值为“false”。</p>
</td>
</tr>
</tbody>
</table>

## 注意事项<a name="section3956161017109"></a>

最短路径算法（Shortest Path）只返回一条最短路径。

