# 创建用户并授权使用GES<a name="ges_01_0069"></a>

如果您需要对您所拥有的GES服务进行精细的权限管理，您可以使用[统一身份认证服务](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)（Identity and Access Management，简称IAM），通过IAM，您可以：

-   根据企业的业务组织，在您的华为云账号中，给企业中不同职能部门的员工创建IAM用户，让员工拥有唯一安全凭证，并使用GES资源。
-   根据企业用户的职能，设置不同的访问权限，以达到用户之间的权限隔离。
-   将GES资源委托给更专业、高效的其他华为云账号或者云服务，这些账号或者云服务可以根据权限进行代运维。

如果华为云账号已经能满足您的要求，不需要创建独立的IAM用户，您可以跳过本章节，不影响您使用GES服务的其它功能。

## 前提条件<a name="section3299192113013"></a>

-   “GES ReadOnlyAccess”属于策略，请先在IAM控制台中开通基于策略的访问控制公测，开通方法请参见：[申请基于策略的访问控制公测](https://support.huaweicloud.com/usermanual-iam/iam_01_019.html)。
-   给用户组授权之前，请您了解用户组可以添加的GES权限，并结合实际需求进行选择，GES支持的系统权限，请参见：[GES系统权限](GES系统权限.md)。若您需要对除GES之外的其它服务授权，IAM支持服务的所有权限请参见[权限策略](https://support.huaweicloud.com/permissions/policy_list.html?product=ges)。

## 示例流程<a name="section63665495717"></a>

本章节通过简单的用户组授权方法，将GES服务的策略授予用户组，并将用户添加至用户组中，从而使用户拥有对应的GES权限，操作流程如[图1](#fig4118155455715)所示。

**图 1**  给用户授权GES权限流程<a name="fig4118155455715"></a>  
![](figures/给用户授权GES权限流程.jpg "给用户授权GES权限流程")

1.  <a name="li1166368712"></a>[创建用户组并授权](https://support.huaweicloud.com/usermanual-iam/iam_03_0001.html)

    在IAM控制台创建用户组，并授予GES服务普通用户权限“GES ReadOnlyAccess”。

2.  [创建用户并加入用户组](https://support.huaweicloud.com/usermanual-iam/iam_02_0001.html)

    在IAM控制台创建用户，并将其加入[1](#li1166368712)中创建的用户组。

3.  [用户登录](https://support.huaweicloud.com/usermanual-iam/iam_01_0552.html)并验证权限

    使用新创建的用户登录控制台，切换至授权区域，验证权限：

    -   在“服务列表”中选择图引擎服务，进入GES主界面，单击右上角“创建图”，尝试创建一个新图，如果无法创建新图（假设当前权限仅包含GES ReadOnlyAccess），表示“GES ReadOnlyAccess”已生效。
    -   在“服务列表”中选择除图引擎服务外（假设当前策略仅包含GES ReadOnlyAccess）的任一服务，若提示权限不足，表示“GES ReadOnlyAccess”已生效。



