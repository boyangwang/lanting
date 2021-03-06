# SingleFile Companion
SingleFile Companion is a program that runs outside the browser. It:
 - makes the saving process more transparent when the auto-save is active in SingleFile,  
 - allows you to save pages in another directory than the download directory,
 - saves pages in an anonymous session in a separate browser.
 
 It uses the [Native Messaging API](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Native_messaging) to communicate with SingleFile.

## Install

 - Install [SingleFile CLI](https://github.com/gildas-lormeau/SingleFile/tree/master/cli)

 - In the `companion` folder of SingleFile, go into the subfolder corresponding to your OS and your browser. For example, if you use Chome on Windows:

`cd companion`

`cd win`

`cd chrome`

 - Make `install.sh` executable (Linux/Unix/BSD etc.).

`chmod +x install.sh`

 - Run `install`

`./install.sh` (Linux/Unix/BSD etc.)

`install.bat` (Windows)

 - Enable the option `Misc. > save the page with SingleFile Companion` in SingleFile

## Options

The `options.json` file allows configuring SingleFile Companion. Here are the entries you can edit:
 - `savePath`: path where to save files (default: `SingleFile/companion` path)
 - `backEnd`: backend used to save the page (default: `"puppeteer"`)
 - `errorFile`: path of the file where errors are stored (default: `undefined`)
 - `browserHeadless`: whether the browser is launched in headless mode (default: `true`)
 - `browserDebug`: whether the browser is launched with the developer tools opened (default: `false`)

## Notes

 - Only the Chrome version of SingleFile allows you to use SingleFile Companion at the moment. This feature will be available in Firefox when this bug is fixed: https://bugzilla.mozilla.org/show_bug.cgi?id=1630415. Although, you can use SingleFile Companion with Firefox by installing SingleFile manually, see https://github.com/gildas-lormeau/SingleFile#install.
