# How to Package Windows7

Windows 7 apps are supported in the [Win32 platform module](https://www.npmjs.com/package/pwabuilder-win32) for pwabuilder.

1. Make sure **pwabuilder** installed. If not, install using: 

`npm install -g pwabuilder`

2. Add **win32 platform** by: 

`pwabuilder platform add win32 pwabuilder-win32`

3. Then, use pwabuilder to generate the polyfills:

 `pwabuilder https://btdj.azurewebsites.net/ -d C:\Projects -l debug -p win32`. 