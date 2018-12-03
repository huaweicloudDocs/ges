# 业务面查询Job状态<a name="ges_03_0037"></a>

## 功能介绍<a name="section58484388201256"></a>

查询Job的执行状态。对点过滤查询、边过滤查询、执行算法等异步API，命令下发后，会返回jobId，通过jobId查询任务的执行状态。

## URI<a name="section20990726201256"></a>

-   URI 格式

    GET /ges/v1.0/\{projectId\}/graphs/\{graphName\}/jobs/\{jobId\}/status?offset=_offset_&limit=_limit_

-   参数说明

    **表 1**  URI参数说明

    <a name="table704858020149"></a>
    <table><thead align="left"><tr id="row2641929920149"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p48844757201436"><a name="p48844757201436"></a><a name="p48844757201436"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p64111224201436"><a name="p64111224201436"></a><a name="p64111224201436"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.8%" id="mcps1.2.5.1.3"><p id="p25626627201436"><a name="p25626627201436"></a><a name="p25626627201436"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.199999999999996%" id="mcps1.2.5.1.4"><p id="p62490911201436"><a name="p62490911201436"></a><a name="p62490911201436"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5069365220149"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p34819880201436"><a name="p34819880201436"></a><a name="p34819880201436"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1838054201436"><a name="p1838054201436"></a><a name="p1838054201436"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.3 "><p id="p14664660201436"><a name="p14664660201436"></a><a name="p14664660201436"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.5.1.4 "><p id="p46986778201436"><a name="p46986778201436"></a><a name="p46986778201436"></a>服务所在域ID。</p>
    </td>
    </tr>
    <tr id="row309032620149"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p27840876201436"><a name="p27840876201436"></a><a name="p27840876201436"></a>jobId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p40518487201436"><a name="p40518487201436"></a><a name="p40518487201436"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.3 "><p id="p60771990201436"><a name="p60771990201436"></a><a name="p60771990201436"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.5.1.4 "><p id="p23584146201436"><a name="p23584146201436"></a><a name="p23584146201436"></a>Job ID。</p>
    </td>
    </tr>
    <tr id="row5426698520149"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p12973251201436"><a name="p12973251201436"></a><a name="p12973251201436"></a>offset</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p44200405201436"><a name="p44200405201436"></a><a name="p44200405201436"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.3 "><p id="p23463039201436"><a name="p23463039201436"></a><a name="p23463039201436"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.5.1.4 "><p id="p21458026201436"><a name="p21458026201436"></a><a name="p21458026201436"></a>本次查询偏移量，默认为0。</p>
    </td>
    </tr>
    <tr id="row487557320149"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p6536110201436"><a name="p6536110201436"></a><a name="p6536110201436"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p59662897201436"><a name="p59662897201436"></a><a name="p59662897201436"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.3 "><p id="p856497201436"><a name="p856497201436"></a><a name="p856497201436"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.5.1.4 "><p id="p136632011564"><a name="p136632011564"></a><a name="p136632011564"></a>本次查询返回最大数量(最大100000)，默认为100000。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section6971305201256"></a>

-   请求样例

    ```
    GET http://Endpoint/ges/v1.0/{projectId}/graphs/{graphId}/jobs/{jobId}/status?offset=0&limit=2
    ```


## 响应<a name="section30236463201256"></a>

