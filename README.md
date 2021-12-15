# Windows10 超级装机优化工具，内含近 200 项调优和隐私保护设置

### ❀原创教程，转载本页必须注明链接和作者
来源于[Github/Disassembler0][0]，及[YouTube/Craft Computing][1]。主要进行了翻译，删重复，拆分以便编辑和注释掉可能不用优化的项目（就这样也花了我一整天才搞出来）。整个压缩包内包含了使用说明，优化部分1-7，以及其他可选优化。

##### 注意，这套代码里包括了Windows10预装应用的卸载，更改注册表，临时关闭文件管理器，更改Windows服务组件等等操作，所以不建议已经用了很久的系统直接拿来运行。

#### 优化项目

> 1「隐私」：
 - √ 关闭信息收集 --------------------- Disable Telemetry（关后无法加入Insider Program）
 - √ 关闭Wi-Fi密码共享 ---------------- Disable Wi-Fi Sense
 - √ 禁用Windows Defender阻止应用运行 - Disable SmartScreen Filter
 - √ 关闭开始菜单内置Bing搜索 --------- Disable Start Menu Bing Search
 - √ 禁用地理位置汇报 ----------------- Disable Location Tracking
 - √ 禁用微软反馈 --------------------- Disable Feedback
 - √ 禁用广告识别 --------------------- Disable Advertising ID
 - √ 禁用小娜 ------------------------- Disable Cortana
 - × 仅用本地网P2P更新Windows --------- Restrict Windows Update P2P only to local network
 - √ 移除开机内核加载log生成+阻止创建 -- Remove AutoLogger file and restrict directory
 - √ 禁用疑难解答信息收集 ------------- Stop and disable Diagnostics Tracking Service

> 2「一般Windows服务」：
 - √ 降低用户账户控制UAC通知"设置变更弹窗"的弹出级别 - Lower UAC level
 - √ 启用本机多用户共享本地网盘 -------------------- Enable sharing mapped drives between users
 - × 关闭防火墙 ----------------------------------- Disable Firewall
 - × 禁用Win自带杀软 ------------------------------ Disable Windows Defender
 - √ 关闭Windows更新后自重启 ---------------------- Disable Windows Update automatic restart
 - √ 关闭Windows家庭组相关服务 --------------------- Stop and disable Home Groups services
 - √ 降低DMWAPPUSHService启动的优先级

> 3「任务栏和文件管理器」：
 - × 禁用通知中心（右下角消息）----------------- Disable Action Center
 - × 禁用锁定（非公司电脑用） ------------------ Disable Lock screen
 - √ 禁用自动播放（USB插入后自动扫描媒体）------- Disable Autoplay
 - × 禁用程序自启动+CDROM双击直接打开exe ------- Disable Autorun for all drives
 - √ 关闭粘滞键命令 --------------------------- Disable Sticky keys prompt
 - √ 隐藏搜索框（开始菜单键直接输入即搜索）------ Hide Search button / box
 - × 任务栏移除任务视图按钮 -------------------- Hide Task View button
 - √ 小任务栏 --------------------------------- Show small icons in taskbar
 - √ 任务栏程序满后再合并 ---------------------- Show titles in taskbar
 - √ 隐藏所有小三角内图标 ---------------------- Hide tray icons as needed
 - √ 显示后缀名 ------------------------------- Show known file extensions
 - × 显示隐藏文件（系统用但影响文件夹和桌面排版）- Show hidden files
 - √ 文件管理器默认打开我的电脑/此电脑 ---------- Change default Explorer view to "Computer"
 - √ 桌面显示我的电脑/此电脑 ------------------- Show Computer shortcut on desktop
 - × 文件管理器左栏（Shell NameSpace）移除桌面 - Remove Desktop icon from computer namespace
 - × 文件管理器左栏（Shell NameSpace）移除文档 - Remove Documents icon from computer namespace
 - × 文件管理器左栏（Shell NameSpace）移除下载 - Remove Downloads icon from computer namespace
 - × 文件管理器左栏（Shell NameSpace）移除图片 - Remove Pictures icon from computer namespace
 - × 文件管理器左栏（Shell NameSpace）移除音乐 - Remove Music icon from computer namespace
 - × 文件管理器左栏（Shell NameSpace）移除视频 - Remove Video icon from computer namespace
 - × 添加副英语（美国）键盘（方便替换微软键盘为第三方用）- Add secondary en-US keyboard

> 4「卸载预装和赞助应用」：
 - √ 禁用并彻底卸载OneDrive --- Disable and completely uninstall OneDrive
 - × 卸载Windows自带WMP播放器 - Uninstall Windows Media Player
 - √ 卸载工作文件夹功能 ------- Uninstall Work Folders Client
