# 业务面API构造请求<a name="ges_03_0121"></a>

-   [请求URI](#section1849899574)
-   [请求方法](#section1454211155819)
-   [请求消息头](#section25981138124716)
-   [请求消息体](#section14612192315587)

本节介绍GES业务面REST API请求的组成。

## 请求URI<a name="section1849899574"></a>

图引擎服务业务面API请求URI由如下部分组成。

**\{URI-scheme\} :// \{SERVER\_URL\} / \{resource-path\} ? \{query-string\}**

尽管请求URI包含在请求消息头中，但大多数语言或框架都要求您从请求消息中单独传递它，所以在此单独拿出来强调。

-   **URI-scheme**：表示用于传输请求的协议，当前所有API均采用**HTTPS**协议。
-   **SERVER\_URL**：图的访问地址，取值请参考[业务面API使用限制](业务面API使用限制.md)。
-   **resource-path**：资源路径，即API访问路径。从具体API的URI模块获取，例如“ges/v1.0/\{projectId\}/graphs/\{graphName\}/vertices/action?action\_id=query”。
-   **query-string**：查询参数，是可选部分，并不是每个API都有查询参数。查询参数前面需要带一个“？”，形式为“参数名=参数取值”，例如“limit=10”，表示查询不超过10条数据。

## 请求方法<a name="section1454211155819"></a>

HTTP请求方法（也称为操作或动词），可告知服务正在请求什么类型的操作。

-   **GET**：请求服务器返回指定资源。
-   **PUT**：请求服务器更新指定资源。
-   **POST**：请求服务器新增资源或执行特殊操作。
-   **DELETE**：请求服务器删除指定资源，如删除对象等。
-   **HEAD**：请求服务器资源头部。
-   **PATCH**：请求服务器更新资源的部分内容。当资源不存在的时候，PATCH可能会去创建一个新的资源。

## 请求消息头<a name="section25981138124716"></a>

附加请求消息头字段，如指定的URI和HTTP方法所要求的字段。例如，定义消息体类型的请求消息头“Content-Type”，请求鉴权信息等。

如下公共消息头需要添加到请求中。

**表 1**  公共请求消息头

<a name="d0e691"></a>
<table><thead align="left"><tr id="row43435224"><th class="cellrowborder" valign="top" width="18.411841184118412%" id="mcps1.2.5.1.1"><p id="p28592218"><a name="p28592218"></a><a name="p28592218"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="8.990899089908991%" id="mcps1.2.5.1.2"><p id="p11761112125318"><a name="p11761112125318"></a><a name="p11761112125318"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="31.24312431243124%" id="mcps1.2.5.1.3"><p id="p34268337"><a name="p34268337"></a><a name="p34268337"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="41.35413541354136%" id="mcps1.2.5.1.4"><p id="p19870205"><a name="p19870205"></a><a name="p19870205"></a>示例</p>
</th>
</tr>
</thead>
<tbody><tr id="row33821495"><td class="cellrowborder" valign="top" width="18.411841184118412%" headers="mcps1.2.5.1.1 "><p id="p55186561"><a name="p55186561"></a><a name="p55186561"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="8.990899089908991%" headers="mcps1.2.5.1.2 "><p id="p167626126538"><a name="p167626126538"></a><a name="p167626126538"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="31.24312431243124%" headers="mcps1.2.5.1.3 "><p id="p13565126104710"><a name="p13565126104710"></a><a name="p13565126104710"></a>消息体的类型（格式），默认取值为“application/json”，有其他取值时会在具体接口中专门说明。</p>
</td>
<td class="cellrowborder" valign="top" width="41.35413541354136%" headers="mcps1.2.5.1.4 "><p id="p16048387"><a name="p16048387"></a><a name="p16048387"></a>application/json</p>
</td>
</tr>
<tr id="row26328706"><td class="cellrowborder" valign="top" width="18.411841184118412%" headers="mcps1.2.5.1.1 "><p id="p52250442"><a name="p52250442"></a><a name="p52250442"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="8.990899089908991%" headers="mcps1.2.5.1.2 "><p id="p207626126535"><a name="p207626126535"></a><a name="p207626126535"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="31.24312431243124%" headers="mcps1.2.5.1.3 "><p id="p85652644714"><a name="p85652644714"></a><a name="p85652644714"></a>用户Token。例如，IAM用户Token也就是调用<a href="https://support.huaweicloud.com/api-iam/iam_30_0001.html" target="_blank" rel="noopener noreferrer">获取用户Token</a>接口的响应值，该接口是唯一不需要认证的接口。</p>
</td>
<td class="cellrowborder" valign="top" width="41.35413541354136%" headers="mcps1.2.5.1.4 "><p id="p45894015"><a name="p45894015"></a><a name="p45894015"></a>-</p>
</td>
</tr>
<tr id="row10392952"><td class="cellrowborder" valign="top" width="18.411841184118412%" headers="mcps1.2.5.1.1 "><p id="p36522766"><a name="p36522766"></a><a name="p36522766"></a>X-Language</p>
</td>
<td class="cellrowborder" valign="top" width="8.990899089908991%" headers="mcps1.2.5.1.2 "><p id="p15762181265317"><a name="p15762181265317"></a><a name="p15762181265317"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="31.24312431243124%" headers="mcps1.2.5.1.3 "><p id="p5554106"><a name="p5554106"></a><a name="p5554106"></a>请求语言，支持配置如下值：</p>
<a name="ul49986954"></a><a name="ul49986954"></a><ul id="ul49986954"><li>zh-cn：中文</li><li>en-us：英文</li></ul>
</td>
<td class="cellrowborder" valign="top" width="41.35413541354136%" headers="mcps1.2.5.1.4 "><p id="p6355195"><a name="p6355195"></a><a name="p6355195"></a>en-us</p>
</td>
</tr>
</tbody>
</table>

## 请求消息体<a name="section14612192315587"></a>

请求消息体通常以结构化格式发出，与请求消息头中Content-type对应，传递除请求消息头之外的内容。若请求消息体中参数支持中文，则中文字符必须为UTF-8编码。

每个接口的请求消息体内容不同，也并不是每个接口都需要有请求消息体（或者说消息体为空），GET、DELETE操作类型的接口就不需要消息体，消息体具体内容需要根据具体接口而定。

例如，对于IAM[获取用户Token](https://support.huaweicloud.com/api-iam/iam_30_0001.html)接口，您可以从接口的请求部分看到所需的请求参数及参数说明。将消息体加入后的请求如下所示，加粗的斜体字段需要根据实际值填写，其中**_username_**为用户名，**_domainname_**为用户所属的账号名称，**_\*\*\*\*\*\*\*\*_**为用户登录密码，**_xxxxxxxxxxxxxxxxxx_**为project的名称。例如cn-north-1，可以从[地区和终端节点](https://developer.huaweicloud.com/endpoint?all)中获取。

>![](public_sys-resources/icon-note.gif) **说明：** 
>scope参数定义了Token的作用域，下面示例中获取的Token仅能访问project下的资源。您还可以设置Token的作用域为某个账号下所有资源或账号的某个project下的资源，详细定义请参见IAM[获取用户Token](https://support.huaweicloud.com/api-iam/iam_30_0001.html)。

```
POST https: //iam.cn-north-1.myhuaweicloud.com/v3/auth/tokensContent-Type: application/json{
    "auth": {
        "identity": {
            "methods": [
                "password"
            ],
            "password": {
                "user": {
                    "name": "username",
                    "password": "********",
                    "domain": {
                        "name": "domainname"
                    }
                }
            }
        },
        "scope": {
            "project": {
                "name": "xxxxxxxxxxxxxxxxxx"
            }
        }
    }
}
```

到这里为止这个请求需要的内容就具备齐全了，您可以使用[curl](https://curl.haxx.se/)、[Postman](https://www.getpostman.com/)或直接编写代码等方式发送请求调用API。对于IAM[获取用户Token](https://support.huaweicloud.com/api-iam/iam_30_0001.html)接口，返回的响应消息头中“x-subject-token”就是需要获取的用户Token。有了Token之后，您就可以使用Token认证调用其他API。

