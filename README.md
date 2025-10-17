# gpu-drivers-ansible

An Ansible role for installing gpu drivers on RHEL 9 systems.

## Requirements

- Ansible 2.9 or higher
- RHEL 9 or compatible system
- Root privileges

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `nvidia_driver_repo_url` | `"https://developer.download.nvidia.com/compute/cuda/repos/rhel9/"` | NVIDIA repository URL |
| `nvidia_driver_module_version` | `"open-dkms"` | NVIDIA Driver module version to install |
| `nvidia_driver_install_cuda_drivers` | `true` | Whether to install CUDA drivers (cuda-drivers package) |
| `nvidia_driver_install_container_tools` | `true` | Whether to install container tools (and CDI config) |
| `nvidia_driver_install_management_library` | `true` | Whether to install management library (NVML) |
| `nvidia_driver_blacklist_nouveau` | `true` | Whether to blacklist nouveau driver |

## Example usage

See playbook.yaml