-   要素说明

    **表 2**  要素说明

    <a name="table22433401201626"></a>
    <table><thead align="left"><tr id="row46477880201626"><th class="cellrowborder" valign="top" width="22.18%" id="mcps1.2.5.1.1"><p id="p19101902201639"><a name="p19101902201639"></a><a name="p19101902201639"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.240000000000002%" id="mcps1.2.5.1.2"><p id="p3750257201639"><a name="p3750257201639"></a><a name="p3750257201639"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.05%" id="mcps1.2.5.1.3"><p id="p35335380201639"><a name="p35335380201639"></a><a name="p35335380201639"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="38.53%" id="mcps1.2.5.1.4"><p id="p43593503201639"><a name="p43593503201639"></a><a name="p43593503201639"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row58031533201626"><td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.5.1.1 "><p id="p66107279201639"><a name="p66107279201639"></a><a name="p66107279201639"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.240000000000002%" headers="mcps1.2.5.1.2 "><p id="p53089412201639"><a name="p53089412201639"></a><a name="p53089412201639"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.05%" headers="mcps1.2.5.1.3 "><p id="p5275138201639"><a name="p5275138201639"></a><a name="p5275138201639"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.53%" headers="mcps1.2.5.1.4 "><p id="p24633008201639"><a name="p24633008201639"></a><a name="p24633008201639"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row47668354201626"><td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.5.1.1 "><p id="p39396202201639"><a name="p39396202201639"></a><a name="p39396202201639"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.240000000000002%" headers="mcps1.2.5.1.2 "><p id="p36975784201639"><a name="p36975784201639"></a><a name="p36975784201639"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.05%" headers="mcps1.2.5.1.3 "><p id="p42248531201639"><a name="p42248531201639"></a><a name="p42248531201639"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.53%" headers="mcps1.2.5.1.4 "><p id="p66687826201639"><a name="p66687826201639"></a><a name="p66687826201639"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row61867570201626"><td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.5.1.1 "><p id="p28607870201639"><a name="p28607870201639"></a><a name="p28607870201639"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.240000000000002%" headers="mcps1.2.5.1.2 "><p id="p35536095201639"><a name="p35536095201639"></a><a name="p35536095201639"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.05%" headers="mcps1.2.5.1.3 "><p id="p59851441201639"><a name="p59851441201639"></a><a name="p59851441201639"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.53%" headers="mcps1.2.5.1.4 "><p id="p16128539201639"><a name="p16128539201639"></a><a name="p16128539201639"></a>查询成功时返回任务状态，可选值为waiting，running，complete。查询失败时字段为空。</p>
    </td>
    </tr>
    <tr id="row31360382201626"><td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.5.1.1 "><p id="p13654267201639"><a name="p13654267201639"></a><a name="p13654267201639"></a>data</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.240000000000002%" headers="mcps1.2.5.1.2 "><p id="p32253866201639"><a name="p32253866201639"></a><a name="p32253866201639"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.05%" headers="mcps1.2.5.1.3 "><p id="p62426349201639"><a name="p62426349201639"></a><a name="p62426349201639"></a>JSON</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.53%" headers="mcps1.2.5.1.4 "><p id="p23369517201639"><a name="p23369517201639"></a><a name="p23369517201639"></a>算法运行的结果。查询失败时字段为空。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   参数说明

    **表 3**  data参数说明

    <a name="table47512335201716"></a>
    <table><thead align="left"><tr id="row36430718201716"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p4871729120184"><a name="p4871729120184"></a><a name="p4871729120184"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.03%" id="mcps1.2.5.1.2"><p id="p5378648320184"><a name="p5378648320184"></a><a name="p5378648320184"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.97%" id="mcps1.2.5.1.3"><p id="p6173784320184"><a name="p6173784320184"></a><a name="p6173784320184"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p3470939620184"><a name="p3470939620184"></a><a name="p3470939620184"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row24176707201716"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p2797499920184"><a name="p2797499920184"></a><a name="p2797499920184"></a>vertices</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.2 "><p id="p5138247420184"><a name="p5138247420184"></a><a name="p5138247420184"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.3 "><p id="p123084520184"><a name="p123084520184"></a><a name="p123084520184"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p3258959220184"><a name="p3258959220184"></a><a name="p3258959220184"></a>点上关联的算法结果。</p>
    </td>
    </tr>
    <tr id="row6924880201716"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p127511220184"><a name="p127511220184"></a><a name="p127511220184"></a>edges</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.2 "><p id="p3617521520184"><a name="p3617521520184"></a><a name="p3617521520184"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.3 "><p id="p4451132320184"><a name="p4451132320184"></a><a name="p4451132320184"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p4864744420184"><a name="p4864744420184"></a><a name="p4864744420184"></a>边上关联的算法结果。</p>
    </td>
    </tr>
    <tr id="row56295548201716"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p3050689520184"><a name="p3050689520184"></a><a name="p3050689520184"></a>outputs</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.2 "><p id="p5513943020184"><a name="p5513943020184"></a><a name="p5513943020184"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.3 "><p id="p3710883720184"><a name="p3710883720184"></a><a name="p3710883720184"></a>JSON</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p5302584520184"><a name="p5302584520184"></a><a name="p5302584520184"></a>其他输出结果。</p>
    </td>
    </tr>
    <tr id="row30909938201716"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p113585520184"><a name="p113585520184"></a><a name="p113585520184"></a>data_return_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.2 "><p id="p2489539120184"><a name="p2489539120184"></a><a name="p2489539120184"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.3 "><p id="p326076320184"><a name="p326076320184"></a><a name="p326076320184"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p6279527620184"><a name="p6279527620184"></a><a name="p6279527620184"></a>本次查询返回结果数量。</p>
    </td>
    </tr>
    <tr id="row6828642201716"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p951166320184"><a name="p951166320184"></a><a name="p951166320184"></a>data_offset</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.2 "><p id="p3224725120184"><a name="p3224725120184"></a><a name="p3224725120184"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.3 "><p id="p6189050220184"><a name="p6189050220184"></a><a name="p6189050220184"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p4707480320184"><a name="p4707480320184"></a><a name="p4707480320184"></a>本次查询返回结果偏移量。</p>
    </td>
    </tr>
    <tr id="row64104516201716"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p2490214620184"><a name="p2490214620184"></a><a name="p2490214620184"></a>data_total_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.2 "><p id="p380793920184"><a name="p380793920184"></a><a name="p380793920184"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.3 "><p id="p4000760820184"><a name="p4000760820184"></a><a name="p4000760820184"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1939079320184"><a name="p1939079320184"></a><a name="p1939079320184"></a>异步任务产生的结果数据总量。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求成功样例

    ```
    Http Status Code: 200
    {
        "data": {
            "outputs": {
                "data_return_size": 2,
                "vertices": [
                    {
                        "id": "Sarah",
                        "label": "user",
                        "properties": {
                            "Occupation": [
                                "other or not specified"
                            ],
                            "ChineseName": [
                                "莎拉"
                            ],
                            "Zip-code": [
                                "55105"
                            ],
                            "Gender": [
                                "F"
                            ],
                            "Age": [
                                "18-24"
                            ]
                        }
                    },
                    {
                        "id": "Sidney",
                        "label": "user",
                        "properties": {
                            "Occupation": [
                                "writer"
                            ],
                            "ChineseName": [
                                "西德尼"
                            ],
                            "Zip-code": [
                                "85296"
                            ],
                            "Gender": [
                                "M"
                            ],
                            "Age": [
                                "18-24"
                            ]
                        }
                    }
                ],
                "data_offset": 0,
                "data_total_size": 19
             }
        },
        "status": "complete"
    }       
    ```

