# 删除点label\(1.1.6\)<a name="ges_03_0100"></a>

## 功能介绍<a name="section47729112194146"></a>

删除点label。

## URI<a name="section32131610194146"></a>

-   URI格式

    ```
    DELETE /ges/v1.0/{projectId}/graphs/{graphName}/vertices/{vertexId}/labels/{labelName}
    ```


-   参数说明

    **表 1**  URI参数说明

    <a name="table5183729620297"></a>
    <table><thead align="left"><tr id="row6523211320297"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p27822115202917"><a name="p27822115202917"></a><a name="p27822115202917"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p38998823202917"><a name="p38998823202917"></a><a name="p38998823202917"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p4788088202917"><a name="p4788088202917"></a><a name="p4788088202917"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p52290813202917"><a name="p52290813202917"></a><a name="p52290813202917"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1546260920297"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p19512773202917"><a name="p19512773202917"></a><a name="p19512773202917"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p37030743202917"><a name="p37030743202917"></a><a name="p37030743202917"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p46700222202917"><a name="p46700222202917"></a><a name="p46700222202917"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p24621666202917"><a name="p24621666202917"></a><a name="p24621666202917"></a>项目编号，用于资源隔离。</p>
    </td>
    </tr>
    <tr id="row5685517820297"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p31128191202917"><a name="p31128191202917"></a><a name="p31128191202917"></a>graphName</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p38355577202917"><a name="p38355577202917"></a><a name="p38355577202917"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p19794060202917"><a name="p19794060202917"></a><a name="p19794060202917"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p59815007202917"><a name="p59815007202917"></a><a name="p59815007202917"></a>图名称。</p>
    </td>
    </tr>
    <tr id="row19437144817531"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1143714895312"><a name="p1143714895312"></a><a name="p1143714895312"></a>vertexId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p3437114816531"><a name="p3437114816531"></a><a name="p3437114816531"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p1437748165319"><a name="p1437748165319"></a><a name="p1437748165319"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p343734875312"><a name="p343734875312"></a><a name="p343734875312"></a>点名称。</p>
    </td>
    </tr>
    <tr id="row2361152107"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p3361815191013"><a name="p3361815191013"></a><a name="p3361815191013"></a>labelName</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1536615101012"><a name="p1536615101012"></a><a name="p1536615101012"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p14361215121014"><a name="p14361215121014"></a><a name="p14361215121014"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p63661511017"><a name="p63661511017"></a><a name="p63661511017"></a>点label。，</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section4280014194146"></a>

-   请求样例

    ```
    DELETE
    http://{SERVER_URL}/ges/v1.0/{projectId}/graphs/{graphName}/vertices/46/labels/movie
    ```


## 响应<a name="section3840388720054"></a>

-   要素说明

    **表 2**  要素说明

    <a name="table903063420229"></a>
    <table><thead align="left"><tr id="row2003346920229"><th class="cellrowborder" valign="top" width="13.750000000000002%" id="mcps1.2.5.1.1"><p id="p1916487320246"><a name="p1916487320246"></a><a name="p1916487320246"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="9.790000000000001%" id="mcps1.2.5.1.2"><p id="p885090020246"><a name="p885090020246"></a><a name="p885090020246"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.14%" id="mcps1.2.5.1.3"><p id="p4583431220246"><a name="p4583431220246"></a><a name="p4583431220246"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="65.32%" id="mcps1.2.5.1.4"><p id="p2159175520246"><a name="p2159175520246"></a><a name="p2159175520246"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row4144941520229"><td class="cellrowborder" valign="top" width="13.750000000000002%" headers="mcps1.2.5.1.1 "><p id="p6380778120246"><a name="p6380778120246"></a><a name="p6380778120246"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.2 "><p id="p104775420246"><a name="p104775420246"></a><a name="p104775420246"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.14%" headers="mcps1.2.5.1.3 "><p id="p1775926420246"><a name="p1775926420246"></a><a name="p1775926420246"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="65.32%" headers="mcps1.2.5.1.4 "><p id="p2921428620246"><a name="p2921428620246"></a><a name="p2921428620246"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row648389420229"><td class="cellrowborder" valign="top" width="13.750000000000002%" headers="mcps1.2.5.1.1 "><p id="p2370532520246"><a name="p2370532520246"></a><a name="p2370532520246"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.2 "><p id="p4108313520246"><a name="p4108313520246"></a><a name="p4108313520246"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.14%" headers="mcps1.2.5.1.3 "><p id="p3939965420246"><a name="p3939965420246"></a><a name="p3939965420246"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="65.32%" headers="mcps1.2.5.1.4 "><p id="p3725543420246"><a name="p3725543420246"></a><a name="p3725543420246"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row5242418520229"><td class="cellrowborder" valign="top" width="13.750000000000002%" headers="mcps1.2.5.1.1 "><p id="p4723069520246"><a name="p4723069520246"></a><a name="p4723069520246"></a>result</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.2 "><p id="p48112120246"><a name="p48112120246"></a><a name="p48112120246"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.14%" headers="mcps1.2.5.1.3 "><p id="p3897086820246"><a name="p3897086820246"></a><a name="p3897086820246"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="65.32%" headers="mcps1.2.5.1.4 "><p id="p252371920246"><a name="p252371920246"></a><a name="p252371920246"></a>成功时result值为success。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求成功样例

    ```
    Http Status Code: 200
    {
    }
    ```

-   请求失败样例

    ```
    Http Status Code: 400
     {
      "errorMessage": "Vertex [46] does not have label [movie]",
      "errorCode": "GES.8182"
     }
    ```


## 返回值<a name="section3657169620521"></a>

-   正常

    200

-   异常

**表 3**  异常返回值说明

<a name="table2812047420614"></a>
<table><thead align="left"><tr id="row3627919420614"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p46070382071"><a name="p46070382071"></a><a name="p46070382071"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p376257772071"><a name="p376257772071"></a><a name="p376257772071"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1713957020614"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p363220402071"><a name="p363220402071"></a><a name="p363220402071"></a>400 Bad Request</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p564041242071"><a name="p564041242071"></a><a name="p564041242071"></a>请求错误。</p>
</td>
</tr>
<tr id="row6629428120614"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p479822552071"><a name="p479822552071"></a><a name="p479822552071"></a>401 Unauthorized</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p613574802071"><a name="p613574802071"></a><a name="p613574802071"></a>鉴权失败。</p>
</td>
</tr>
<tr id="row542350320614"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p350999072071"><a name="p350999072071"></a><a name="p350999072071"></a>403 Forbidden</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p245202182071"><a name="p245202182071"></a><a name="p245202182071"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row552849520614"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p242813842071"><a name="p242813842071"></a><a name="p242813842071"></a>404 Not Found</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p206350632071"><a name="p206350632071"></a><a name="p206350632071"></a>找不到资源。</p>
</td>
</tr>
<tr id="row286211520635"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p105756432071"><a name="p105756432071"></a><a name="p105756432071"></a>500 Internal Server Error</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p513207162071"><a name="p513207162071"></a><a name="p513207162071"></a>服务内部错误。</p>
</td>
</tr>
<tr id="row3290567720639"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p331650242071"><a name="p331650242071"></a><a name="p331650242071"></a>503 Service Unavailable</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p20124622071"><a name="p20124622071"></a><a name="p20124622071"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

