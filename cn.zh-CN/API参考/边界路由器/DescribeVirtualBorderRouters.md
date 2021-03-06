# DescribeVirtualBorderRouters {#doc_api_1088690 .reference}

使用DescribeVirtualBorderRouters查询已创建的边界路由器（VBR）。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Vpc&api=DescribeVirtualBorderRouters)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeVirtualBorderRouters|要执行的操作。

 取值： **DescribeVirtualBorderRouters**。

 |
|RegionId|String|是|cn-shanghai|VBR所在的地域。 您可以通过调用[DescribeRegions](~~36063~~) 接口获取地域ID。

 |
|Filter.N.Key|String|否|1|第n个过滤器的类型。N取值：1-5

 |
|Filter.N.Value.N|RepeatList|否|1|第n个过滤器的第m个值。M取值：1-5

 |
|PageNumber|Integer|否|10|列表的页码，默认值为1。

 |
|PageSize|Integer|否|1|分页查询时每页的行数，最大值为50，默认值为10。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|VirtualBorderRouterSet| | |查询到的VBR合集，每个VBR的详细信息参见表 1 。

 |
|└AccessPointId|String|ap-cn-kojok19x3j0q6kx|物理专线接入点的ID。

 |
|└ActivationTime|String|2017-06-08T12:20:55|VBR第一次激活的时间。

 |
|└AssociatedCens| | |云企业网。

 |
|└CenId|String|cen-kojok19x3j0q6kx|云企业网实例的ID。

 |
|└CenOwnerId|Long|1086496381294461|云企业网实例所属账号的UID。

 |
|└CenStatus|String|Attached|云企业网状态。

 |
|└AssociatedPhysicalConnections| | |绑定的物理连接。

 |
|└CircuitCode|String|12|VBR专线侧接口对应运营商的电路编码。

 |
|└LocalGatewayIp|String|116.62.222.28|VBR专线侧接口本端的IP地址。

 |
|└PeerGatewayIp|String|116.62.222.28|VBR专线侧接口对端的IP地址。

 |
|└PeeringSubnetMask|String|255.255.255.252|实VBR专线侧接口本端与对端互联的子网掩码。

 |
|└PhysicalConnectionBusinessStatus|String|Normal|物理专线业务状态。

 |
|└PhysicalConnectionId|String|pc-119mfjzm7|物理专线ID。

 |
|└PhysicalConnectionOwnerUid|String|qfrgrgs|物理专线owner的UID。

 |
|└PhysicalConnectionStatus|String|Normal|物理专线状态。

 |
|└VlanId|String|0|VBR的VLAN ID。

 |
|└VlanInterfaceId|String|ri-kojok19x3j0q6kx|虚拟边界路由器（VBR）专线侧接口（RouterInterface）的ID。可以用来做VBR上路由的下一跳。

 |
|└CircuitCode|String|longtel001|运营商为物理专线提供的电路编码。

 |
|└CreationTime|String|2017-06-08T12:20:55|VBR的创建时间。

 |
|└Description|String|VBR|VBR的描述信息。

 |
|└LocalGatewayIp|String|116.62.222.28|阿里云侧互联IP。

 |
|└Name|String|test|VBR的名称。

 |
|└PeerGatewayIp|String|116.62.222.28|客户侧互联IP。

 |
|└PeeringSubnetMask|String|255.255.255.252|阿里云侧互联IP和客户侧互联IP的子网掩码。

 |
|└PhysicalConnectionBusinessStatus|String|Normal|物理专线业务状态。

 |
|└PhysicalConnectionId|String|pc-119mfjzm7|VBR所属的物理专线的ID。

 |
|└PhysicalConnectionOwnerUid|String|usdgbh123fvgf|物理专线owner的UID。

 |
|└PhysicalConnectionStatus|String|Normal|物理专线状态。

 |
|└RecoveryTime|String|2017-06-08T12:20:55|VBR最近一次从Terminated状态恢复到Active状态的时间。

 |
|└RouteTableId|String|rtb-bp1nxxxxxxxxxxxxxxxx|VBR的路由表的ID。

 |
|└Status|String|active|物理专线状态：

 -   Initial：申请中
