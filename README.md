<img src="https://user-images.githubusercontent.com/65562694/165377635-7e07394b-aa92-43f7-bbc2-c267d4e1863f.png" style="width:100px;height:100px;">    <img src="https://github.com/smctighevcp/Packer/blob/main/packer-icon.svg" style="width:100px;height:100px;">

# Azure Pipeline Packer Templates Examples
<img alt="Packer" src="https://img.shields.io/badge/Packer-1.7.0+-blue?style=for-the-badge&logo=packer">  <img alt="VMware vSphere 7.0 Update 2+" src="https://img.shields.io/badge/VMware%20vSphere-7.0%20Update%202+-blue?style=for-the-badge">

## Introduction

This repository contains example Packer configurations and Azure DevOps Pipeline YAML to orchestrate the provisioning of vSphere virtual machine templates.  For more information on how to utilise this check out my [blog post](https://stephanmctighe.com/*****)


## Available Builds
* Windows Server 2022 | Standard & Datacenter | Core & Desktop
* Windows Server 2019 | Standard & Datacenter | Core & Desktop

## Structure
```console
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

 ## Variables to Customise
 
 Values to change in `*.pkrvars.hcl`
 
 ```hcl
    vm_inst_os_kms_key_standard   = "<standard-kms-key>"
    vm_inst_os_kms_key_datacenter = "<datacenter-kms-key>"
    vm_guest_os_timezone          = "<time-zone>"
    vm_inst_os_iso_path           = "[<datastore-name>] /Media/windows_server_20XX.iso"
    vm_inst_vmtools_iso_path      = "[<datastore-name>] /Media/VMTools/windows.iso"
  ```
    
Values to change in `variables.pkr.hcl` (Change the value for the default parameter)

 ```hcl
    variable "default_vsphere_server"
    variable "default_vsphere_compute_cluster"
    variable "default_vsphere_datacenter"
    variable "default_vsphere_datastore"
    variable "default_vsphere_folder"
    variable "default_vsphere_portgroup_name"
    variable "default_content_library_destination"
  ```
