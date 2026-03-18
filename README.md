# GitSync

## Integrations
|Name|Description|
|----|-----------|
|Google Chronicle|Google SecOps enables you to examine the aggregated security information for your enterprise going back for months or longer. Use Google SecOps to search across all of the domains accessed from within your enterprise. To enable the Google API client to communicate with the Backstory API you will need Google Developer Service Account Credential, https://developers.google.com/identity/protocols/OAuth2#serviceaccount.|
|Sample Integration|This is an educational integration designed to showcase the most common design patterns, when working with actions, connectors and jobs.|
|Silent Push|Silent Push integration.In case of any queries, please reach out to support@silentpush.com|


## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|Crowdstrike - Alerts Connector|Pull alerts from Crowdstrike. Dynamic List works with the "display_name" parameter. Note: To fetch identity protection detections use "Identity Protection Detections Connector".|True|
|Google Chronicle - Chronicle Alerts Connector|Pull information about Rule based alerts from Google Chronicle. Note: dynamic list is used for filtering purposes. For all of the details please visit the documentation portal.|True|
|Microsoft Sentinel Incident Tracking Connector|Connector works with Microsoft Azure Sentinel incidents and fetches updates to the Sentinel incidents as the new SecOps alerts. Connector's Dynamic List can be used to specify the incidents names that needs to be fetched. It is recommended to configure SecOps Alerts grouping based on SourceGroupIdentifier for this connector. See connector documentation for more information.|True|


## Playbooks
|Name|Description|
|----|-----------|
|Default 1||
|NGBlock||
|NGBlock1||
|NGP10||
|NGP6||
|NGP7||
|NGP8||
|NGP9||
|New Block|An embedded workflow that can receive inputs and return an output.|
|New Playbook||
|New Playbook 1||
|New Playbook 11||
|New Playbook 111||
|New Playbook NG||
|New Playbook NG1||
|New Playbook NG3||
|New Playbook NG5||
|New Playbook ng||
|New Playbook s3||
|Playbook 2||
|Playbook 4||
|Push Playbook Block 1|An embedded workflow that can receive inputs and return an output.|
|New Block 2|An embedded workflow that can receive inputs and return an output.|
|New Playbook 1||
|Push Playbook 1||
|New Playbook||
|Playbook 1||
|Playbook 3||
|Podman 1P 1||
|Playbook Podman2P||


## Visual Families
|Name|Description|
|----|-----------|
|Family Testing  1|Family Testing  1|
|Podman_1P_Visual_Families_100|Podman_1P_Visual_Families_100|
|Podman_1P_Visual_Families_87|Podman_1P_Visual_Families_87|
|Podman_1P_Visual_Families_89|Podman_1P_Visual_Families_89|


## Jobs
|Name|Description|
|----|-----------|
|Google Chronicle Alerts Creator Job|This job will sync new SOAR alerts with Chronicle SIEM.Note: This job is only supported from Chronicle SOAR version 6.2.30 and higher.|
|projects/project/locations/location/instances/instance/integrations/GoogleChronicle/jobs/1/jobInstances/5|This job will synchronize information about Chronicle SOAR Cases and Chronicle SOAR Alerts with Chronicle SIEM. Note: This job is only supported from Chronicle SOAR version 6.1.44 and higher.|
|projects/project/locations/location/instances/instance/integrations/GoogleChronicle/jobs/1/jobInstances/8|This job will synchronize information about Chronicle SOAR Cases and Chronicle SOAR Alerts with Chronicle SIEM. Note: This job is only supported from Chronicle SOAR version 6.1.44 and higher.|
|projects/project/locations/location/instances/instance/integrations/SampleIntegration/jobs/26/jobInstances/6|This is an example of a simple job. It has 2 functions: if a case has a tag "Closed", it will close the case from the job, if a case has a tag "Currency", it will add a comment to the case.|

