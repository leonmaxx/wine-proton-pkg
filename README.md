# wine-proton-pkg
PKG packaging script for standalone WINE from [ValveSoftware/Proton](https://github.com/ValveSoftware/Proton/) repository.  
  
DXVK, DXVK-NVAPI, VKD3D-Proton and AMD FSR are integrated.  
Some of Proton and Steam support patches are removed.  
  
To use DXVK-NVAPI set environment variable `DXVK_ENABLE_NVAPI=1`.  
To use AMD FSR with full screen hack set environment variable `WINEFXFSR=1`.  
If you want to tune CAS sharpening level use `WINEFXCAS={level}`.  