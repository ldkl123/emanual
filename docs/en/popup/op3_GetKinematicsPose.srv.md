---
layout: popup
---

- File: `online_walking_module_msgs/GetKinematicsPose.srv`

- Message Definition
 ```
 string    name
 ---
 op3_online_walking_module_msgs/KinematicsPose pose
 ```

- Description
This service acquires parameters that are applied on op3_online_walking_module.  

  - Request  
* ` string    name`   
&emsp;&emsp; group name (such as body, left_foot, right_foot)

  - Response
* `KinematicsPose pose`([op3_online_walking_module_msgs/KinematicsPose](op3_KinematicsPose.msg))     
&emsp;&emsp; For details, refer to [KinematicsPose.msg](op3_KinematicsPose.msg).

[&lt;&lt; Back](op3_online_walking_module_msgs.md)
