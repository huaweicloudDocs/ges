# 业务面API认证鉴权<a name="ges_03_0112"></a>

调用GES业务面API只能通过Token认证调用请求。

## Token认证<a name="section1265211312241"></a>

Token在计算机系统中代表令牌（临时）的意思，拥有Token就代表拥有某种权限。Token认证就是在调用API的时候将Token加到请求消息头，从而通过身份认证，获得操作API的权限。

Token可通过调用[获取用户Token](https://support.huaweicloud.com/api-iam/iam_30_0001.html)接口获取，调用本服务API需要project级别的Token，即调用[获取用户Token](https://support.huaweicloud.com/api-iam/iam_30_0001.html)接口时，请求body中auth.scope的取值需要选择project，如下所示。

```
{ 
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
                "name": "xxxxxxxx" 
            } 
        } 
    } 
}
```

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   Token的有效期为24小时，需要使用一个Token鉴权时，可以先缓存起来，避免频繁调用。
>-   GES服务必须通过project的方式来获取token，不支持scope为domain的方式。

获取Token后，再调用其他接口时，您需要在请求消息头中添加“X-Auth-Token”，其值即为Token。例如Token值为“ABCDEFJ....”，则调用接口时将“X-Auth-Token: ABCDEFJ....”加到请求消息头即可，如下所示。

```
GET https://iam.cn-north-1.myhuaweicloud.com/v3/auth/projects  
Content-Type: application/json 
X-Auth-Token: ABCDEFJ....
```

您还可以通过这个视频教程了解如何使用Token认证：[https://bbs.huaweicloud.com/videos/101333](https://bbs.huaweicloud.com/videos/101333)  。