> 
> · 关闭以下Windows服务：
 - √ 疑难解答的内核ETW信息收集 ----------------- Diagnostics Hub Standard Collector Service
 - √ 无线联网准入链接推送（公用无线网同意条款用）- WAP Push Message Routing Service
 - √ 缓存地图管理器 --------------------------- Downloaded Maps Manager
 - × 应用程序获知并共用单一TCP端口服务 --------- Net.Tcp Port Sharing Service
 - √ 远程桌面 -------------------------------- Routing and Remote Access
 - × 远程注册表 ------------------------------ Remote Registry
 - √ 外网已知连接共享（电脑做网关）------------- Internet Connection Sharing (ICS)
 - × 内网分布式链接跟踪（活动目录等功能，加入域后用）Distributed Link Tracking Client
 - × 生物识别服务（指纹，脸部识别）------------- Windows Biometric Service
 - × 无线网自动配置 --------------------------- WLAN AutoConfig
 - √ Win自带播放器WMP的网络共享 ---------------- Windows Media Player Network Sharing
 - × 安全中心 --------------------------------- Windows Security Center Service
 - × 搜索 ------------------------------------- Windows Search
 - √ Xbox Live Auth Manager
 - √ Xbox Live Game Save Service
 - √ Xbox Live Networking Service
 - √ 流量监控 --------------------------------- Windows Network Data Usage Monitor
> 
 - √ 阻止Windows更新的自动下载及其P2P上传 ----------- Optimizes Windows updates by disabling automatic download and seeding
 - × 禁止Windows自动更新硬件驱动 -------------------- Disable automatic driver update
> 
> · 卸载以下Windows预装+赞助商应用：
 - √ Microsoft.3DBuilder
 - √ Microsoft.Advertising.Xaml
 - √ Microsoft.Appconnector
 - √ Microsoft.BingFinance
 - √ Microsoft.BingNews
 - √ Microsoft.BingSports
 - √ Microsoft.BingTranslator
 - √ Microsoft.BingWeather
 - × Microsoft.FreshPaint
 - √ Microsoft.GamingServices
 - √ Microsoft.Microsoft3DViewer
 - √ Microsoft.WindowsFeedbackHub
 - √ Microsoft.MicrosoftOfficeHub
 - √ Microsoft.MixedReality.Portal
 - √ Microsoft.MicrosoftPowerBIForWindows
 - √ Microsoft.MicrosoftSolitaireCollection
 - × Microsoft.MicrosoftStickyNotes
 - √ Microsoft.MinecraftUWP
 - √ Microsoft.NetworkSpeedTest
 - √ Microsoft.Office.OneNote
 - √ Microsoft.People
 - √ Microsoft.Print3D
 - √ Microsoft.SkypeApp
 - √ Microsoft.Wallet
 - × Microsoft.Windows.Photos
 - × Microsoft.WindowsAlarms
 - × Microsoft.WindowsCalculator
 - × Microsoft.WindowsCamera
 - √ microsoft.windowscommunicationsapps
 - √ Microsoft.WindowsMaps
 - √ Microsoft.WindowsPhone
 - √ Microsoft.WindowsSoundRecorder
 - × Microsoft.WindowsStore
 - √ Microsoft.Xbox.TCUI
 - √ Microsoft.XboxApp
 - √ Microsoft.XboxGameOverlay
 - √ Microsoft.XboxGamingOverlay
 - √ Microsoft.XboxSpeechToTextOverlay
 - √ Microsoft.YourPhone
 - √ Microsoft.ZuneMusic
 - √ Microsoft.ZuneVideo
 - √ Microsoft.Windows.CloudExperienceHost
 - √ Microsoft.Windows.ContentDeliveryManager
 - √ Microsoft.Windows.PeopleExperienceHost
 - √ Microsoft.XboxGameCallableUI
 - √ Microsoft.CommsPhone
 - √ Microsoft.ConnectivityStore
 - √ Microsoft.GetHelp
 - √ Microsoft.Getstarted
 - √ Microsoft.Messaging
 - √ Microsoft.Office.Sway
 - √ Microsoft.OneConnect
 - √ Microsoft.WindowsFeedbackHub
 - √ Microsoft.Microsoft3DViewer
 - × Microsoft.MSPaint
 - √ Microsoft.BingFoodAndDrink
 - √ Microsoft.BingHealthAndFitness
 - √ Microsoft.BingTravel
 - √ Microsoft.WindowsReadingList
 - √ Microsoft.MixedReality.Portal
 - √ Microsoft.ScreenSketch
 - √ Microsoft.XboxGamingOverlay
 - √ Microsoft.YourPhone
 - √ 2FE3CB00.PicsArt-PhotoStudio
 - √ 46928bounde.EclipseManager
 - √ 4DF9E0F8.Netflix
 - √ 613EBCEA.PolarrPhotoEditorAcademicEdition
 - √ 6Wunderkinder.Wunderlist
 - √ 7EE7776C.LinkedInforWindows
 - √ 89006A2E.AutodeskSketchBook
 - √ 9E2F88E3.Twitter
 - √ A278AB0D.DisneyMagicKingdoms
 - √ A278AB0D.MarchofEmpires
 - √ ActiproSoftwareLLC.562882FEEB491
 - √ CAF9E577.Plex"
 - √ ClearChannelRadioDigital.iHeartRadio
 - √ D52A8D61.FarmVille2CountryEscape
 - √ D5EA27B7.Duolingo-LearnLanguagesforFree
 - √ DB6EA5DB.CyberLinkMediaSuiteEssentials
 - √ DolbyLaboratories.DolbyAccess
 - √ DolbyLaboratories.DolbyAccess
 - √ Drawboard.DrawboardPDF
 - √ Facebook.Facebook
 - √ Fitbit.FitbitCoach
 - √ Flipboard.Flipboard
 - √ GAMELOFTSA.Asphalt8Airborne
 - √ KeeperSecurityInc.Keeper
 - √ NORDCURRENT.COOKINGFEVER
 - √ PandoraMediaInc.29680B314EFC2
 - √ Playtika.CaesarsSlotsFreeCasino
 - √ ShazamEntertainmentLtd.Shazam
 - √ SlingTVLLC.SlingTV
 - √ SpotifyAB.SpotifyMusic
 - × TheNewYorkTimes.NYTCrossword
 - √ ThumbmunkeysLtd.PhototasticCollage
 - √ TuneIn.TuneInRadio
 - √ WinZipComputing.WinZipUniversal
 - √ XINGAG.XING
 - √ flaregamesGmbH.RoyalRevolt2
 - √ king.com.*
 - √ king.com.BubbleWitch3Saga
 - √ king.com.CandyCrushSaga
 - √ king.com.CandyCrushSodaSaga
 - × Microsoft.BioEnrollment
 - × Microsoft.MicrosoftEdge
 - × Microsoft.Windows.Cortana
 - × Microsoft.WindowsFeedback
 - × Microsoft.XboxGameCallableUI
 - × Microsoft.XboxIdentityProvider
 - × Windows.ContactSupport"
