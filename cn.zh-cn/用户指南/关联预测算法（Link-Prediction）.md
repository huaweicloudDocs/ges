# 关联预测算法（Link Prediction）<a name="ges_01_0043"></a>

## 概述<a name="section204471932366"></a>

关联预测算法（Link Prediction）给定两个节点，根据Jaccard度量方法计算两个节点的相似程度，预测他们之间的紧密关系。

## 适用场景<a name="section6091138294734"></a>

关联预测算法（Link Prediction）适用于社交网上的好友推荐、关系预测等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  关联预测算法（Link Prediction）参数说明

<a name="table1583210523384"></a>
<table><thead align="left"><tr id="row14849155212385"><th class="cellrowborder" valign="top" width="14.85148514851485%" id="mcps1.2.7.1.1"><p id="p1385335233815"><a name="p1385335233815"></a><a name="p1385335233815"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.861386138613863%" id="mcps1.2.7.1.2"><p id="p28571452153816"><a name="p28571452153816"></a><a name="p28571452153816"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.782178217821784%" id="mcps1.2.7.1.3"><p id="p11861352173813"><a name="p11861352173813"></a><a name="p11861352173813"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="11.881188118811881%" id="mcps1.2.7.1.4"><p id="p10707182413348"><a name="p10707182413348"></a><a name="p10707182413348"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="19.801980198019802%" id="mcps1.2.7.1.5"><p id="p9866652183810"><a name="p9866652183810"></a><a name="p9866652183810"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.7.1.6"><p id="p81773216346"><a name="p81773216346"></a><a name="p81773216346"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1487205213384"><td class="cellrowborder" valign="top" width="14.85148514851485%" headers="mcps1.2.7.1.1 "><p id="p15878125233817"><a name="p15878125233817"></a><a name="p15878125233817"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p4884165218386"><a name="p4884165218386"></a><a name="p4884165218386"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.2.7.1.3 "><p id="p1988965273820"><a name="p1988965273820"></a><a name="p1988965273820"></a>输入起点ID</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.4 "><p id="p178791739193412"><a name="p178791739193412"></a><a name="p178791739193412"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.2.7.1.5 "><p id="p1789385217383"><a name="p1789385217383"></a><a name="p1789385217383"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.6 "><p id="p217032123416"><a name="p217032123416"></a><a name="p217032123416"></a>-</p>
</td>
</tr>
<tr id="row889715527381"><td class="cellrowborder" valign="top" width="14.85148514851485%" headers="mcps1.2.7.1.1 "><p id="p890110527380"><a name="p890110527380"></a><a name="p890110527380"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p3904105243817"><a name="p3904105243817"></a><a name="p3904105243817"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.2.7.1.3 "><p id="p19095525380"><a name="p19095525380"></a><a name="p19095525380"></a>输入终点ID</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.4 "><p id="p3885183933413"><a name="p3885183933413"></a><a name="p3885183933413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.2.7.1.5 "><p id="p15913752103813"><a name="p15913752103813"></a><a name="p15913752103813"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.6 "><p id="p8171332183414"><a name="p8171332183414"></a><a name="p8171332183414"></a>-</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section9539286457"></a>

输入参数source=Lee，target=Alice，计算两个节点之间的关联度，JSON结果会展示在查询结果区。

