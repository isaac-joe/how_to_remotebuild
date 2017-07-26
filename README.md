# 在 Visual Studio 透過 remotebuild 建置 iOS App
<<<<<<< 3bb87acfaff12873b9a3070bf249ea2919f43b65
這是 2015 版本喔！

Visual Studio 開發 Cordova 專案，要 Build 出 iOS 的 App，可以這麼做：

如果開始安裝 Visual Studio 2015 時沒有勾選＂HTML/JavaScript (Apache Cordova) ＂，請由 "控制台 -\> 程式集 -\> 程式和功能 -\> 解除安裝或變更程式" 找到 Visual Studio 2015，選擇變更後再把「HTML/JavaScript(Apache Cordova)」勾選安裝。



首先增加 Visual Studio內的安裝套件：Cross Platform Mobile Development

![][image-1]
Windows 環境下安裝：
0.  Visual Studio 2015 
0.  Apache Ant 1.8.0 （Visual Studio 2015 instaler 裡面有）
0.  Oracle Java JDK 8 32bit版本 下載網址  
	http://www.oracle.com/technetwork/java/javase/downloads/index.html
0.  Node.js 6.1.1  32bit版本 下載網址https://nodejs.org/dist/v6.11.1/node-v6.11.1-x86.msi
0.  為了符合ngCordova以及AngularJS的需求，Visual Studio的Cordova版本支援不足，請以管理員權限開PowerShell安裝Global的最新Cordova版，指令如下：  
	npm install -g cordova
=======
這是 2015 版本 喔！

Visual Studio 開發 Cordova 專案，要 Build 出 iOS 的 App，首先增加 Visual Studio內的安裝套件：Cross Platform Mobile Development。

如果開始安裝 Visual Studio 2015 時沒有勾選＂HTML/JavaScript (Apache Cordova) ＂，請由 "控制台 -\> 程式集 -\> 程式和功能 -\> 解除安裝或變更程式" 找到 Visual Studio 2015，選擇變更後再把「HTML/JavaScript(Apache Cordova)」勾選安裝。

![][image-1]

接著，分別在已安裝 Visual Studio的 Windows 和已安裝 Xcode 的 MacOS 安裝以下套件：

[注意] Windows與MacOS需要位於同一區網內，例如 Windows 192.168.0.1，MacOS則是 192.168.0.2

**Windows 環境下安裝**

* Node.js 6.1.1 **32bit版本**  👉[下載][1]

接著以系統管理員，開啟 PowerShell 執行以下指令：

npm install -g cordova

為了符合ngCordova以及AngularJS的需求，Visual Studio的Cordova版本支援不足，請以管理員權限開PowerShell安裝Global的最新Cordova版，指令如下：  
	
>>>>>>> start

到時候開Visual Studio Solution時，點擊 Config.XML，出現視窗時，Cordova版本選擇全域版的 Cordova，如果Visual Studio的 舊版 Cordova無法回應AngularJS的指令時。


MacOS 環境下安裝：

0.  Node.js 6.1.1
0.  Cordova 7.0.1或更高（為了符合cordova-ios版本需要4.4.0以上） ，開terminal下指令：  
	npm install -g cordova  
	若出現權限不足，請加上sudo 執行以上指令，給予最高權限。
0.  Xcode 8.3.3 不要裝 Xcode 9.0
0.  Xcode 命令列工具
開啟終端機 terminal 指令為：
xcode-select  --install
0.  remotebuild  
	開終端機下指令  
	sudo npm install -g remotebuild

Visual Studio建置，選擇iOS，並可以選擇模擬器 iPhone系列，須在MacOS開啟 remotebuild 監聽 Visual Studio 要求組建的命令。

我們選擇簡易模式以HTTP服務，不用HTTPS，也就不用填PIN碼給Visual studio。開始 remotebuild 服務的  terminal 指令
remotebuild --secure false

<<<<<<< 3bb87acfaff12873b9a3070bf249ea2919f43b65
[image-1]:	installer.png
=======
[1]:	https://nodejs.org/dist/v6.11.1/node-v6.11.1-x86.msi

[image-1]:	https://github.com/isaac-joe/how_to_remotebuild/blob/master/installer.png?raw=true
>>>>>>> start
