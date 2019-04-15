# 关联预测（Link Prediction）\(1.0.0\)<a name="ges_03_0088"></a>

**表 1**  parameters参数说明

<a name="table1583210523384"></a>
<table><thead align="left"><tr id="row14849155212385"><th class="cellrowborder" valign="top" width="14.85148514851485%" id="mcps1.2.7.1.1"><p id="p1385335233815"><a name="p1385335233815"></a><a name="p1385335233815"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.861386138613863%" id="mcps1.2.7.1.2"><p id="p28571452153816"><a name="p28571452153816"></a><a name="p28571452153816"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.623762376237625%" id="mcps1.2.7.1.3"><p id="p11861352173813"><a name="p11861352173813"></a><a name="p11861352173813"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="11.04950495049505%" id="mcps1.2.7.1.4"><p id="p10707182413348"><a name="p10707182413348"></a><a name="p10707182413348"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="20.792079207920793%" id="mcps1.2.7.1.5"><p id="p9866652183810"><a name="p9866652183810"></a><a name="p9866652183810"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.7.1.6"><p id="p81773216346"><a name="p81773216346"></a><a name="p81773216346"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1487205213384"><td class="cellrowborder" valign="top" width="14.85148514851485%" headers="mcps1.2.7.1.1 "><p id="p15878125233817"><a name="p15878125233817"></a><a name="p15878125233817"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p4884165218386"><a name="p4884165218386"></a><a name="p4884165218386"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21.623762376237625%" headers="mcps1.2.7.1.3 "><p id="p1988965273820"><a name="p1988965273820"></a><a name="p1988965273820"></a>输入起点ID。</p>
</td>
<td class="cellrowborder" valign="top" width="11.04950495049505%" headers="mcps1.2.7.1.4 "><p id="p178791739193412"><a name="p178791739193412"></a><a name="p178791739193412"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.2.7.1.5 "><p id="p1789385217383"><a name="p1789385217383"></a><a name="p1789385217383"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.6 "><p id="p217032123416"><a name="p217032123416"></a><a name="p217032123416"></a>-</p>
</td>
</tr>
<tr id="row889715527381"><td class="cellrowborder" valign="top" width="14.85148514851485%" headers="mcps1.2.7.1.1 "><p id="p890110527380"><a name="p890110527380"></a><a name="p890110527380"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.2 "><p id="p3904105243817"><a name="p3904105243817"></a><a name="p3904105243817"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21.623762376237625%" headers="mcps1.2.7.1.3 "><p id="p19095525380"><a name="p19095525380"></a><a name="p19095525380"></a>输入终点ID。</p>
</td>
<td class="cellrowborder" valign="top" width="11.04950495049505%" headers="mcps1.2.7.1.4 "><p id="p3885183933413"><a name="p3885183933413"></a><a name="p3885183933413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.2.7.1.5 "><p id="p15913752103813"><a name="p15913752103813"></a><a name="p15913752103813"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.6 "><p id="p8171332183414"><a name="p8171332183414"></a><a name="p8171332183414"></a>-</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table8100130114818"></a>
<table><thead align="left"><tr id="row11001100488"><th class="cellrowborder" valign="top" width="31.919999999999998%" id="mcps1.2.4.1.1"><p id="p101001205481"><a name="p101001205481"></a><a name="p101001205481"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.400000000000002%" id="mcps1.2.4.1.2"><p id="p81006017483"><a name="p81006017483"></a><a name="p81006017483"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.68%" id="mcps1.2.4.1.3"><p id="p131391531105817"><a name="p131391531105817"></a><a name="p131391531105817"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row101001074820"><td class="cellrowborder" valign="top" width="31.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p41001014483"><a name="p41001014483"></a><a name="p41001014483"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="23.400000000000002%" headers="mcps1.2.4.1.2 "><p id="p110012010481"><a name="p110012010481"></a><a name="p110012010481"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.68%" headers="mcps1.2.4.1.3 "><p id="p1313933155811"><a name="p1313933155811"></a><a name="p1313933155811"></a>起点ID</p>
</td>
</tr>
<tr id="row1610040114811"><td class="cellrowborder" valign="top" width="31.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p101009024814"><a name="p101009024814"></a><a name="p101009024814"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="23.400000000000002%" headers="mcps1.2.4.1.2 "><p id="p101002074820"><a name="p101002074820"></a><a name="p101002074820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.68%" headers="mcps1.2.4.1.3 "><p id="p101391031105812"><a name="p101391031105812"></a><a name="p101391031105812"></a>终点ID</p>
</td>
</tr>
<tr id="row7858131718584"><td class="cellrowborder" valign="top" width="31.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p9858151710588"><a name="p9858151710588"></a><a name="p9858151710588"></a>link_prediction</p>
</td>
<td class="cellrowborder" valign="top" width="23.400000000000002%" headers="mcps1.2.4.1.2 "><p id="p2858217145813"><a name="p2858217145813"></a><a name="p2858217145813"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="44.68%" headers="mcps1.2.4.1.3 "><p id="p158583179585"><a name="p158583179585"></a><a name="p158583179585"></a>关联预测结果</p>
</td>
</tr>
</tbody>
</table>

