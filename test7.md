
## {{Name}}{{ADK\_GUID}} 
{{VisioDiagram\_VirtualMachine}} 
### Settings
The virtual machine {{Name}} has the following settings:

| Name | {{Name}}  |
| --- | --- |
| Operating System | {{VMImage.Offer}}  |
| Location | {{Location}}  |
| Size | {{VMSize}} <passthrough><ul><li><span>Number</span><span> </span><span>Of</span><span> </span><span>Cores</span><span> :</span><span> </span>{{VMSizeDetails.NumberOfCores}}</li><li><span>Memory</span><span> (</span><span>MB</span><span>): </span>{{VMSizeDetails.MemoryInMB}}</li><li><span>Max</span><span> </span><span>Data</span><span> </span><span>Disk</span><span> </span><span>Count</span><span>: </span>{{VMSizeDetails.MaxDataDiskCount}}</li><li><span>OS Disk Size (MB</span><span>) :</span><span> </span>{{VMSizeDetails.OsDiskSizeInMB}}</li><li><span>Resource Disk Size (MB</span><span>) :</span><span> </span>{{VMSizeDetails.ResourceDiskSizeInMB}}</li></ul></passthrough> |
| --- | --- |
| Availability Set | {{AvailabilitySetName}}  |
| Fault Domain | {{FaultDomain}}  |
| Update Domain | {{UpdateDomain}}  |
| State | {{PowerState}}  |
| Diagnostic Storage | {{DiagnosticStorage\_InternalLink}}  |
| Provisioning Date | {{ProvisioningDate}}  |
| Last Patch Date | {{LastPatchDate}}  |
| Resource Group | {{RG\_InternalLink}}  |
| Auto Update Status | {{AutoUpdateStatus}}  |


### Tags