-   Approved：审批通过
-   Allocating：正在分配资源
-   Allocated：接入施工中。
-   Confirmed：等待用户确认
-   Enabled：已开通
-   Rejected：申请被拒绝
-   Canceled：已取消
-   Allocation Failed：资源分配失败
-   Terminated：已终止

 |
|└TerminationTime|String|2017-06-08T12:20:55|VBR最近一次被终止的时间。

 |
|└VbrId|String|vbr-kojok19x3j0q6kx|VBR的ID。

 |
|└VlanId|Integer|10|VBR的VLAN ID。

 |
|└VlanInterfaceId|String|ri-2zeo3xzyf38r4urzdpvfs|VBR的路由器接口的ID。

 |
|TotalCount|Integer|10|列表条条目数。

 |
|PageNumber|Integer|10|当前页码。

 |
|PageSize|Integer|10|每页包含多少条目。

 |
|RequestId|String|DE77A7F3-3B74-41C0-A5BC-CAFD188C28B6|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://vpc.aliyuncs.com/?Action=DescribeVirtualBorderRouters
&RegionId=cn-shanghai
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeVirtualBorderRoutersResponse>
  <RequestId>AE65530E-8436-4FB1-8217-DCD35712AC89</RequestId>
  <PageNumber>1</PageNumber>
  <VirtualBorderRouterSet>
    <VirtualBorderRouterType>
      <LocalGatewayIp>10.1.1.1</LocalGatewayIp>
      <PeerGatewayIp>10.2.2.2</PeerGatewayIp>
      <Description/>
      <PhysicalConnectionOwnerUid>123157908XXXXXXXX</PhysicalConnectionOwnerUid>
      <VlanId>10</VlanId>
      <RecoveryTime/>
      <PhysicalConnectionStatus>Enabled</PhysicalConnectionStatus>
      <PhysicalConnectionId>pc-2zeoaxkq3jot5pXXXXXy</PhysicalConnectionId>
      <RouteTableId>vtb-2ze9hmd6yofwvb1dd79j9</RouteTableId>
      <PeeringSubnetMask>255.0.0.0</PeeringSubnetMask>
      <TerminationTime/>
      <Name/>
      <CreationTime>2018-03-06T11:16:34Z</CreationTime>
      <ActivationTime>2018-03-06T11:16:34Z</ActivationTime>
      <CircuitCode/>
      <Status>active</Status>
      <PhysicalConnectionBusinessStatus>Normal</PhysicalConnectionBusinessStatus>
      <VlanInterfaceId>ri-2zeum6rgu0586gjrocikm</VlanInterfaceId>
      <AccessPointId>ap-cn-beijing-dx-A</AccessPointId>
      <VbrId>vbr-2zecmmvg5gvu8XXXXw</VbrId>
    </VirtualBorderRouterType>
  </VirtualBorderRouterSet>
  <TotalCount>1</TotalCount>
  <PageSize>10</PageSize>
</DescribeVirtualBorderRoutersResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"DescribeVirtualBorderRoutersResponse":{
		"PageNumber":"1",
		"VirtualBorderRouterSet":{
			"VirtualBorderRouterType":{
				"LocalGatewayIp":"10.1.1.1",
				"PeerGatewayIp":"10.2.2.2",
				"PhysicalConnectionOwnerUid":"123157908XXXXXXXX",
				"VlanId":"10",
				"PhysicalConnectionStatus":"Enabled",
				"PhysicalConnectionId":"pc-2zeoaxkq3jot5p7XXXXy",
				"RouteTableId":"vtb-2ze9hmd6yofwvb1dd79j9",
				"PeeringSubnetMask":"255.0.0.0",
				"CreationTime":"2018-03-06T11:16:34Z",
				"ActivationTime":"2018-03-06T11:16:34Z",
				"Status":"active",
				"PhysicalConnectionBusinessStatus":"Normal",
				"VlanInterfaceId":"ri-2zeum6rgu0586gjrocikm",
				"VbrId":"vbr-2zecmmvg5gvu8i4XXX",
				"AccessPointId":"ap-cn-beijing-dx-A"
			}
		},
		"TotalCount":"1",
		"PageSize":"10",
		"RequestId":"AE65530E-8436-4FB1-8217-DCD35712AC89"
	}
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidFilterKey.ValueNotSupported|Specified filter key is not supported: Filter.X.key|该过滤器的Key不支持：Filter.X.key|

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

