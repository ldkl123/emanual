---
layout: popup
---

- File: `thormang3_walking_module_msgs/SetDampingBalanceParam.srv`


- Message Definition
 ```
 float32             updating_duration
 DampingBalanceParam balance_param
 ---
 int32 result
 ```

- Description
A service that can modify Balance Algorithm Parameter.

  - Request
* ` float32      updating_duration`
&emsp;&emsp; Time duration when updating Balance Parameter.
&emsp;&emsp; The Parameter is gradually updated based on configured time.
&emsp;&emsp; 0 or negative value will update the Balance Parameter immediately.

* `DampingBalanceParam balance_param`([thormang3_walking_module_msgs/DampingBalanceParam](DampingBalanceParam.msg))
&emsp;&emsp; The Balance Parameter to be applied

  - Response
* ` int32 result`
&emsp;&emsp; Result of the "SetDampingBalanceParam" Service

| Name                           | Value | Description                                   |
|--------------------------------|-------|-----------------------------------------------|
| NO_ERROR                       | 0x00  | There is no error.                            |
| NOT_ENABLED_WALKING_MODULE     | 0x02  | The thormang3_walking_module is not enabled.  |
| PREV_REQUEST_IS_NOT_FINISHED   | 0x20  | The previous request is not finished.         |
| TIME_CONST_IS_ZERO_OR_NEGATIVE | 0x40  | One or some time constant is zero or negative |


<br>
[[&lt;&lt; Back|thormang3_walking_module_msgs]]
