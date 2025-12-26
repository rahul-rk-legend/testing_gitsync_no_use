# Playbook 1P Folder 1




**Enabled:** True

**Version:** 1

**Type:** Playbook

**Priority:** 2

**Playbook Simulator:** False


### Playbook Trigger
**Trigger Type:** All

**Conditions Operator:** And

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
||Equals||


### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Siemplify_Get Case Details_1|This action will get all the data from a case and return a JSON result.  The result includes comments, entity information, insights, playbooks that ran, alert information and events.|Siemplify|Get Case Details|
|Siemplify_Assign Case_1|Use the "Assign Case" action to assign the case to a user.|Siemplify|Assign Case|

### Involved Blocks
|Name|Description|
|----|-----------|
|Block 1P Folder 1|An embedded workflow that can receive inputs and return an output.|
