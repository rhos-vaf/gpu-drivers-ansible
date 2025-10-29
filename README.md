# gpu-drivers-ansible

Ansible roles for installing gpu drivers on RHEL 9 systems.

## Requirements

- Ansible 2.9 or higher
- RHEL 9 or compatible system
- Root privileges

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `nvidia_driver_repo_url` | `"https://developer.download.nvidia.com/compute/cuda/repos/rhel9/"` | NVIDIA repository URL |
| `nvidia_driver_url` | "" | Install from a URL instead of a repo |
| `nvidia_driver_module_version` | `"open-dkms"` | NVIDIA Driver module version to install |
| `nvidia_driver_install_cuda_drivers` | `true` | Whether to install CUDA drivers (cuda-drivers package) |
| `nvidia_driver_install_container_tools` | `true` | Whether to install container tools (and CDI config) |
| `nvidia_driver_container_tools_version_release` | `1.17.8-1` | Version of the container tools to install |
| `nvidia_driver_generate_cdi_config` | `true` | Whether to generate the CDI config file |
| `nvidia_driver_install_management_library` | `true` | Whether to install management library (NVML) |
| `nvidia_driver_management_library_package_name` | `libnvidia-ml` | This package is called "nvidia-driver-NVML" in older versions |
| `nvidia_driver_blacklist_nouveau` | `true` | Whether to blacklist nouveau driver |

## Example usage

See playbook.yaml