-   请求失败样例

    ```
    Http Status Code: 400
    {
       
    "errorMessage": "can not find job, jobId is  9440a7ebXXXXXXXXXXXXXXXXXXXX2d079a67001679122",
      
    "errorCode": "GES.8301"
    }
    ```


## 返回值<a name="section43583103201256"></a>

-   正常

    200

-   异常

    **表 4**  异常返回值说明

    <a name="table7140218185450"></a>
    <table><thead align="left"><tr id="row1329614185450"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p3495986518551"><a name="p3495986518551"></a><a name="p3495986518551"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p1317678318551"><a name="p1317678318551"></a><a name="p1317678318551"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row22356742185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1665962118551"><a name="p1665962118551"></a><a name="p1665962118551"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p725208518551"><a name="p725208518551"></a><a name="p725208518551"></a>请求错误。</p>
    </td>
    </tr>
    <tr id="row44828867185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5227908718551"><a name="p5227908718551"></a><a name="p5227908718551"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p674761518551"><a name="p674761518551"></a><a name="p674761518551"></a>鉴权失败。</p>
    </td>
    </tr>
    <tr id="row57737827185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p2006437818551"><a name="p2006437818551"></a><a name="p2006437818551"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1460190818551"><a name="p1460190818551"></a><a name="p1460190818551"></a>没有操作权限。</p>
    </td>
    </tr>
    <tr id="row29364829185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4159095618551"><a name="p4159095618551"></a><a name="p4159095618551"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1342429918551"><a name="p1342429918551"></a><a name="p1342429918551"></a>找不到资源。</p>
    </td>
    </tr>
    <tr id="row4978157185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5552901118551"><a name="p5552901118551"></a><a name="p5552901118551"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p155603218551"><a name="p155603218551"></a><a name="p155603218551"></a>服务内部错误。</p>
    </td>
    </tr>
    <tr id="row18376792185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p6060569918551"><a name="p6060569918551"></a><a name="p6060569918551"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1011455218551"><a name="p1011455218551"></a><a name="p1011455218551"></a>服务不可用。</p>
    </td>
    </tr>
    </tbody>
    </table>


