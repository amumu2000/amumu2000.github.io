1. 重启文件资源管理器
    ```shell
    taskkill /f /im explorer.exe ; start explorer.exe
    ```
2. 将右键菜单修改为win10风格
   ```shell
   reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
   ```
3. 将右键菜单还原为win10风格
   ```shell
   reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
   ```
4. 取消隐藏快捷方式lnk后缀
   ```shell
   reg delete HKCR\lnkfile /v NeverShowExt /f
   ```
5. 隐藏快捷方式lnk后缀
   ```shell
   reg add HKCR\lnkfile /v NeverShowExt /f
   ```