| Tag Key | Tag Value |
| --- | --- |
{{#Tags}}| {{Key}}  | {{Value}}  |
{{/Tags}}
 
### Network interfaces

{{#MicrosoftNetworkInterfaces}}
#### {{Name}} 

##### Settings


| Name | {{Name}}  |
| --- | --- |
| Is primary | {{Primary}}  |
| Provisioning State | {{ProvisioningState}}  |
| Network Security Group | {{NSG\_InternalLink}}  |
| Enable IP Forwarding | {{EnableIPForwarding}}  |
| Location | {{Location}}  |
| Mac Address | {{MacAddress}}  |


##### Tags


| Tag Key | Tag Value |
| --- | --- |
{{#Tags}}| {{Key}}  | {{Value}}  |
{{/Tags}}

##### IP Configurations


| Public IP | Private IP | Subnet Name |
| --- | --- | --- |
{{#MicrosoftNetworkInterfacesIPConfiguration}}| {{PublicIP}}  | {{PrivateIPAddress}}  | {{Subnet.Name}}  |
{{/MicrosoftNetworkInterfacesIPConfiguration}}
 {{/MicrosoftNetworkInterfaces}}

### Load Balancers

{{#MicrosoftNetworkLoadBalancer}}
#### {{Name}}{{ADK\_GUID}} 

##### Settings


| Name | {{Name}}  |
| --- | --- |
| Location | {{Location}}  |
| Provisioning State | {{ProvisioningState}}  |


##### Inbound NAT Rules


| Name | Protocol | BackendPort | Front End Port | Enable Floating IP |
| --- | --- | --- | --- | --- |
{{#LBInboundNatRule}}| {{Name}}  | {{Protocol}}  | {{BackendPort}}  | {{FrontendPort}}  | {{EnableFloatingIP}}  |
{{/LBInboundNatRule}}

##### Inbound NAT Pools


| Name | Protocol | BackendPort | Front End Port Range Start | Front End Port Range End |
| --- | --- | --- | --- | --- |
{{#LBInboundNatPool}}| {{Name}}  | {{Protocol}}  | {{BackendPort}}  | {{FrontendPortRangeStart}}  | {{FrontendPortRangeEnd}}  |
{{/LBInboundNatPool}}
 
##### Tags


| Tag Key | Tag Value |
| --- | --- |
{{#Tags}}| {{Key}}  | {{Value}}  |
{{/Tags}}
{{/MicrosoftNetworkLoadBalancer}}

### Virtual Disks
The Virtual Machine is using the following disks
#### Data Hard Disks


| Name | VHD Uri | Size (GB) | Is Managed Disk | Host Caching |
| --- | --- | --- | --- | --- |
{{#MicrosoftComputeDataDisks}}| {{Name}}  | {{VHDUri}}  | {{DiskSizeGB}}  | {{IsManagedDisk}}  | {{Caching}}  |
{{/MicrosoftComputeDataDisks}}

#### OS Hard Disks


| Name | VHD Uri | Size (GB) | Is Managed Disk | Host Caching |
| --- | --- | --- | --- | --- |
{{#MicrosoftComputeOSDisks}}| {{Name}}  | {{VHDUri}}  | {{DiskSizeGB}}  | {{IsManagedDisk}}  | {{Caching}}  |
{{/MicrosoftComputeOSDisks}}

### Installed Softwares
 

| Name | Version | Publisher | Installation Date |
| --- | --- | --- | --- |
{{#InstalledSoftware}}| {{DisplayName}}  | {{DisplayVersion}}  | {{Publisher}}  | {{InstallDate}}  |
{{/InstalledSoftware}}

### Activated Features
 

| Feature Name |
| --- |
{{#ActivatedFeatures}}| {{Name}}  |
{{/ActivatedFeatures}}

### Startup Commands
 

| Name | Command |
| --- | --- |
{{#StartupCommands}}| {{Name}}  | {{Command}}  |
{{/StartupCommands}}

### Drives
 

| Letter | Volume Name | Size | Free Space |
| --- | --- | --- | --- |
{{#Drives}}| {{DeviceID}}  | {{VolumeName}}  | {{SizeDisplay}}  | {{FreeSpaceDisplay}}  |
{{/Drives}}

### Services
 

| Display Name | Start Mode | Status |
| --- | --- | --- |
{{#Services}}| {{DisplayName}}  | {{Started}}  | {{StartMode}}  |
{{/Services}}

### Metrics

#### Processor Time
{{Diagram\_ComputePercentageCPU\_removeifempty}} 
#### Available Bytes
{{Diagram\_ComputeAvailableMemory\_removeifempty}}  
### Role Assignments


| Principal Name | Role Name | Role Description | Type |
| --- | --- | --- | --- |
{{#RoleAssignments}}| {{PrincipalName}}  | {{RoleName}}  | {{RoleDescription}}  | {{RoleAssigmentType}}  |
{{/RoleAssignments}}

### Management Locks
The following management locks have been found: 

| Name | Type | Level | Notes |
| --- | --- | --- | --- |
{{#ManagementLocks}}| {{Name}}  | {{Type}}  | {{LockProperties.Level}}  | {{LockProperties.Notes}}  |
{{/ManagementLocks}}

### Changes
The following changes have been detected. 

| Name | Type | Change | Property Name | Previous Value | Current Value |
| --- | --- | --- | --- | --- | --- |
{{#Differences}}| {{DifferenceObjectName}}  | {{DifferenceObjectType}}  | {{DifferenceType}}  | {{PropertyName}}  | {{OldValue}}  | {{NewValue}}  |
{{/Differences}}
 
### Warnings
The following warnings have been detected in the virtual machine. 

| Criticity | Type | Description | s |
| --- | --- | --- | --- |
{{#Warnings}}| {{Criticity}}  | {{Type}}  | {{Description}}  | {{Message\_Hyperlink}}  |
{{/Warnings}}

### Billing
{{Diagram\_Billing\_removeifempty}} Total cost : {{ADK\_Price}}
