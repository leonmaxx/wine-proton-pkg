# wine-proton-pkg
PKG packaging script for standalone WINE from [ValveSoftware/Proton](https://github.com/ValveSoftware/Proton/) repository.  
  
Patches:  
* **User Shared Data** - required for some games (from wine-staging).  
* **Dll Redirect** - used for redirecting DirectX libraries (rebased to wine 4.11).  
* **Staging Tab** in Winecfg - here you can enable Gallium Nine, D9VK, DXVK.  
* Reverted patches that disabled `winemenubuilder` and crash reporting.  
  
Use [wine-proton-dxvk-pkg](https://github.com/leonmaxx/wine-proton-dxvk-pkg) to install D9VK and DXVK libs.
