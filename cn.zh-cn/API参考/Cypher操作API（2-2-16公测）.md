# Cypher操作API（2.2.16公测）<a name="ges_03_0212"></a>

-   [功能介绍](#section11581657646)
-   [URL](#section1688218509514)
-   [请求](#section024212129238)
-   [响应](#section19473183810432)
-   [返回值](#section5966141394619)
-   [Cypher预置条件](#section96831823102810)
-   [基本操作](#section874721075619)
-   [Cypher实现的兼容性](#section1885065125812)

## 功能介绍<a name="section11581657646"></a>

Cypher是一种被广泛使用的声明式图数据库查询语言，使用Cypher语句可以查询GES中的数据，并返回结果。当前的Cypher实现中使用了图的统计信息，目前Cypher查询编译过程中使用了基于label的点边索引，如需正常使用Cypher，请先参考[labelDetails数据各要素说明](查询图概要信息(1-0-0).md#table1326183819100)构建点边索引。

## URL<a name="section1688218509514"></a>

-   URI 格式

    ```
    POST /ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=execute-cypher-query
    ```

-   参数说明

    **表 1**  URI参数说明

    <a name="table1810588194531"></a>
    <table><thead align="left"><tr id="row60039522194531"><th class="cellrowborder" valign="top" width="16.24%" id="mcps1.2.5.1.1"><p id="p17147315194548"><a name="p17147315194548"></a><a name="p17147315194548"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.139999999999999%" id="mcps1.2.5.1.2"><p id="p46755299194548"><a name="p46755299194548"></a><a name="p46755299194548"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.6%" id="mcps1.2.5.1.3"><p id="p29082892194548"><a name="p29082892194548"></a><a name="p29082892194548"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.019999999999996%" id="mcps1.2.5.1.4"><p id="p6904021194548"><a name="p6904021194548"></a><a name="p6904021194548"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row43054002194531"><td class="cellrowborder" valign="top" width="16.24%" headers="mcps1.2.5.1.1 "><p id="p65907560194548"><a name="p65907560194548"></a><a name="p65907560194548"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.139999999999999%" headers="mcps1.2.5.1.2 "><p id="p36912130194548"><a name="p36912130194548"></a><a name="p36912130194548"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.6%" headers="mcps1.2.5.1.3 "><p id="p37092573194548"><a name="p37092573194548"></a><a name="p37092573194548"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.019999999999996%" headers="mcps1.2.5.1.4 "><p id="p18457547124515"><a name="p18457547124515"></a><a name="p18457547124515"></a>项目编号，用于资源隔离。</p>
    </td>
    </tr>
    <tr id="row13142191315810"><td class="cellrowborder" valign="top" width="16.24%" headers="mcps1.2.5.1.1 "><p id="p1691521120589"><a name="p1691521120589"></a><a name="p1691521120589"></a>graphName</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.139999999999999%" headers="mcps1.2.5.1.2 "><p id="p791761175818"><a name="p791761175818"></a><a name="p791761175818"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.6%" headers="mcps1.2.5.1.3 "><p id="p492031115815"><a name="p492031115815"></a><a name="p492031115815"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.019999999999996%" headers="mcps1.2.5.1.4 "><p id="p145715471455"><a name="p145715471455"></a><a name="p145715471455"></a>图名称。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section024212129238"></a>

-   请求样例

```
POST http://{SERVER_URL}/ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=execute-cypher-query
{
       "statements": [{
              "statement": "match (n) return n limit 1",
              "parameters": {},
              "resultDataContents": ["row"]
       }]
}

```

-   参数说明

    **表 2**  Body参数说明

    <a name="table15122952104720"></a>
    <table><thead align="left"><tr id="row1411885215473"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p1118185244718"><a name="p1118185244718"></a><a name="p1118185244718"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.36%" id="mcps1.2.5.1.2"><p id="p1311825210479"><a name="p1311825210479"></a><a name="p1311825210479"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="15.27%" id="mcps1.2.5.1.3"><p id="p131181152144717"><a name="p131181152144717"></a><a name="p131181152144717"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="47.370000000000005%" id="mcps1.2.5.1.4"><p id="p11181052124718"><a name="p11181052124718"></a><a name="p11181052124718"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row111184522471"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p58331712490"><a name="p58331712490"></a><a name="p58331712490"></a>statements</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.36%" headers="mcps1.2.5.1.2 "><p id="p158331113492"><a name="p158331113492"></a><a name="p158331113492"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.27%" headers="mcps1.2.5.1.3 "><p id="p783341204917"><a name="p783341204917"></a><a name="p783341204917"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.370000000000005%" headers="mcps1.2.5.1.4 "><p id="p128341316492"><a name="p128341316492"></a><a name="p128341316492"></a>statements为一个语句组，包含一到多条语句。其中每个元素的格式如<a href="#table201251452114711">表 statement参数说明</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  statement参数说明

    <a name="table201251452114711"></a>
    <table><thead align="left"><tr id="row15123175211475"><th class="cellrowborder" valign="top" width="25.09%" id="mcps1.2.5.1.1"><p id="p712245274719"><a name="p712245274719"></a><a name="p712245274719"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.45%" id="mcps1.2.5.1.2"><p id="p12122552184712"><a name="p12122552184712"></a><a name="p12122552184712"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.33%" id="mcps1.2.5.1.3"><p id="p8122195217477"><a name="p8122195217477"></a><a name="p8122195217477"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.13%" id="mcps1.2.5.1.4"><p id="p2123152194714"><a name="p2123152194714"></a><a name="p2123152194714"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row0123205220479"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p1926816422511"><a name="p1926816422511"></a><a name="p1926816422511"></a>statement</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p1426816422515"><a name="p1426816422515"></a><a name="p1426816422515"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p6268204275113"><a name="p6268204275113"></a><a name="p6268204275113"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p426824255117"><a name="p426824255117"></a><a name="p426824255117"></a>Cypher语句。</p>
    </td>
    </tr>
    <tr id="row15125352194713"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p19268242175112"><a name="p19268242175112"></a><a name="p19268242175112"></a>parameters</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p15268134235113"><a name="p15268134235113"></a><a name="p15268134235113"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p5268942135117"><a name="p5268942135117"></a><a name="p5268942135117"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p82687426515"><a name="p82687426515"></a><a name="p82687426515"></a>Cypher语句参数，在进行参数化查询时使用，默认为空。</p>
    <p id="p68732762013"><a name="p68732762013"></a><a name="p68732762013"></a>如需使用，请参考<a href="#section1885065125812">参数化查询</a>。</p>
    </td>
    </tr>
    <tr id="row101300225512"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p72681442125113"><a name="p72681442125113"></a><a name="p72681442125113"></a>resultDataContents</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p1826844245119"><a name="p1826844245119"></a><a name="p1826844245119"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p4268114217515"><a name="p4268114217515"></a><a name="p4268114217515"></a>String或List</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p526884214511"><a name="p526884214511"></a><a name="p526884214511"></a>返回的结果样式，可选参数有“row”,”graph”两种样式可选，一次可返回多个样式。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应<a name="section19473183810432"></a>

-   要素说明

    **表 4**  要素说明

    <a name="table203335934319"></a>
    <table><thead align="left"><tr id="row173355919438"><th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.1"><p id="p1113351184419"><a name="p1113351184419"></a><a name="p1113351184419"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.24%" id="mcps1.2.5.1.2"><p id="p1513321118447"><a name="p1513321118447"></a><a name="p1513321118447"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.089999999999998%" id="mcps1.2.5.1.3"><p id="p1713331144415"><a name="p1713331144415"></a><a name="p1713331144415"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="59.28%" id="mcps1.2.5.1.4"><p id="p8134211204415"><a name="p8134211204415"></a><a name="p8134211204415"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row13336592434"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p104163220555"><a name="p104163220555"></a><a name="p104163220555"></a>results</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.5.1.2 "><p id="p154123215553"><a name="p154123215553"></a><a name="p154123215553"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.089999999999998%" headers="mcps1.2.5.1.3 "><p id="p144163219555"><a name="p144163219555"></a><a name="p144163219555"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.28%" headers="mcps1.2.5.1.4 "><p id="p11473218557"><a name="p11473218557"></a><a name="p11473218557"></a>一个List，每个元素是一条Cypher语句的返回结果。</p>
    </td>
    </tr>
    <tr id="row19331259104319"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p1941932185516"><a name="p1941932185516"></a><a name="p1941932185516"></a>errors</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.5.1.2 "><p id="p64113215557"><a name="p64113215557"></a><a name="p64113215557"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.089999999999998%" headers="mcps1.2.5.1.3 "><p id="p648328550"><a name="p648328550"></a><a name="p648328550"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.28%" headers="mcps1.2.5.1.4 "><p id="p15410322559"><a name="p15410322559"></a><a name="p15410322559"></a>一个List，每个元素包含字符串形式的code和message信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 5**  参数results中各要素说明

    <a name="table19909163265613"></a>
    <table><thead align="left"><tr id="row29101132195616"><th class="cellrowborder" valign="top" width="15.15%" id="mcps1.2.5.1.1"><p id="p16761113955713"><a name="p16761113955713"></a><a name="p16761113955713"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.479999999999999%" id="mcps1.2.5.1.2"><p id="p1761239125710"><a name="p1761239125710"></a><a name="p1761239125710"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.58%" id="mcps1.2.5.1.3"><p id="p1776118397573"><a name="p1776118397573"></a><a name="p1776118397573"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="58.79%" id="mcps1.2.5.1.4"><p id="p17761163914572"><a name="p17761163914572"></a><a name="p17761163914572"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1791073214563"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p17761123917573"><a name="p17761123917573"></a><a name="p17761123917573"></a>columns</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.479999999999999%" headers="mcps1.2.5.1.2 "><p id="p976133916574"><a name="p976133916574"></a><a name="p976133916574"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.58%" headers="mcps1.2.5.1.3 "><p id="p27611939165717"><a name="p27611939165717"></a><a name="p27611939165717"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.79%" headers="mcps1.2.5.1.4 "><p id="p16761183975714"><a name="p16761183975714"></a><a name="p16761183975714"></a>返回的字段名。</p>
    </td>
    </tr>
    <tr id="row1791019327563"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p4761139105714"><a name="p4761139105714"></a><a name="p4761139105714"></a>data</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.479999999999999%" headers="mcps1.2.5.1.2 "><p id="p37615393575"><a name="p37615393575"></a><a name="p37615393575"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.58%" headers="mcps1.2.5.1.3 "><p id="p576103975712"><a name="p576103975712"></a><a name="p576103975712"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.79%" headers="mcps1.2.5.1.4 "><p id="p27611039195719"><a name="p27611039195719"></a><a name="p27611039195719"></a>返回的数据值，每个元素代表一条记录。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 6**  参数data中各要素说明：

    <a name="table10759475586"></a>
    <table><thead align="left"><tr id="row07590765812"><th class="cellrowborder" valign="top" width="15.15%" id="mcps1.2.5.1.1"><p id="p3112733145811"><a name="p3112733145811"></a><a name="p3112733145811"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.61%" id="mcps1.2.5.1.2"><p id="p9112533125815"><a name="p9112533125815"></a><a name="p9112533125815"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.06%" id="mcps1.2.5.1.3"><p id="p41121033175814"><a name="p41121033175814"></a><a name="p41121033175814"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="58.18%" id="mcps1.2.5.1.4"><p id="p1112163375815"><a name="p1112163375815"></a><a name="p1112163375815"></a>含义</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row167609715814"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p1811203355819"><a name="p1811203355819"></a><a name="p1811203355819"></a>row</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.61%" headers="mcps1.2.5.1.2 "><p id="p4112193316581"><a name="p4112193316581"></a><a name="p4112193316581"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.06%" headers="mcps1.2.5.1.3 "><p id="p1711211336584"><a name="p1711211336584"></a><a name="p1711211336584"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.18%" headers="mcps1.2.5.1.4 "><p id="p61131733195818"><a name="p61131733195818"></a><a name="p61131733195818"></a>表示具体一行的内容，每个元素对应该行的一个字段，仅当resultDataContents为空或者包含“row”类型时显示。</p>
    </td>
    </tr>
    <tr id="row576011745813"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p1911373395814"><a name="p1911373395814"></a><a name="p1911373395814"></a>meta</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.61%" headers="mcps1.2.5.1.2 "><p id="p21131133135813"><a name="p21131133135813"></a><a name="p21131133135813"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.06%" headers="mcps1.2.5.1.3 "><p id="p1611353395815"><a name="p1611353395815"></a><a name="p1611353395815"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.18%" headers="mcps1.2.5.1.4 "><p id="p111131133175813"><a name="p111131133175813"></a><a name="p111131133175813"></a>表示该行每个字段的类型信息，仅当resultDataContents为空或者包含“row”类型时显示。</p>
    </td>
    </tr>
    <tr id="row9449831115819"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p411313315811"><a name="p411313315811"></a><a name="p411313315811"></a>graph</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.61%" headers="mcps1.2.5.1.2 "><p id="p4113433155811"><a name="p4113433155811"></a><a name="p4113433155811"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.06%" headers="mcps1.2.5.1.3 "><p id="p41131333185810"><a name="p41131333185810"></a><a name="p41131333185810"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.18%" headers="mcps1.2.5.1.4 "><p id="p211343310587"><a name="p211343310587"></a><a name="p211343310587"></a>以“graph”样式返回该行信息，仅当resultDataContents包含“graph”类型时显示。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求成功样例

    ```
    Http Status Code: 200
    {
        "results": [
            {
                "columns": ["n"],
                "data": [
                    {
                        "row": [
                            {
                                "occupation": "artist",
                                "gender": "F",
                                "Zip-code": "98133",
                                "userid": 0,
                                "age": "25-34"
                            }
                        ],
                        "meta": [
                            {
                                "id": "46",
                                "type": "node",
                                "labels": [
                                    "user"
                                ]
                            }
                        ]
                    }
                ]
            }
        ],
        "errors": []
    }
    
    ```

-   请求失败样例

    ```
    Http Status Code: 200
    {
        "results": [],
        "errors": [
            {
                "code": "GES.8904",
                "message": "Label index in vertices is not found."
            }
        ]
    }
    ```


## 返回值<a name="section5966141394619"></a>

-   正常

200

-   异常

<a name="table14278750194616"></a>
<table><thead align="left"><tr id="row83740507465"><th class="cellrowborder" colspan="2" valign="top" id="mcps1.1.3.1.1"><p id="p183751450184614"><a name="p183751450184614"></a><a name="p183751450184614"></a><strong id="b193757504468"><a name="b193757504468"></a><a name="b193757504468"></a>表1 </strong>异常返回值说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1737575074614"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p4375205044618"><a name="p4375205044618"></a><a name="p4375205044618"></a>返回值</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p73753507461"><a name="p73753507461"></a><a name="p73753507461"></a>说明</p>
</td>
</tr>
<tr id="row737519505469"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p137520504464"><a name="p137520504464"></a><a name="p137520504464"></a>400 Bad Request</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p153751350134617"><a name="p153751350134617"></a><a name="p153751350134617"></a>请求错误。</p>
</td>
</tr>
<tr id="row63755505463"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p1237516505467"><a name="p1237516505467"></a><a name="p1237516505467"></a>401 Unauthorized</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p537515034613"><a name="p537515034613"></a><a name="p537515034613"></a>鉴权失败。</p>
</td>
</tr>
<tr id="row9375750204613"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p19375125014619"><a name="p19375125014619"></a><a name="p19375125014619"></a>403 Forbidden</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p93751550104610"><a name="p93751550104610"></a><a name="p93751550104610"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row7375155017461"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p737545024614"><a name="p737545024614"></a><a name="p737545024614"></a>404 Not Found</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p1137520505466"><a name="p1137520505466"></a><a name="p1137520505466"></a>找不到资源。</p>
</td>
</tr>
<tr id="row637545034618"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p237520503468"><a name="p237520503468"></a><a name="p237520503468"></a>500 Internal Server Error</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p203751350204610"><a name="p203751350204610"></a><a name="p203751350204610"></a>服务内部错误。</p>
</td>
</tr>
<tr id="row143759503461"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p19376350104620"><a name="p19376350104620"></a><a name="p19376350104620"></a>503 Service Unavailable</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p0376125034618"><a name="p0376125034618"></a><a name="p0376125034618"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## Cypher预置条件<a name="section96831823102810"></a>

当前的Cypher查询编译过程中使用了基于label的点边索引，如需正常使用Cypher，请使用新建索引API构建索引，示例如下：

-   点label索引添加命令示例

    ```
    POST http://{SERVER_URL}/ges/v1.0/{projectId}/graphs/{graphName}/indices
    {
            "indexName": "cypher_vertex_index",
            "indexType": "GlobalCompositeVertexIndex",
            "hasLabel": "true",
            "indexProperty": []
    }
    ```

-   边label索引添加命令示例

    ```
    POST http://{SERVER_URL}/ges/v1.0/{projectId}/graphs/{graphName}/indices
    {
            "indexName": "cypher_edge_index",
            "indexType": "GlobalCompositeEdgeIndex",
            "hasLabel": "true",
            "indexProperty": []
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >1.  需要同时添加两个索引（点label索引和边label索引）才能正常使用Cypher查询。
    >2.  不需要构建的情况：如果图中已经存在hasLabel为true, indexProperty为空的点索引或边索引，则不需要重复构建。
    >3.  添加索引API为异步接口，查询索引是否添加成功，请使用[查询Job状态API](查询Job状态(1-0-0)-业务面.md)。


## 基本操作<a name="section874721075619"></a>

<a name="table17321759135613"></a>
<table><thead align="left"><tr id="row1233159145618"><th class="cellrowborder" valign="top" width="28.29%" id="mcps1.1.3.1.1"><p id="p1994174175712"><a name="p1994174175712"></a><a name="p1994174175712"></a>操作名</p>
</th>
<th class="cellrowborder" valign="top" width="71.71%" id="mcps1.1.3.1.2"><p id="p119419414571"><a name="p119419414571"></a><a name="p119419414571"></a>Cypher语句</p>
</th>
</tr>
</thead>
<tbody><tr id="row1533175915566"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p09484105718"><a name="p09484105718"></a><a name="p09484105718"></a>查点</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p159474155719"><a name="p159474155719"></a><a name="p159474155719"></a>match (n) return n</p>
</td>
</tr>
<tr id="row123345919560"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p13949415712"><a name="p13949415712"></a><a name="p13949415712"></a>查边</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p395114155710"><a name="p395114155710"></a><a name="p395114155710"></a>match (n)-[r]-&gt;(m) return n, m</p>
</td>
</tr>
<tr id="row1933159175610"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p17951544579"><a name="p17951544579"></a><a name="p17951544579"></a>查路径</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p995148576"><a name="p995148576"></a><a name="p995148576"></a>match (n:user)-[r]-&gt;(m:movie)--&gt;(s:series) return n,r,m,s</p>
</td>
</tr>
<tr id="row113345918561"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p39517475715"><a name="p39517475715"></a><a name="p39517475715"></a>过滤查询</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p16953410578"><a name="p16953410578"></a><a name="p16953410578"></a>match(n:user) where n.userid&gt;=5 return n</p>
</td>
</tr>
<tr id="row183475915565"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p69510411578"><a name="p69510411578"></a><a name="p69510411578"></a>分组聚集</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p89510417575"><a name="p89510417575"></a><a name="p89510417575"></a>match(n:movie) return n.genres, count(*)</p>
</td>
</tr>
<tr id="row23412595562"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p14958415579"><a name="p14958415579"></a><a name="p14958415579"></a>去重</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p10954495712"><a name="p10954495712"></a><a name="p10954495712"></a>match(n:movie) return distinct n.genres</p>
</td>
</tr>
<tr id="row1334125918564"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p179515419577"><a name="p179515419577"></a><a name="p179515419577"></a>排序</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p199584185718"><a name="p199584185718"></a><a name="p199584185718"></a>match(n:movie) return n order by n.movieid</p>
</td>
</tr>
<tr id="row53445914564"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p99517455720"><a name="p99517455720"></a><a name="p99517455720"></a>创建点</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p89515415576"><a name="p89515415576"></a><a name="p89515415576"></a>create (n:user{userid:1}) return n</p>
</td>
</tr>
<tr id="row13425911565"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p39574165719"><a name="p39574165719"></a><a name="p39574165719"></a>删除点</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p159516415717"><a name="p159516415717"></a><a name="p159516415717"></a>match (n:user{userid:1}) delete n</p>
</td>
</tr>
<tr id="row193416594565"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p15951246579"><a name="p15951246579"></a><a name="p15951246579"></a>更改标签</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p1951042576"><a name="p1951042576"></a><a name="p1951042576"></a>match (n:user{userid:1}) set n:movie return n</p>
</td>
</tr>
<tr id="row1034205925619"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p795441572"><a name="p795441572"></a><a name="p795441572"></a>更改属性</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p49518411571"><a name="p49518411571"></a><a name="p49518411571"></a>match (n:user{userid:1}) set n.userid=2 return n</p>
</td>
</tr>
</tbody>
</table>

## Cypher实现的兼容性<a name="section1885065125812"></a>

-   Cypher支持的子句列表

    Cypher实现了若干子句，通过对子句进行组合可以实现丰富的查询语义，进而完成点边过滤、多跳查询、排序去重、分组聚集等诸多能力。目前GES支持的Cypher子句如下：

    **表 7**  Cypher支持的子句清单

    <a name="table79051242012"></a>
    <table><thead align="left"><tr id="row290615421816"><th class="cellrowborder" valign="top" width="21.822182218221823%" id="mcps1.2.4.1.1"><p id="p4668102414215"><a name="p4668102414215"></a><a name="p4668102414215"></a>子句</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.001600160016004%" id="mcps1.2.4.1.2"><p id="p76683249217"><a name="p76683249217"></a><a name="p76683249217"></a>支持情况</p>
    </th>
    <th class="cellrowborder" valign="top" width="62.17621762176218%" id="mcps1.2.4.1.3"><p id="p17668162420220"><a name="p17668162420220"></a><a name="p17668162420220"></a>举例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row790604213111"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p16668624324"><a name="p16668624324"></a><a name="p16668624324"></a>match</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p966819241122"><a name="p966819241122"></a><a name="p966819241122"></a>部分支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p76684241827"><a name="p76684241827"></a><a name="p76684241827"></a>match (n:movie) return n</p>
    </td>
    </tr>
    <tr id="row179061842413"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p366813241921"><a name="p366813241921"></a><a name="p366813241921"></a>return</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p1366816242218"><a name="p1366816242218"></a><a name="p1366816242218"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p1666820242217"><a name="p1666820242217"></a><a name="p1666820242217"></a>return [1,2,3] as p</p>
    </td>
    </tr>
    <tr id="row89061042217"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p106681924625"><a name="p106681924625"></a><a name="p106681924625"></a>with</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p1466862419219"><a name="p1466862419219"></a><a name="p1466862419219"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p26697240211"><a name="p26697240211"></a><a name="p26697240211"></a>match (n) with labels(n) as label, count(*) as count</p>
    <p id="p76699241524"><a name="p76699241524"></a><a name="p76699241524"></a>where count &gt; 10 return *</p>
    </td>
    </tr>
    <tr id="row190613429112"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p18669324623"><a name="p18669324623"></a><a name="p18669324623"></a>where</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p176692242026"><a name="p176692242026"></a><a name="p176692242026"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p1466917241027"><a name="p1466917241027"></a><a name="p1466917241027"></a>match (n:movie) where n.movieid &gt; 10 return n</p>
    </td>
    </tr>
    <tr id="row890754210113"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p176692024623"><a name="p176692024623"></a><a name="p176692024623"></a>order by</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p206696241225"><a name="p206696241225"></a><a name="p206696241225"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p4669424723"><a name="p4669424723"></a><a name="p4669424723"></a>match (n:movie) return n order by n.genres</p>
    </td>
    </tr>
    <tr id="row59072422116"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p1166915248213"><a name="p1166915248213"></a><a name="p1166915248213"></a>skip</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p15669524221"><a name="p15669524221"></a><a name="p15669524221"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p76690241325"><a name="p76690241325"></a><a name="p76690241325"></a>match (n:movie) return n order by n.genres skip 5</p>
    </td>
    </tr>
    <tr id="row2090717429110"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p366922410214"><a name="p366922410214"></a><a name="p366922410214"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p14669624527"><a name="p14669624527"></a><a name="p14669624527"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p4669112416217"><a name="p4669112416217"></a><a name="p4669112416217"></a>match (n:movie) return n order by n.genres skip 5 limit 10</p>
    </td>
    </tr>
    <tr id="row690716421017"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p56691248214"><a name="p56691248214"></a><a name="p56691248214"></a>create</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p0669152416219"><a name="p0669152416219"></a><a name="p0669152416219"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p3669172410214"><a name="p3669172410214"></a><a name="p3669172410214"></a>create (n:user{_ID_: 'Jack' }) return n</p>
    </td>
    </tr>
    <tr id="row1990711421012"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p96691824727"><a name="p96691824727"></a><a name="p96691824727"></a>delete</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p13669102414212"><a name="p13669102414212"></a><a name="p13669102414212"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p186695241222"><a name="p186695241222"></a><a name="p186695241222"></a>match (n:movie)&lt;-[r]-(m:user) delete r</p>
    </td>
    </tr>
    <tr id="row5907194210112"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p19669132413219"><a name="p19669132413219"></a><a name="p19669132413219"></a>set</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p106691524924"><a name="p106691524924"></a><a name="p106691524924"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p6669524226"><a name="p6669524226"></a><a name="p6669524226"></a>match (n:user{userid:0}) set n.gender='M' return n</p>
    </td>
    </tr>
    <tr id="row139076421719"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p16691224123"><a name="p16691224123"></a><a name="p16691224123"></a>call procedures</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p366918249218"><a name="p366918249218"></a><a name="p366918249218"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p867011241023"><a name="p867011241023"></a><a name="p867011241023"></a>call db.schema()</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >1.  目前暂不支持union、merge、foreach、unwind、optional等操作，暂不支持使用Cypher语句增删索引，后续会逐渐开放支持。
    >2.  由于GES的元数据不是Schema Free的，点边label属性等有严格的限制，因此不支持Remove操作。
    >3.  对于限定范围的多跳查询（如match \(a\)-\[:\*3..5\]-\>\(b\)）和基于路径的点边创建（如Create p=\(a\)-\[r\]-\>\(b\) return p）等暂不提供支持。
    >4.  Order by子句不支持List类型的排序，当属性值的Cardinality不为single时，排序结果未知。

-   参数化查询支持

    Cypher支持参数化的查询。通过把查询语句中的数值、字符串等值类型提取为参数，加速查询的编译时间，提高查询速度。

    以下提供几种参数化查询的示例：

    -   参数化查询请求示例1：

        ```
        POST http://{SERVER_URL}/ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=execute-cypher-query
        {
                 "statements": [{
                           "statement": " match (n:user) where n.occupation = $occupation return n",
                           "parameters": {
                                 "occupation" : "artist"
                            },
                           "resultDataContents": ["row"]
                 }]
        }
        ```

    -   参数化查询请求示例2：

        ```
        POST http://{SERVER_URL}/ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=execute-cypher-query
        {
                 "statements": [{
                           "statement": " match (n:user {`Zip-code`:'98133'}) set n = $props return n",
                           "parameters": {
                                   "props": {
                                   "gender": "M",
                                   "age": "56+"
                                }
                            },
                           "resultDataContents": ["row"]
                 }]
        }
        ```


    >![](public_sys-resources/icon-note.gif) **说明：** 
    >参数化查询不适用于以下场景，下列查询语句均无法正常执行：
    >-   属性键值，如：match \(n\) where n.$param = 'something'
    >-   点边标签，如：match \(n:user\) set n:$code

-   数据类型支持

    GES目前支持char、char\_array、float、double、bool、long、Integer、date、enum、string共10种数据类型，布尔型和数值型在Cypher语法中都能得到支持，其他类型和Cypher存在如下的映射关系，在GES内部实现了类型的转换：

    **表 8**  GES和Cypher的类型映射关系

    <a name="table41064510414"></a>
    <table><thead align="left"><tr id="row410717554117"><th class="cellrowborder" valign="top" width="15.52155215521552%" id="mcps1.2.4.1.1"><p id="p8781151919414"><a name="p8781151919414"></a><a name="p8781151919414"></a>GES类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.33213321332133%" id="mcps1.2.4.1.2"><p id="p8781191913410"><a name="p8781191913410"></a><a name="p8781191913410"></a>Cypher类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="63.14631463146314%" id="mcps1.2.4.1.3"><p id="p87812199412"><a name="p87812199412"></a><a name="p87812199412"></a>备注</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1510717512414"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p2781191918419"><a name="p2781191918419"></a><a name="p2781191918419"></a>char</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p15781111924116"><a name="p15781111924116"></a><a name="p15781111924116"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p77814192415"><a name="p77814192415"></a><a name="p77814192415"></a>-</p>
    </td>
    </tr>
    <tr id="row121079510411"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p2781719154113"><a name="p2781719154113"></a><a name="p2781719154113"></a>char_array</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p36291023193119"><a name="p36291023193119"></a><a name="p36291023193119"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p10794161916415"><a name="p10794161916415"></a><a name="p10794161916415"></a>-</p>
    </td>
    </tr>
    <tr id="row121089511415"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p177811419194118"><a name="p177811419194118"></a><a name="p177811419194118"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p818353415315"><a name="p818353415315"></a><a name="p818353415315"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p179451934113"><a name="p179451934113"></a><a name="p179451934113"></a>-</p>
    </td>
    </tr>
    <tr id="row6108185184118"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p1378191974110"><a name="p1378191974110"></a><a name="p1378191974110"></a>enum</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p11781151904113"><a name="p11781151904113"></a><a name="p11781151904113"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p1778131934115"><a name="p1778131934115"></a><a name="p1778131934115"></a>由于Cypher语法中未提供枚举相关的语法，在Cypher查询时enum作为String进行输出，使用Cypher设置属性时对于不在枚举列表中的值会设置失败。</p>
    </td>
    </tr>
    <tr id="row151089594116"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p16781171917419"><a name="p16781171917419"></a><a name="p16781171917419"></a>date</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p07821192413"><a name="p07821192413"></a><a name="p07821192413"></a>Temporal</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p14782201974117"><a name="p14782201974117"></a><a name="p14782201974117"></a>目前支持Date按GES的日期格式输入和输出，暂不支持调用Cypher日期函数输入日期。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 9**  Cypher特殊类型支持情况

    <a name="table1962142294414"></a>
    <table><thead align="left"><tr id="row16621022104412"><th class="cellrowborder" valign="top" width="15.761576157615762%" id="mcps1.2.4.1.1"><p id="p569833418442"><a name="p569833418442"></a><a name="p569833418442"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.97209720972097%" id="mcps1.2.4.1.2"><p id="p2069803494415"><a name="p2069803494415"></a><a name="p2069803494415"></a>支持情况</p>
    </th>
    <th class="cellrowborder" valign="top" width="63.26632663266327%" id="mcps1.2.4.1.3"><p id="p17698203419447"><a name="p17698203419447"></a><a name="p17698203419447"></a>查询举例 &amp; 备注</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row362262224419"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p16698934104412"><a name="p16698934104412"></a><a name="p16698934104412"></a>Node</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.97209720972097%" headers="mcps1.2.4.1.2 "><p id="p369823404413"><a name="p369823404413"></a><a name="p369823404413"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.26632663266327%" headers="mcps1.2.4.1.3 "><p id="p46982346448"><a name="p46982346448"></a><a name="p46982346448"></a>match (n) return n limit 10</p>
    </td>
    </tr>
    <tr id="row16622122224415"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p1869818349442"><a name="p1869818349442"></a><a name="p1869818349442"></a>Relationship</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.97209720972097%" headers="mcps1.2.4.1.2 "><p id="p5698123412444"><a name="p5698123412444"></a><a name="p5698123412444"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.26632663266327%" headers="mcps1.2.4.1.3 "><p id="p15698123444418"><a name="p15698123444418"></a><a name="p15698123444418"></a>match (n)-[r]-&gt;(m) return r limit 10</p>
    </td>
    </tr>
    <tr id="row762252217444"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p76985348442"><a name="p76985348442"></a><a name="p76985348442"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.97209720972097%" headers="mcps1.2.4.1.2 "><p id="p136984342440"><a name="p136984342440"></a><a name="p136984342440"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.26632663266327%" headers="mcps1.2.4.1.3 "><p id="p569853412448"><a name="p569853412448"></a><a name="p569853412448"></a>return [1,2,3] as li</p>
    </td>
    </tr>
    <tr id="row56221622194410"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p569815344448"><a name="p569815344448"></a><a name="p569815344448"></a>Map</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.97209720972097%" headers="mcps1.2.4.1.2 "><p id="p1169853414448"><a name="p1169853414448"></a><a name="p1169853414448"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.26632663266327%" headers="mcps1.2.4.1.3 "><p id="p10698123411445"><a name="p10698123411445"></a><a name="p10698123411445"></a>match (n)--&gt;(m) return {start:id(n), end:id(m)}</p>
    </td>
    </tr>
    <tr id="row1062202234417"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p169811348445"><a name="p169811348445"></a><a name="p169811348445"></a>Path</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.97209720972097%" headers="mcps1.2.4.1.2 "><p id="p56981734114415"><a name="p56981734114415"></a><a name="p56981734114415"></a>暂不支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.26632663266327%" headers="mcps1.2.4.1.3 ">&nbsp;&nbsp;</td>
    </tr>
    <tr id="row16221922194416"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p469893415441"><a name="p469893415441"></a><a name="p469893415441"></a>Point、Spatial</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.97209720972097%" headers="mcps1.2.4.1.2 "><p id="p14698203414410"><a name="p14698203414410"></a><a name="p14698203414410"></a>暂不支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.26632663266327%" headers="mcps1.2.4.1.3 ">&nbsp;&nbsp;</td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >对[表 Cypher特殊类型支持情况](#table1962142294414)中提到的特殊类型，其中除了List用于匹配GES中的多值属性外，其他类型均无法通过set语句设为点边上某个属性的值。

-   表达式

    Cypher查询的where子句支持多种的表达式，可以组合成丰富的过滤条件，目前支持的表达式如下:

    <a name="table20406172153417"></a>
    <table><thead align="left"><tr id="row840652112342"><th class="cellrowborder" valign="top" width="23.522352235223522%" id="mcps1.1.4.1.1"><p id="p84021124133414"><a name="p84021124133414"></a><a name="p84021124133414"></a>运算类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.242024202420243%" id="mcps1.1.4.1.2"><p id="p640213244347"><a name="p640213244347"></a><a name="p640213244347"></a>表达式</p>
    </th>
    <th class="cellrowborder" valign="top" width="56.23562356235624%" id="mcps1.1.4.1.3"><p id="p040216246346"><a name="p040216246346"></a><a name="p040216246346"></a>举例&amp;备注</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row54067210343"><td class="cellrowborder" rowspan="3" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p94021124173420"><a name="p94021124173420"></a><a name="p94021124173420"></a>逻辑运算</p>
    <p id="p542272423418"><a name="p542272423418"></a><a name="p542272423418"></a></p>
    <p id="p154221124163413"><a name="p154221124163413"></a><a name="p154221124163413"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="20.242024202420243%" headers="mcps1.1.4.1.2 "><p id="p2403162443414"><a name="p2403162443414"></a><a name="p2403162443414"></a>and</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.23562356235624%" headers="mcps1.1.4.1.3 "><p id="p1040312453411"><a name="p1040312453411"></a><a name="p1040312453411"></a>match (n:user) where n.age='Under 18' and n.gender='F' return n</p>
    </td>
    </tr>
    <tr id="row10407172163412"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p5403524173416"><a name="p5403524173416"></a><a name="p5403524173416"></a>or</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1840392418345"><a name="p1840392418345"></a><a name="p1840392418345"></a>match(n:user) where n.`Zip-code`='22181' or n.userid=6 return n</p>
    </td>
    </tr>
    <tr id="row6407132112349"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1540372443418"><a name="p1540372443418"></a><a name="p1540372443418"></a>not</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p12403112483420"><a name="p12403112483420"></a><a name="p12403112483420"></a>match(n:movie) where not n.genres contains 'Drama' return n</p>
    </td>
    </tr>
    <tr id="row184076215343"><td class="cellrowborder" rowspan="2" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p12403132416348"><a name="p12403132416348"></a><a name="p12403132416348"></a>空值判断</p>
    <p id="p742117241340"><a name="p742117241340"></a><a name="p742117241340"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="20.242024202420243%" headers="mcps1.1.4.1.2 "><p id="p3403524133415"><a name="p3403524133415"></a><a name="p3403524133415"></a>is null</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.23562356235624%" headers="mcps1.1.4.1.3 "><p id="p44035247344"><a name="p44035247344"></a><a name="p44035247344"></a>match (n) where n.userid is null return n</p>
    </td>
    </tr>
    <tr id="row174076216347"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p8403924103416"><a name="p8403924103416"></a><a name="p8403924103416"></a>is not null</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p184037244342"><a name="p184037244342"></a><a name="p184037244342"></a>match (n) where n.userid is not null return n</p>
    </td>
    </tr>
    <tr id="row1407162173415"><td class="cellrowborder" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p24030242342"><a name="p24030242342"></a><a name="p24030242342"></a>比较运算</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.242024202420243%" headers="mcps1.1.4.1.2 "><p id="p1440312418348"><a name="p1440312418348"></a><a name="p1440312418348"></a>&gt;,&gt;=,&lt;,&lt;=,=,&lt;&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.23562356235624%" headers="mcps1.1.4.1.3 "><p id="p15403624163420"><a name="p15403624163420"></a><a name="p15403624163420"></a>match(n:user) where n.userid&gt;=5 return n</p>
    </td>
    </tr>
    <tr id="row240832117341"><td class="cellrowborder" rowspan="3" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p1840320246347"><a name="p1840320246347"></a><a name="p1840320246347"></a>字符串比较</p>
    <p id="p1542115249348"><a name="p1542115249348"></a><a name="p1542115249348"></a></p>
    <p id="p842192418349"><a name="p842192418349"></a><a name="p842192418349"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="20.242024202420243%" headers="mcps1.1.4.1.2 "><p id="p240342411342"><a name="p240342411342"></a><a name="p240342411342"></a>starts with</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.23562356235624%" headers="mcps1.1.4.1.3 "><p id="p8403132416347"><a name="p8403132416347"></a><a name="p8403132416347"></a>match(n:movie) where n.genres starts with 'Comedy' return n</p>
    </td>
    </tr>
    <tr id="row15408142113344"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p174031624153412"><a name="p174031624153412"></a><a name="p174031624153412"></a>ends with</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1340362473410"><a name="p1340362473410"></a><a name="p1340362473410"></a>match(n:movie) where n.genres ends with 'Drama' return n</p>
    </td>
    </tr>
    <tr id="row19408721143412"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p840311247347"><a name="p840311247347"></a><a name="p840311247347"></a>contains</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1440322414345"><a name="p1440322414345"></a><a name="p1440322414345"></a>match(n:movie) where n.genres contains 'Drama' return n</p>
    </td>
    </tr>
    <tr id="row19408142111340"><td class="cellrowborder" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p11405324143418"><a name="p11405324143418"></a><a name="p11405324143418"></a>List相关运算</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.242024202420243%" headers="mcps1.1.4.1.2 "><p id="p1140511246346"><a name="p1140511246346"></a><a name="p1140511246346"></a>in</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.23562356235624%" headers="mcps1.1.4.1.3 "><p id="p20405924173417"><a name="p20405924173417"></a><a name="p20405924173417"></a>match(n:student) where 'math' in n.courses return n</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >Cypher查询的where子句暂不支持case表达式、算数运算符、正则匹配等。

-   函数和过程

    -   函数

    在分组聚集、点边操作时，cypher支持一系列的函数，目前支持的函数如下所示：

    <a name="table199151027173910"></a>
    <table><thead align="left"><tr id="row591618275395"><th class="cellrowborder" valign="top" width="18.18181818181818%" id="mcps1.1.4.1.1"><p id="p145671949203910"><a name="p145671949203910"></a><a name="p145671949203910"></a>类别</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.392339233923394%" id="mcps1.1.4.1.2"><p id="p165675498391"><a name="p165675498391"></a><a name="p165675498391"></a>函数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="58.425842584258426%" id="mcps1.1.4.1.3"><p id="p14568204913917"><a name="p14568204913917"></a><a name="p14568204913917"></a>举例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row09162027203917"><td class="cellrowborder" rowspan="2" valign="top" width="18.18181818181818%" headers="mcps1.1.4.1.1 "><p id="p1256814953913"><a name="p1256814953913"></a><a name="p1256814953913"></a>聚集函数</p>
    <p id="p192775733913"><a name="p192775733913"></a><a name="p192775733913"></a></p>
    </td>
    <td class="cellrowborder" rowspan="2" valign="top" width="23.392339233923394%" headers="mcps1.1.4.1.2 "><p id="p16568144963919"><a name="p16568144963919"></a><a name="p16568144963919"></a>count</p>
    <p id="p5101125716396"><a name="p5101125716396"></a><a name="p5101125716396"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="58.425842584258426%" headers="mcps1.1.4.1.3 "><p id="p1568114918394"><a name="p1568114918394"></a><a name="p1568114918394"></a>match (n) return count(*)</p>
    </td>
    </tr>
    <tr id="row8916122703912"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1956819494395"><a name="p1956819494395"></a><a name="p1956819494395"></a>match (n) return count(n.userid)</p>
    </td>
    </tr>
    <tr id="row6917527183917"><td class="cellrowborder" rowspan="3" valign="top" width="18.18181818181818%" headers="mcps1.1.4.1.1 "><p id="p1156810498391"><a name="p1156810498391"></a><a name="p1156810498391"></a>一般函数</p>
    <p id="p6577149173918"><a name="p6577149173918"></a><a name="p6577149173918"></a></p>
    <p id="p105760491390"><a name="p105760491390"></a><a name="p105760491390"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="23.392339233923394%" headers="mcps1.1.4.1.2 "><p id="p156814917393"><a name="p156814917393"></a><a name="p156814917393"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.425842584258426%" headers="mcps1.1.4.1.3 "><p id="p1856894913918"><a name="p1856894913918"></a><a name="p1856894913918"></a>match (n) return id(n)</p>
    </td>
    </tr>
    <tr id="row209172027103918"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p12568124903911"><a name="p12568124903911"></a><a name="p12568124903911"></a>labels</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p656854916391"><a name="p656854916391"></a><a name="p656854916391"></a>match (n) return labels(n)</p>
    </td>
    </tr>
    <tr id="row20917627183910"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p135681849113911"><a name="p135681849113911"></a><a name="p135681849113911"></a>type</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p13917172713399"><a name="p13917172713399"></a><a name="p13917172713399"></a>match(n)-[r]-&gt;(m) return type(r)</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >avg\(\)、max\(\)、min\(\)等聚集函数，以及sin\(\)、cos\(\)等数学函数将在后续版本中陆续开放。

    -   过程

        目前GES 支持如下三个过程（Procedure）：

        <a name="table1866019378431"></a>
        <table><thead align="left"><tr id="row186611937124312"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p198491939104314"><a name="p198491939104314"></a><a name="p198491939104314"></a>名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p20849143914313"><a name="p20849143914313"></a><a name="p20849143914313"></a>语句</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row4661113754316"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p8849839164317"><a name="p8849839164317"></a><a name="p8849839164317"></a>获取图模式相关信息</p>
        </td>
        <td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p784912399436"><a name="p784912399436"></a><a name="p784912399436"></a>call db.schema()</p>
        </td>
        </tr>
        <tr id="row0661937154319"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p685013974317"><a name="p685013974317"></a><a name="p685013974317"></a>获取点label</p>
        </td>
        <td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p2850173984311"><a name="p2850173984311"></a><a name="p2850173984311"></a>call db.labels()</p>
        </td>
        </tr>
        <tr id="row5661173754317"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p1485053964314"><a name="p1485053964314"></a><a name="p1485053964314"></a>获取边label</p>
        </td>
        <td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p285083964314"><a name="p285083964314"></a><a name="p285083964314"></a>call db.relationshipTypes()</p>
        </td>
        </tr>
        </tbody>
        </table>


-   点id的兼容性
    -   Cypher添加点时不提供设置id的语法，GES中添加点需要一个字符串型的id，来唯一的标识一个点。为了兼容Cypher语法**，**当前Create语句实现中，通过使用一个特殊的标识符\_ID\_指定点的id。例如create \(n\{\_ID\_:’123456’\} \)语句，会创建一个id为’123456’的点。
    -   若创建时未指明id，则系统为此点生成一个随机id。

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >标识符“\_ID\_”仅在create语句中支持，match、set等子句均不支持\_ID\_标识。Match子句中可使用函数id\(\)获取点id。


-   添加边时的平行边处理策略：

    通过cypher添加边的时候，允许添加重复边，此处的重复边的定义为<源点，终点\>相同的两条边。