> 
 - √ 阻止Windows重装卸载的预装应用 ----------------- Prevents Apps from re-installing
 - √ 阻止Windows重装卸载的推荐应用 ----------------- Prevents "Suggested Applications" returning

> 5「开始菜单」：
 - √ 密码永不过期 ---------------------------------- Password never expires
 - √ 本机所有（包括未来添加）用户移除开始菜单所有瓷块 - Remove Start Menu Tiles
 - √ 移除现有开始菜单排版文件 ----------------------- Delete layout file if it already exists
 - √ 清除开始菜单排版缓存
 - √ 移除正常安装要求输入的隐私设置（音识，位置，寻回，信息搜集，Ink/输入搜集等）- Disable Privacy Settings Experience

> 6「黑色主题」：
 - √ 启用黑色主题 ---------------------------------- Windows Enable Dark Mode

> 7「UWP应用隐私」：
 - √ 禁用UWP应用后台自启动
 - √ 禁用UWP应用声纹启动
 - √ 禁用UWP应用通知信息访问权限
 - √ 禁用UWP应用账户信息访问权限
 - √ 禁用UWP应用联系人访问权限
 - √ 禁用UWP应用日历信息访问权限
 - √ 禁用UWP应用电话簿访问权限
 - √ 禁用UWP应用通话记录访问权限
 - √ 禁用UWP应用电子邮箱访问权限
 - √ 禁用UWP应用的短信访问权限
 - √ 禁用UWP应用的无线传输数据（如蓝牙）访问权限
 - √ 禁用UWP应用的外部设备同步权限
 - √ 禁用UWP应用的疑难解答信息访问权限
 - × 禁用UWP应用的库和文件系统访问权限
 - × 阻止创建UWP专用的Swap file（类似页文件Page file）

> 其它（需要手动运行）：
 - × 修复右键新建文本文档项目缺失 ---- Restore Desktop Right click --> New --> .txt context menu
 - × 去掉硬盘进度条 ----------------- Remove hard disk precentage bar
 - × 桌面恢复右键排列图标 ------------ Restore Desktop Right click --> sort by context menu
 - × 启用关机确认 ------------------- Enable shutdown confirmation button
 - × 清除我的电脑/此电脑下快速访问 ---- Collapse Quick Access ribbon from This PC window
 - × 右键新建去掉.rtf .psd和联系人 --- Remove Desktop Right click --> New --> .rtf, .psd & Contact context menu
 - × 我的电脑/此电脑USB盘符去重复 ---- De-redundant the same USB drive showing twice in File Exp. Name Space

#### Credits :
[@Disassembler0]( https://github.com/Disassembler0 ).
[Craft Computing]( https://www.youtube.com/channel/UCp3yVOm6A55nx65STpm3tXQ ).
Windows Debloat Video URL : https://www.youtube.com/watch?v=PdKMiFKGQuc <br>

#### 下载链接：[谷歌盘][3]，QQ群存档(加群问题说明来拿装机优化工具): <a href='https://jq.qq.com/?_wv=1027&k=5YJFXyf'>691892901</a><br>
那了个么就这样咯~

  [0]: https://github.com/Disassembler0/Win10-Initial-Setup-Script
  [1]: https://www.youtube.com/watch?v=PdKMiFKGQuc
  [2]: 
  [3]: https://drive.google.com/file/d/1l2_2hirNwmSE8_rsoL4lHU_Dkkt3ABUY/view?usp=sharing
