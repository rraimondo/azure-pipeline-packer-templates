<img src="https://github.com/smctighevcp/Packer/blob/main/packer-icon.svg" style="width:50px;height:50px;">

# Azure Pipeline Packer Templates Examples
<img alt="Packer" src="https://img.shields.io/badge/Packer-1.7.0+-blue?style=for-the-badge&logo=packer">  <img alt="VMware vSphere 7.0 Update 2+" src="https://img.shields.io/badge/VMware%20vSphere-7.0%20Update%202+-blue?style=for-the-badge">

Contains example Packer configurations and Azure DevOps Pipeline YAML





## Structure
```
├── config
│   ├── windows
|   |   └── autounattend.pkrtpl.hcl
├── scripts
│   ├── windows
|   |   └── cleanup.ps1
|   |   └── initial-configuration.ps1
|   |   └── os-configuration.ps1
|   |   └── package-installations.ps1
├── vars
│   ├── windows-server-2019.pkrvars.hcl
│   ├── windows-server-2022.pkrvars.hcl
├── build.pkr.hcl
├── variables.pkr.hcl
```
