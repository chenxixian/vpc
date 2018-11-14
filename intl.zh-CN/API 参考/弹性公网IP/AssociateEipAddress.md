# AssociateEipAddress {#reference_i4w_xmt_ndb .reference}

将EIP绑定到同地域的云产品实例上。

调用该接口时，请注意：

-   只有Available状态的EIP才能够进行绑定操作。

-   一个EIP只能绑定一个云产品实例。


## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 AssociateEipAddress

 |
|AllocationId|String|是| EIP的ID。

 |
|InstanceType|String|否| 要绑定的云产品实例的类型，取值：

 -   EcsInstance（默认值）：VPC类型的ECS实例

只有处于运行中和已停止状态的ECS实例可以绑定EIP。

-   SlbInstance：VPC类型的SLB实例

绑定EIP后，负载均衡实例可以转发来自公网的请求。

-   Nat：NAT网关

如果NAT网关已购买了NAT带宽包，则无法绑定EIP。请提交工单进行处理。

-   HaVip：HAVIP

只有Available或者InUse状态的HaVip可以绑定EIP。


 每个ECS实例、负载均衡实例和HAVIP同时只能绑定一个EIP，NAT网关可以绑定多个EIP。

 |
|InstanceId|String|是| 云产品的实例ID。

 |

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=AssociateEipAddress
&AllocationId=eip-25877c70x
&InstanceId=i-25skktcp4
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <AssociateEipAddressResponse>
        <RequestId>0ED8D006-F706-4D23-88ED-E11ED28DCAC0</RequestId>
    </AssociateEipAddressResponse>
    ```

-   JSON格式

    ```
    { 
        "RequestId": "0ED8D006-F706-4D23-88ED-E11ED28DCAC0"
    }
    ```


