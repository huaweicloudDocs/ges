# GES自定义策略<a name="ges_01_0075"></a>

如果系统预置的GES权限，不满足您的授权要求，可以创建自定义策略。自定义策略中可以添加的授权项（Action）请参考[权限策略和授权项](https://support.huaweicloud.com/api-ges/ges_03_0148.html)。

目前华为云支持以下两种方式创建自定义策略：

-   可视化视图创建自定义策略：无需了解策略语法，按可视化视图导航栏选择云服务、操作、资源、条件等策略内容，可自动生成策略。
-   JSON视图创建自定义策略：可以在选择策略模板后，根据具体需求编辑策略内容；也可以直接在编辑框内编写JSON格式的策略内容。

具体创建步骤请参见：[创建自定义策略](https://support.huaweicloud.com/usermanual-iam/iam_01_0605.html)。本章为您介绍常用的GES自定义策略样例。

## GES自定义策略样例<a name="section1493518251395"></a>

-   示例1：授权用户拥有查询类权限、操作图权限

    ```
    { 
        "Version": "1.1", 
        "Statement": [ 
            { 
                "Effect": "Allow", 
                "Action": [ 
                         "ges:*:get*",
                         "ges:*:list*",
                         "ges:graph:operate"
                ] 
            } 
        ] 
    }
    ```

-   示例2：拒绝用户删除图

    拒绝策略需要同时配合其他策略使用，否则没有实际作用。用户被授予的策略中，一个授权项的作用如果同时存在Allow和Deny，则遵循Deny优先。

    如果您给用户授予GES FullAccess的系统策略，但不希望用户拥有GES FullAccess中定义的删除图权限，您可以创建一条拒绝删除独享集群的自定义策略，然后同时将GES FullAccess和拒绝策略授予用户，根据Deny优先原则，则用户可以对GES执行除了删除图外的所有操作。拒绝策略示例如下：

    ```
    { 
          "Version": "1.1", 
          "Statement": [ 
                { 
    		  "Effect": "Deny", 
                      "Action": [ 
                            "ges:graph:delete" 
                      ] 
                } 
          ] 
    }
    ```

-   示例3：授权用户操作图名称前缀为ges\_project的图（ges\_project名字不区分大小写），访问图列表。

    ```
    {
        "Version": "1.1",
        "Statement": [
            {
                "Effect": "Allow",
                "Action": [
                    "ges:graph:create",
                    "ges:graph:delete",
                    "ges:graph:access",
                    "ges:graph:getDetail"
                ],
                "Resource": [
                    "ges:*:*:graphName:ges_project*"
                ]
            },
            {
                "Effect": "Allow",
                "Action": [
                    "ges:graph:list"
                ]
            }
        ]
    }
    ```

-   示例4：授权用户操作部分图资源，查看所有资源。

    该策略分为两部分：

    -   第一部分：授权用户操作资源名称前缀为ges\_project的资源，资源包含图、元数据、备份。
    -   第二部分：授权用户查询图列表、查询备份列表、查询任务列表、查询元数据列表、校验元数据文件、查看job详情。

    ```
    {
        "Version": "1.1",
        "Statement": [
            {
                "Action": [
                    "ges:backup:delete",
                    "ges:graph:access",
                    "ges:metadata:create",
                    "ges:graph:operate",
                    "ges:graph:delete",
                    "ges:metadata:delete",
                    "ges:graph:create",
                    "ges:backup:create",
                    "ges:metadata:getDetail",
                    "ges:graph:getDetail"
                ],
                "Resource": [
                    "ges:*:*:backupName:ges_project*",
                    "ges:*:*:graphName:ges_project*",
                    "ges:*:*:metadataName:ges_project*"
                ],
                "Effect": "Allow"
            },
            {
                "Action": [
                    "ges:graph:list",
                    "ges:backup:list",
                    "ges:jobs:list",
                    "ges:metadata:list",
                    "ges:metadata:operate",
                    "ges:jobs:getDetail"
                ],
                "Effect": "Allow"
            }
        ]
    }
    ```


