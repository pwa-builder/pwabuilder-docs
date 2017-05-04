# How to Package Windows7

At this time you can not build the Windows 7 app via the PWA Builder Web Site, so you'll need to build this app via the CLI tool.Windows 7 apps are supported in the [Win32 platform module](https://www.npmjs.com/package/pwabuilder-win32) for pwabuilder.

1. Make sure **pwabuilder** installed. If not, install using: 

`npm install -g pwabuilder`

2. Add **win32 platform** by: 

`pwabuilder platform add win32 pwabuilder-win32`

3. Then, use pwabuilder to generate the polyfills:

 `pwabuilder https://btdj.azurewebsites.net/ -d C:\Projects -l debug -p win32`. 

  Parameter |  Discription
 --- | --- 
 *-d* | the directory you would like to generate the app
 *-l* | the log level of the CLI
 *-p* | the platforms to build