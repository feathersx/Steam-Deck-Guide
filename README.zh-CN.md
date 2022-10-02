<h1 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/142779553-82147e51-7e6d-47bd-9db6-fe2f5ad95355.png">
  <br />
  Steam Deck 指南
</h1>

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/142779557-400f19c8-6084-41ee-9449-fb08a15d6c45.png">
<br />
</p>


#### 指南不仅涵盖Steam Deck的使用说明，也包括应用和工具，这将使你更好地和更有效地使用你的Steam Deck设备。


**备注: 你可以轻松转换这个 markdown 文件到 PDF 在 [VSCode](https://code.visualstudio.com/) 中使用这个扩展 [Markdown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf) 或者在线转换工具 [AnyConv](https://anyconv.com/md-to-pdf-converter/).**

**备注2: 本指南将不断地更新，以获得新的信息，请随时在这里 [issue](https://github.com/mikeroyal/Steam-Deck-Guide/issues) 提出问题，如果你认为应该添加一些东西。**

# 目录

1. [开始使用 Steam Deck](#开始使用-steam-deck)

     - [Steam Deck 配件](#steam-deck-配件)
     - [Steam Deck 开发](#steam-deck-开发)
     - [Steam数据库](#steamdb)
     - [获取软件](#获取软件)
     - [用于Steam Deck的其他Linux操作系统](#用于steam-deck的其他linux操作系统)
     - [在Steam Deck上安装Windows 10或11操作系统](#在-steam-deck-上安装-windows-10-或-11操作系统)
     - [提高电池寿命](#提高电池寿命)
     - [复制/传输文件到Steam Deck的工具](#复制传输文件到-steam-deck-的工具)
     - [在你的Steam Deck上运行Android应用程序](#在你的-steam-deck-上运行android应用程序)
     - [在你的Steam Deck上运行Bottles](#在你的-steam-deck-上运行bottles)
     - [Steam Tinker Launch配置工具](#steam-tinker-launch配置工具)
     - [RetroDECK复古游戏模拟器](#RetroDECK复古游戏模拟器)
     - [在Steam Deck上添加Btrfs TF卡ext4工具](#btrfs-on-steam-deck)
     - [用于Steam Deck的系统插件](#plugin-loaders系统插件)
        * [Decky Loader 插件加载器](#decky-loader插件加载器)
          * [Steam Deck 强力硬件设置工具](#steam-deck-power-tools强力硬件设置工具)
        * [Crankshaft 插件管理器](#crankshaft插件管理器)
     - [在你的Steam Deck上安装虚幻引擎5](#在linux上安装虚幻引擎unreal-engine)

2. [游戏](#gaming游戏)

     - [Steam 服务介绍](#steam-服务介绍)
     - [ProtonDB 游戏兼容性数据库](#protondb-游戏兼容性数据库)
     - [Lutris 第三方游戏平台](#lutris-第三方游戏平台)
        * [Epic 游戏商店整合](#epic-游戏商店整合)
        * [暴雪战网整合](#暴雪战网整合)
        * [EA Play 整合](#ea-play-整合)
        * [Origin 整合](#origin-整合)
        * [Ubisoft Connect 育碧整合](#ubisoft-connect-整合)
        * [GOG Galaxy 整合](#gog-galaxy-整合)
     - [GameHub 游戏库](#gamehub游戏库)
     - [Epic 游戏商店](#epic-游戏商店)
     - [Game Streaming 游戏串流](#game-streaming游戏串流)
     - [游戏模拟器](#game-emulators游戏模拟器)

3. [游戏开发](#游戏开发)

4. [Vulkan 开发](#vulkan-开发)

5. [DirectX 开发](#directx-开发)

6. [OpenGL 开发](#opengl-开发)

7. [Wayland 开发](#wayland-开发)

8. [Audio 音频开发](#audio-音频开发)


# 开始使用 Steam Deck
[回到顶部](#目录)

[Steam Deck](https://www.steamdeck.com/) 是由 [Valve 公司](https://valvesoftware.com/) 与 [Advanced Micro Devices (AMD)](https://www.amd.com/)合作开发的一款掌上游戏电脑。它允许用户游玩他们的整个Steam游戏库，但可以由用户修改，以运行其他游戏店面或应用程序。Steam Deck于2022年2月开始发货。

* [Steam Deck 小册子](https://store.steampowered.com/news/app/1675200/view/3401926123919972634)

* [Steam Deck 顶级技巧和窍门 第一部分 | GamingOnLinux](https://www.gamingonlinux.com/2022/08/top-quick-steam-deck-tips-and-tricks/)
 
* [Steam Deck 技巧和窍门第二部分 | GamingOnLinux](https://www.gamingonlinux.com/2022/08/steam-deck-tips-and-tricks-part-2/)

* [Steam Deck 拆解 作者：Jeff Suovanen | iFixit](https://www.ifixit.com/News/57101/steam-deck-teardown)

* [解锁Steam Deck教程 | Chris Titus Tech](https://christitus.com/unlock-steam-deck/)

* [Steam Deck 硬件评测 by Linus Tech Tips
](https://www.bilibili.com/video/BV1J44y1p7Ay/)

* [Steam Deck 拆箱体验 by Linus Tech Tips](https://www.youtube.com/watch?v=_UB9XoPlJ0U)

* [Steam Deck 拆解 by Linus Tech Tips](https://www.youtube.com/watch?v=ZK43RAc90ZA)

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/142779563-30ada576-1bf4-42fb-8ad5-3fa3a6e40103.png">
<br />
</p>

Steam Deck 设备信息，来自: [Steam Deck](https://www.steamdeck.com)

[Steam OS 3.0](https://store.steampowered.com/steamdeck) 是一个 [immutable](https://en.wikipedia.org/wiki/Immutable_object) 使用 [KDE Plasma](https://kde.org/plasma-desktop) 的桌面操作系统(OS)。这允许你使用[Flatpak](https://flatpak.org/)在容器中安装应用程序，而不是安装在根文件系统上。这不仅意味着应用程序的安装与系统核心文件系统是隔离的，而且还意味着恶意应用程序入侵/破坏你的系统的能力大大降低。

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/157353163-6f5c4c1a-a89f-4ee5-9ffe-1d9f991c773c.png">
  <br />
  SteamOS 3.0 来自 KDE Plasma 桌面
</h3>

**Steam Deck Specs:**

操作系统: [SteamOS](https://en.wikipedia.org/wiki/SteamOS) 3.0 基于 [ArchLinux](https://archlinux.org/).

系统芯片 (SoC): AMD 定制 APU.

CPU：Zen 2 4核/8线程、频率2.4-3.5GHz（最高可达 448 GFlops FP32）

内存:	16 GB LPDDR5 板载 RAM（5500 MT/s 32 位四通道）

存储选项:

 - 基本版本: 64 GB eMMC for $399(US).
 - 高级版本: 256 GB NVMe SSD for $529(US).
 - 旗舰版本: 512 GB NVMe SSD for $649(US).

**所有型号均使用 M.2 2230 接口。**

可移动存储: **microSD（TF）** 支持高达2TB的额外存储，用于游戏存储。

显示屏幕: 7英寸, 1280 × 800 LCD, native 800p @ 60Hz.

扩展坞分辨率: 最高 8K @ 60Hz 或 4K @ 120Hz.

显卡（GPU）：8 RDA 2 CUs、频率1.0-1.6GHz（最高可达 1.6 TFlops FP32）
APU 功率：4-15W

## Steam Deck 配件
[回到顶部](#目录)

[PROJECT Killswitch](https://dbrand.com/killswitch) 是为Steam Deck定制的保护套，由 [dbrand](https://dbrand.com/) 设计。

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/155908502-f015431e-6abd-4e31-8ad1-2d43f5ba6850.png">
<br />
 前面
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/155910314-78b454c8-94d3-43dc-a9e2-75b9819c9398.png">
<br />
 后面
</p>

[JSAUX Steam Deck 扩展坞](https://www.jsaux.com/products/steam-deck-docking-station) 是一个用于Steam Deck的6合1坞站。配备了一个HDMI 4K@60Hz输出，一个千兆以太网输入，一个用于充电的USB-C端口，以及三个USB-A 3.0端口，让你探索玩转Steam Deck的新方式。它支持100W(最大)的电力传输，在与原始充电器配对时，足以为你的Steam Deck全速充电(45W)。

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/186289763-9eca1e86-ed13-4cd4-a1ce-c4e433442d78.png">
<br />
JSAUX Steam Deck 扩展坞
</p>

[NexDock](https://nexdock.com/features/) 是一个带有HDMI输入端口和Type-C电缆NexDock的配件，可以将Steam Deck变成一台全功能的电脑。

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/163284895-74fdfeaa-54df-4d7c-8e79-6117ca40b794.jpg">
<br />
</p>

**NexDock 2-in-1. 来自: [NexDock](https://nexdock.com/features/)**

[Xbox Wireless Controller + USB-C® Cable](https://www.xbox.com/en-us/accessories/controllers/xbox-wireless-controller-usb-c)

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/187094245-3c406751-4e4b-42fd-bd2c-a72181722fad.png">
<br />
Xbox Controller
</p>

[PlayStation 5 DualSense™ Wireless Controller](https://www.playstation.com/en-us/accessories/dualsense-wireless-controller/)

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/187094347-109c80cd-5cc3-4a97-8a8f-0181687ab0d4.png">
<br />
PS 5  DualSense™ Controller
</p>

[Steam Deck 钢化玻璃膜 亚马逊](https://www.amazon.com/Tempered-Protector-Compatible-Installation-Manufacturer/dp/B09L9F65JG)

[M.2 2230 SSD 固态硬盘 亚马逊](https://www.amazon.com/m-2-2230-ssd/s?k=m.2+2230+ssd)

[M.2 2230 SSD 固态硬盘 新蛋](https://www.newegg.com/p/pl?d=m.2+2230+ssd)
 
[Lexar MicroSD 存储卡 亚马逊](https://www.amazon.com/lexar-micro-sd-cards/s?k=lexar+micro+sd+cards)

[SanDisk 1TB 存储卡 亚马逊](https://www.amazon.com/SanDisk-1TB-Micro-SD-Cards/s?k=SanDisk+1TB+Micro+SD+Cards)

[Samsung 512GB EVO Select 存储卡 亚马逊](https://www.amazon.com/SAMSUNG-Adapter-microSDXC-MB-ME512KA-AM/dp/B09B1HMJ9Z)

[Anker 45w Ultra Slim 充电器 亚马逊](https://www.amazon.com/Charger-Anker-Ultra-Slim-PowerPort-Laptops/dp/B0841J6CMK)

[Anker PowerCore 充电宝 亚马逊](https://www.amazon.com/Anker-Portable-PowerCore-Essential-Compatible/dp/B08LG2X98F)

[Anker USB C Hub](https://www.anker.com/products/114/142/usb-c-hubs)


## Steam Deck 开发
[回到顶部](#目录)

**开发资源的快速链接**

  - [让你的游戏为Steam Deck做好准备](https://partner.steamgames.com/doc/steamdeck/recommendations)

  - [在没有开发包的情况下为Steam Deck开发](https://partner.steamgames.com/doc/steamdeck/testing)

  - [Steam Deck 开发工具包](https://partner.steamgames.com/doc/steamdeck/devkits)
  
  - [GitLab上的SteamOS Devkit服务](https://gitlab.steamos.cloud/devkit/steamos-devkit-service)

  - [GitLab上的SteamOS Devkit客户端](https://gitlab.steamos.cloud/devkit/steamos-devkit)

  - [Steam Deck 和 Proton html5 粒子引擎](https://partner.steamgames.com/doc/steamdeck/proton)

  - [Steam Deck 开发者论坛](https://steamcommunity.com/groups/steamworks/discussions/27/)

[Steamworks](https://partner.steamgames.com/doc/home) 是一套免费的工具，任何开发者都可以在他们的游戏或软件中使用Steam和Steam Deck。

[Steam Hardware GitLab Repo](https://gitlab.steamos.cloud/SteamDeck/hardware) 是一个包含Steam Deck外部外壳（表面拓扑结构）的CAD文件的资源库，采用知识共享许可方式。这包括STP模型、STL模型和图纸（DWG），供参考。

[Dynamic Cloud Sync](https://steamcommunity.com/groups/steamworks/announcements/detail/3142949576401813670) 是一个工具，Steam将用来在设备进入睡眠模式之前，自动将所有修改过的保存游戏数据上传到云端。然后，用户可以在任何PC、笔记本电脑或其他设备上恢复他们的游戏。当用户回到他们的Steam甲板并唤醒设备时，Steam也将自动下载任何保存游戏的变化。

[Steam Cloud](https://partner.steamgames.com/doc/features/cloud) 是一个工具，为您的游戏提供一个简单透明的远程文件存储系统。在自动云配置中指定的文件或使用云API写入磁盘的文件（创建、修改、删除等）将在游戏退出后自动复制到Steam服务器中。如果用户更换了电脑，在游戏启动之前，这些文件会自动下载到新的电脑上。然后，游戏可以通过云端API读取这些文件，或者像往常一样直接从磁盘上读取这些文件。避免机器的特定配置，如视频设置。

[Gamescope](https://github.com/Plagman/gamescope) 是一个SteamOS会话微组合窗口管理器，以前被称为 [steamcompmgr](https://github.com/ValveSoftware/steamos-compositor).

[AMD FidelityFX Super Resolution (FSR)](https://www.amd.com/en/technologies/radeon-software-fidelityfx) 是一个开源的、高质量的解决方案，用于从较低的分辨率输入产生高分辨率的帧。FSR为昂贵的渲染操作实现了 "实际性能"，例如AMD RDNA™和AMD RDNA™ 2架构的硬件光线追踪（用来替代NVIDIA DLSS）。

[AMD FidelityFX Super Resolution (FSR) 2.0](https://www.amd.com/en/press-releases/2022-03-17-introducing-amd-software-adrenalin-edition-2022-release-and-amd) 是一个开源的、高质量的解决方案，用于从较低的分辨率输入产生高分辨率的帧。它使用时间数据和优化的抗锯齿，在支持的游戏中提高帧率，同时提供类似或优于原始分辨率的图像质量，而不需要专用的机器学习硬件。AMD FSR 2.0将在2022年第二季度的某个时候推出。

[MangoHud](https://github.com/flightlessmango/MangoHud) 是一个Vulkan和OpenGL覆盖，用于监测FPS、温度、CPU/GPU负载等。

[GOverlay](https://github.com/benjamimgois/goverlay) 是一个开源项目，旨在创建一个图形用户界面来管理Vulkan/OpenGL覆盖。它仍然处于早期开发阶段。

[ReplaySorcery](https://github.com/matanui159/ReplaySorcery) 是一个开源的、用于Linux的即时重放解决方案。

[Luxtorpeda](https://github.com/luxtorpeda-dev/luxtorpeda) 是一个Steam Play兼容工具，可以使用本地Linux引擎运行游戏。

[SteamGridDB](https://www.steamgriddb.com/projects) 是一个巨大的数据库，你可以在这里下载和分享定制的视频游戏资产，并使你的游戏库个性化。

[SGDBoop](https://www.steamgriddb.com/boop) 是一个工具，只需点击一个按钮，就能自动将SteamGridDB中的资产直接应用到你的Steam库中，不需要手动下载和设置。 [Available as a Flatpak](https://flathub.org/apps/details/com.steamgriddb.SGDBoop)

[Deck Verified](https://www.steamdeck.com/en/verified) 是一个审查Steam目录中的游戏的程序，以验证它们与Steam Deck的兼容性。因此，当你在Steam Deck上访问你的图书馆时，你会发现每个标题都有一个兼容性徽章，反映了你在Steam Deck上玩每个游戏时可以期待的那种体验。

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/142779573-254b3ce4-e0e8-401f-a343-bf5b3aa29b66.png">
<br />
</p>

Deck 已认证 程序 分类 资源: [Steam Deck](https://www.steamdeck.com/en/verified)

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/142779574-d0410dc5-12cd-41ef-9cfa-03488c50b2ff.png">
<br />
</p>

Steam库游戏的兼容性徽章。资源: [Steam Deck](https://www.steamdeck.com/en/verified)

## SteamDB
[回到顶部](#目录)

[SteamDB](https://steamdb.info/instantsearch/) 是一个关于Steam上所有游戏的数据库。重要提示 SteamDB是一个非官方项目，与Valve或Steam没有任何关系。
   
   - [Steam Deck 已通过验证游戏列表](https://steamdb.info/instantsearch/?refinementList%5Boslist%5D%5B0%5D=Steam%20Deck%20Verified)
   
   - [Steam Deck 可玩的游戏列表](https://steamdb.info/instantsearch/?refinementList%5Boslist%5D%5B0%5D=Steam%20Deck%20Playable)
   
   - [Steam Deck 不支持游戏列表](https://steamdb.info/instantsearch/?refinementList%5Boslist%5D%5B0%5D=Steam%20Deck%20Unsupported)


## 获取软件
[回到顶部](#目录)

[Discover](https://apps.kde.org/discover/)  是一个软件中心，让你从多个来源管理软件，包括你的操作系统的软件库、Flatpak软件库、Snap商店，甚至是store.kde.org的AppImages。另外，Discover允许你寻找、安装和管理Plasma的附加组件和所有你喜欢的KDE应用程序。

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/156265563-1e9776f6-048f-4c20-b93b-d06ddcafed6d.png">
<br />
 KDE Plasma Discover 应用程序商店
</p>

[Flathub](https://flathub.org/) 是一个应用程序商店和数百个应用程序的构建服务，可以轻松地安装在任何Linux发行版上。在线浏览应用程序，从你的应用程序中心或命令行。

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/156265570-56fe8837-3963-49c8-b3f9-24a219929625.png">
<br />
 Flathub 应用程序商店
</p>

**注意：** Flathub应用搜索将被整合到Discover中，如果你想将应用搜索限制在Flathub，你可以通过点击星星将Flatpak标记为默认。

[Flatseal](https://github.com/tchx84/flatseal) 是一个图形化的工具，用于审查和修改你的 [Flatpak](https://flatpak.org/) 应用程序的权限。 [在Flathub商店获得](https://flathub.org/apps/details/com.github.tchx84.Flatseal).


## 用于Steam Deck的其他Linux操作系统。
[回到顶部](#目录)

[HoloISO](https://github.com/theVakhovskeIsTaken/holoiso) 是一个SteamOS 3 (Holo) archiso配置。它的目的是将Steam Deck的Holo操作系统带入一个通用的、可安装的格式，并提供一个接近官方的SteamOS体验。

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/167318762-c54fffa2-9ed4-4695-9d7d-4d03eb5ba49d.png">
  <br />
</p>

HoloISO Desktop. Credit: [theVakhovskeIsTaken](https://github.com/theVakhovskeIsTaken/)

[Nobara Project](https://gitlab.com/GloriousEggroll/nobara-images) 是一个非官方的Fedora Linux Spin，是为游戏定制的。它添加了必要的软件包/工具(如 [Lutris](https://lutris.net/) 和 [ProtonUp-Qt](https://davidotek.github.io/protonup-qt/))，并修复了一些问题，使Fedora在游戏方面更加出色。这个项目是由 [Thomas Crider AKA Glorious Eggroll](https://gitlab.com/GloriousEggroll).

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/179671757-008ac6ef-ee95-43e9-b6eb-2f9bb928f91b.png">
  <br />
</p>

[WinesapOS](https://github.com/LukeShortCloud/winesapOS) 是一个由 [LukeShortCloud](https://github.com/LukeShortCloud) 开发的项目，它提供了一个易于设置的Linux安装。它可以在闪存驱动器、SD卡、HDD、SSD、NVMe或任何其他存储设备上使用。 [release images](https://github.com/LukeShortCloud/winesapOS/releases) 基于SteamOS 3和KDE Plasma桌面环境，与Valve的Steam Deck [Steam Deck](https://store.steampowered.com/steamdeck/) 所使用的一致。

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/163284898-ca65b1ac-8ebc-4adc-b5aa-bd6b5195295e.jpg">
  <br />
</p>

WineapOS Desktop. Credit: [LukeShortCloud](https://github.com/LukeShortCloud)

 **[Manjaro Linux](https://manjaro.org/)**

 <h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/142779587-fbfac305-7cae-4768-80e8-d87830471232.png">
  <br />
  Manjaro Linux Desktop with KDE
</h3>

**[EndeavourOS](https://endeavouros.com/)**

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/107439882-9e414780-6ae7-11eb-819e-e87e7bcc7a97.png">
  <br />
  EndeavourOS Desktop
</h3>

**[Garuda Linux](https://garudalinux.org/)**

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127042105-f6a6d97e-77bd-402e-af4f-df7af588eb08.png">
  <br />
 Garuda Linux Desktop
</h3>

**[ArcoLinux](https://arcolinux.com/)**

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/128940632-9e2a198f-f84d-490b-b4a2-22f6217ee574.png">
  <br />
ArcoLinux Desktop
</h3>

**[ArchTitus](https://github.com/ChrisTitusTech/ArchTitus) created by [ChrisTitusTech](https://www.youtube.com/channel/UCg6gPGh8HU2U01vaFCAsvmQ)**

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/142780015-51242184-ff8b-4705-b6b3-f1913b734bf2.png">
  <br />
ArchTitus Desktop
</h3>

**[Fedora 35](https://getfedora.org/)**

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/142779592-8b70c81e-ac10-4bb3-91b5-efe25fa9afb4.png">
  <br />
Fedora Desktop
</h3>

**[Pop!_OS](https://pop.system76.com)** created by [System76](https://system76.com).

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/142779593-390dfd58-a246-4299-baf2-adf0207da696.png">
  <br />
Pop!_OS Desktop
</h3>

**[Batocera](https://batocera.org/)**

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/4238928/163190916-d39124bb-c67e-42e4-a97c-dac78684c452.png">
  <br />
Emulation Station Front End
</h3>

## 在 Steam Deck 上安装 Windows 10 或 11操作系统

[回到顶部](#目录)

**[Steam Deck Windows 资源](https://help.steampowered.com/en/faqs/view/6121-ECCD-D643-BAA8)**

**[恢复指南](https://help.steampowered.com/en/faqs/view/1B71-EDF2-EB6D-2BB3) 恢复到默认的Steam Deck操作系统。**

**[Windows 11](https://www.microsoft.com/en-us/software-download/windows11)**

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124997795-20cf2400-e000-11eb-8954-4944286b8ea8.png">
  Windows 11 桌面
</h3>

**[Windows 10](https://www.microsoft.com/en-us/software-download/windows10ISO)**

<h3 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/120387363-a9aabf80-c2de-11eb-84a5-8e4b422e7546.png">
  Windows 10 桌面
</h3>

## 提高电池寿命
[回到顶部](#目录)

[Steam Deck - 如何在游戏中获得最佳的电池寿命! | The Phawx YouTube](https://www.youtube.com/watch?v=zB6tkjuXX8A-Y)

[auto-cpufreq](https://github.com/AdnanHodzic/auto-cpufreq) 是一个用于Linux的自动CPU速度和功率优化器，它基于对笔记本电脑的电池状态、CPU使用率、CPU温度和系统负载的主动监测。最终让你在不做任何妥协的情况下提高电池寿命。
   
   - [auto-cpufreq - tool demo (Automatic CPU speed & power optimizer for Linux) | YouTube](https://www.youtube.com/watch?v=QkYRpVEEIlg-Y)

[Power-Control-Panel](https://github.com/project-sbc/Power-Control-Panel) 是一个软件工具，可以在 **windows手持设备（包括Steam Deck）** 上轻松改变TDP。功能包括: 

  - 可配置的配置文件，包括充电器与电池的数值 -新输入的TDP改变能力（按住LB、RB和Dpad方向）
  - 将一个exe指定给一个配置文件，当exe打开时自动启动
  - 登录时自动启动到系统托盘
  - 触摸友好界面，不需要键盘（大部分）。
        
 [Power Control App | Project-SBC YouTube](https://www.youtube.com/watch?v=PcSV1tto2OM-Y)
 
## 复制/传输文件到 Steam Deck 的工具
 [回到顶部](#目录)
 
[KDE Connect](https://kdeconnect.kde.org/)  是一个工具，可以让你轻松地将你的手机和你的电脑连接起来，将你的电脑和你的平板电脑连接起来；或者将你的电脑和你的Steam Deck设备连接起来。它可以用来跨设备共享文件，直接从你的笔记本电脑上读取和发送短信，并远程锁定你的电脑。

[Warpinator](https://github.com/linuxmint/warpinator) 是一个免费的开源工具，用于在同一网络中的计算机之间发送和接收文件。[Warpinator Flatpak](https://flathub.org/apps/details/org.x.Warpinator)

[FileZilla Client](https://filezilla-project.org/) 客户端是一个快速和可靠的跨平台FTP、FTPS和SFTP客户端，具有许多有用的功能和直观的图形用户界面。[FileZilla Flatpak](https://flathub.org/apps/details/org.filezillaproject.Filezilla)

[Dragit](https://github.com/sireliah/dragit) 是一个在设备之间进行直观的文件共享的应用程序。当你想以最小的努力将文件从一台电脑发送到另一台电脑时，它很有用。Dragit在mDNS协议的帮助下自动检测本地网络中的设备并允许你立即发送文件。 [Dragit Flatpak](https://flathub.org/apps/details/com.sireliah.Dragit)

[WinFsp](https://github.com/winfsp/winfsp) 是一套用于Windows计算机的软件组件，允许创建用户模式的文件系统。在这个意义上，它类似于FUSE（用户空间中的文件系统），后者在类似UNIX的计算机上提供同样的功能。

[SSHFS-Win](https://github.com/winfsp/sshfs-win) 是SSHFS在Windows上的一个最小移植。它使用Cygwin的POSIX环境和WinFsp的FUSE（用户空间的文件系统）功能。

[RiftShare](https://riftshare.app) 是一个跨平台（Windows、MacOS、Linux）的文件共享工具，支持使用简单的口令在本地网络和网络外进行完全加密的传输。RiftShare在后台使用 [magic-wormhole](https://github.com/magic-wormhole/magic-wormhole) ，与其他magic-wormhole客户端兼容。它也是完全开源的，并在GPLv3下许可。[RiftShare Flatpak](https://flathub.org/apps/details/app.riftshare.RiftShare)

[SyncThing](https://syncthing.net/) 是一个连续的文件同步程序。它在两台或更多的计算机之间实时同步文件，安全地保护它们不被窥视。适用于Mac OS X、Windows、Linux、FreeBSD、Solaris、OpenBSD、Android和许多其他系统。可在Discover中下载。它也是开源的，在MPL-2.0许可下授权

[Usermode FTP Server](https://gitlab.com/ergoithz/umftpd) 是一个工具，让你作为用户启动一个FTP服务器，用任何FTP客户端传输文件。允许你用许多文件浏览器的内置FTP支持直接访问你的文件。Windows文件浏览器、Thunar、Gnome Files、Dolphin等等。 [Usermode FTP Server on FlatHub](https://flathub.org/apps/details/eu.ithz.umftpd)

## 在你的 Steam Deck 上运行Android应用程序
[回到顶部](#目录)

[Waydroid](https://github.com/waydroid/waydroid) 是一种基于容器的方法，可以在普通的Linux系统上启动一个完整的Android系统。请务必查看 [Waydroid Arch wiki page](https://wiki.archlinux.org/title/Waydroid). 

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/189516892-24454312-836a-4a88-a6b8-a3e9aaa8612c.png">
<br />
 
</p>

[Anbox](https://github.com/anbox) 是一个基于容器的软件，用于在Linux发行版上运行一个完整的Android系统。请务必查看 [Anbox Arch wiki page](https://wiki.archlinux.org/title/Anbox).


## 在你的 Steam Deck 上运行Bottles
[回到顶部](#目录)

[Bottles](https://usebottles.com/) 是一个软件工具，让你在Linux上运行Windows软件。它内置的依赖性安装系统赋予了软件自动兼容的权限。下载管理器可以下载官方组件，如：运行器（Wine、Proton）、DXVK、依赖项等。可在 [FlatHub](https://flathub.org/apps/details/com.usebottles.bottles) 或通过 [KDE Discover](https://apps.kde.org/discover/) 商店获得。

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/182049940-ccba08e7-b05d-4991-b36f-1e2596c390da.png">
 </p>
 
 ## Steam Tinker Launch配置工具
 
 [回到顶部](#目录)
 
 [Steam Tinker Launch](https://github.com/frostworx/steamtinkerlaunch) 是一个用于Steam客户端的Linux封装工具，它可以在运行中快速定制和启动游戏的工具和选项。
 
  <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/176962906-5d388e16-955e-4936-a676-c591d0937acd.png">
 </p>
 
 ## RetroDECK（复古游戏模拟器）
 
 [回到顶部](#目录)
 
[RetroDECK](https://retrodeck.net/) 是一个工具，它带来了一个直接从SteamOS编目和播放你的复古游戏的环境，它是专门为Steam Deck定制的。它由EmulationStation桌面版驱动，使用RetroArch和其他独立的模拟器，让你在一个整洁的环境中导入和播放你最喜欢的复古（甚至非复古）游戏，而不会充斥你的Steam库。
 
 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/180627466-718dd292-cad0-48bb-93d0-e071a9e42194.png">
 </p>
 
 ## Btrfs on Steam Deck
 [回到顶部](#目录)
 
 [SteamOS Btrfs](https://gitlab.com/popsulfr/steamos-btrfs/) 是一个项目，它将帮助你从在Steam Deck的microSD卡或主目录上使用ext4，说明： [Btrfs](https://btrfs.wiki.kernel.org/). 
 
 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/172273657-f184233d-56d8-429b-9a63-d8a2b8e7412b.png">
 </p>
 
 ## Plugin Loaders（系统插件）
 [回到顶部](#目录)

 ### Decky Loader（插件加载器）

[Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader) 是一个用于Steam Deck的插件加载工具。

**特点:**

  - 干净地注入和加载一个或多个插件。
  - 持久性，意味着每次系统更新后都不需要重新安装。
  - 允许插件和加载器之间的双向通信。
  - 允许插件定义python函数并从javascript中运行它们。
  - 允许插件进行fetch请求调用，完全绕过cors（跨域）。

在这个商店[this store](https://plugins.deckbrew.xyz/)里可以找到Decky Loader的可用插件列表。 
 
 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/176962910-9bf09ad0-1ab2-4524-bd50-7420afec2c4a.png">
 </p>

 #### Steam Deck Power Tools（强力硬件设置工具）
[回到顶部](#目录)

[Steam Deck PowerTools](https://github.com/NGnius/PowerTools) 是Decky开发的一个插件，为用户提供高级系统调整。

   - 启用和禁用CPU线程和SMT
   - 设置CPU的最大频率和切换提升
   - 设置一些GPU功率参数（fastPPT & slowPPT）
   - 设置风扇转速（在SteamOS测试版上不支持）
   - 显示补充的电池信息
   - 在重新启动之间保持设置（存储在~/.config/powertools.json中）
  
 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/168942613-685cf180-3b1d-4a29-ba10-f5bdfbcfdfb6.png">
 </p>

 ### Crankshaft（插件管理器）
[Crankshaft](https://crankshaft.space/) 是一个Steam客户端插件管理器和框架。它可以让你安装和创建插件，为你的Steam客户端添加更多功能。 [Available as a Flatpak](https://flathub.org/apps/details/space.crankshaft.Crankshaft)

 <p align="center">
 <img src="https://user-images.githubusercontent.com/2069735/193312550-4c3c5c0d-11ef-4eef-bf19-32e522398fd0.png">
 </p>

## 在Linux上安装虚幻引擎（Unreal Engine）

[回到顶部](#目录)

在您的Linux系统上安装虚幻引擎5的最简单的方法是使用Epic资产管理器，它可以在 [FlatHub](https://flathub.org/) 上以 [Flatpak](https://flatpak.org)的形式提供。如果您的Linux系统上没有安装Flatpak，请按照这里 [简单的说明来开始安装](https://flatpak.org/setup/).

[Epic Asset Manager](https://flathub.org/apps/details/io.github.achetagames.epic_asset_manager) 是一个非官方的客户端，用于安装 [Unreal Engine](https://www.unrealengine.com/)、下载和管理从 [Epic Games Store](https://www.unrealengine.com/marketplace?lang=en-US) 商店购买的资产、项目、插件和游戏。

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/180886562-ef6aa63d-8117-4719-9af1-e25108042c2c.png">
<br />
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/180886564-3ebc8ecb-e2c0-4e53-9f45-f986bd24a89d.png">
<br />
</p>

**开发资源的快速链接**

 - [Sign-up for Epic Games Acount](https://www.epicgames.com/account/password)
 
 - [Sign-up for Epic Games GitHub](https://github.com/EpicGames/Signup)
 
 - [Unreal Engine 5 Linux Binary Download](https://www.unrealengine.com/en-US/linux)
 
 - [Linux Development Requirements for Unreal Engine](https://docs.unrealengine.com/5.0/en-US/linux-development-requirements-for-unreal-engine/)
 
 - [Unreal Engine Performance and Profiling](https://docs.unrealengine.com/5.0/en-US/TestingAndOptimization/PerformanceAndProfiling/)
 
 - [Unreal Engine Blueprint API Reference](https://docs.unrealengine.com/5.0/en-US/BlueprintAPI/index.html)

 - [Unreal Engine C++ API Reference](https://docs.unrealengine.com/5.0/en-US/API/index.html)

 - [Unreal Engine Python API Reference](https://docs.unrealengine.com/5.0/en-US/PythonAPI/index.html)
 
# Gaming（游戏）
[回到顶部](#目录)

## Steam 服务介绍

[Steam](https://store.steampowered.com/about/)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/106686402-13100100-657f-11eb-9012-6bdac264a808.png">
 </p>
 
[Steam Remote Play Together](https://store.steampowered.com/remoteplay/#together) 是一项Steam服务，让你通过互联网与朋友免费分享你的Steam本地多人游戏。使用Remote Play Together，一个玩家拥有并运行游戏，然后最多四个玩家可以加入。

[Steam Link app](https://store.steampowered.com/steamlink/about) 应用程序可以免费使用，将你的Steam PC游戏串流到手机、平板电脑和电视。

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/112692999-14ea9800-8e3d-11eb-964a-6bee4e665900.png">
</p>

[Proton](https://github.com/ValveSoftware/Proton/) 质子引擎是一个与Steam客户端一起使用的工具，它允许Windows独有的游戏在Linux操作系统上运行。它使用Wine来促进这一点。

[ProtonUp-Qt](https://github.com/DavidoTek/ProtonUp-Qt) 是一个工具，用于安装和管理Steam的 [Proton-GE](https://github.com/GloriousEggroll/proton-ge-custom) 和 [Luxtorpeda](https://github.com/luxtorpeda-dev/luxtorpeda) 的 [Wine-GE](https://github.com/GloriousEggroll/wine-ge-custom) 并使用这个图形用户界面。基于AUNaseef的 [ProtonUp](https://github.com/AUNaseef/protonup)，用Python 3和Qt 6制作。

## ProtonDB 游戏兼容性数据库
[回到顶部](#目录)

[ProtonDB](https://www.protondb.com) 收集了超过100,000份来自其他玩家的游戏报告，他们在Linux上用Proton测试游戏，并提供游戏表现的总分。一个不断增长的建议库提供了一些调整，在质子继续发展的同时，你可以尝试让游戏工作。除此之外，你还可以在这个网站上探索Steam游戏目录，浏览和发现各种以前无法在Linux上使用的游戏。

 - [ProtonDB 游戏兼容性检查列表](https://www.protondb.com/explore?selectedFilters=antiCheat)

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108773213-dcd8f800-7512-11eb-8775-19b0c8924d55.png">
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108773214-dd718e80-7512-11eb-983b-ce192e5b30f2.png">
</p>

## Lutris 第三方游戏平台
[回到顶部](#目录)

[Lutris](https://lutris.net) 是一个Linux的游戏客户端。它让你可以访问你所有的视频游戏，但目前的控制台一代除外。同时，与其他商店如GOG、Steam、Battle.net、Origin、Ubisoft Connect和许多其他来源很好地整合，允许你导入你现有的游戏库和社区维护的安装脚本给你一个完全自动化的设置。

### Epic 游戏商店整合

[回到顶部](#目录)

[添加 Epic Games Store](https://lutris.net/games/epic-games-store/)

 <img src="https://user-images.githubusercontent.com/45159366/106686406-14412e00-657f-11eb-97c4-c80c6e25a374.png">
 
 ### 暴雪战网整合
[回到顶部](#目录)

[Blizzard Battle.net](https://lutris.net/games/battlenet/) 暴雪战网是一个基于互联网的在线游戏、数字发行和数字版权管理平台，由动视和暴雪娱乐开发。Battle.net是《魔兽世界》、《暗黑破坏神III》、《星际争霸II》、《炉石传说》、《风暴英雄》、《守望先锋》和《使命召唤》的启动程序。

<img src="https://user-images.githubusercontent.com/45159366/189614458-d51a15cb-d02d-4b1f-9e77-e712dcdb1d73.png">

### EA Play 整合
[回到顶部](#目录)

[EA Play](https://lutris.net/games/ea-desktop/) 是电子艺术公司为Xbox One、Xbox Series X/S、PlayStation 4、PlayStation 5和微软视窗平台提供的基于订阅的视频游戏服务，提供由电子艺术公司出版的精选游戏以及额外的奖励。

<img src="https://user-images.githubusercontent.com/45159366/189614466-476e0c4e-bab9-44bd-86c4-8aeadd739b63.png">

### Origin 整合
[回到顶部](#目录)
 
[Origin](https://lutris.net/games/origin/) 是一个由电子艺界开发的在线游戏、数字发行和数字版权管理（DRM）平台，允许用户在互联网上购买PC和移动平台的游戏，并通过Origin客户端（以前的EA下载管理器、EA下载器和EA链接）下载游戏。

<img src="https://user-images.githubusercontent.com/45159366/189614468-49c4a05c-d6ca-4988-b3e6-10f0c71463d6.png">

### Ubisoft Connect 整合
[回到顶部](#目录)

[Ubisoft Connect](https://lutris.net/games/ubisoft-connect/) 是育碧创建的数字发行、数字版权管理、多人游戏和通信服务，提供类似于其他各游戏公司提供的成就/奖杯的体验。

<img src="https://user-images.githubusercontent.com/45159366/189614471-422cbad8-1ae7-4f06-ad81-7f3b68550569.png">

### GOG Galaxy 整合
[回到顶部](#目录)

[GOG GALAXY](https://lutris.net/games/gog-galaxy/) 是一个完全可选的客户端来安装、播放和更新您的游戏。

<img src="https://user-images.githubusercontent.com/45159366/189615528-385c01a8-f780-49e0-9502-db00d8082d9d.png"> 
        
## GameHub（游戏库）
[回到顶部](#目录)

[GameHub](https://github.com/tkashkin/GameHub) 是一个统一的库，用于存放您的所有游戏。它允许你将不同平台的游戏存储到一个程序中，使你更容易管理你的游戏。

<img src="https://user-images.githubusercontent.com/45159366/107862734-96451880-6e03-11eb-9b92-9d355b890083.png">

**GameHub 支持:**

 - 为Linux制作的游戏
 - **多个兼容层:**
   - Wine
   - Proton
   - [DOSBox](https://www.dosbox.com/)
   - [RetroArch](https://store.steampowered.com/app/1118310/RetroArch/)
   - [ScummVM](https://www.scummvm.org/)
   - [WineWrap](https://www.gog.com/forum/general/adamhms_linux_wine_wrappers_news_faq_discussion/post1) — 一套为支持的游戏 [supported games](https://www.gog.com/forum/general/adamhms_linux_wine_wrappers_news_faq_discussion/post3)预先配置的包装器;
   - custom emulators（定制模拟器）

 - **多个游戏平台:**
   - [Steam](https://store.steampowered.com/)
   - [GOG](https://www.gog.com/)
   - [Humble Bundle (including Humble Trove)](https://www.humblebundle.com/)
   - [itch.io](https://itch.io/)


## Epic 游戏商店
[回到顶部](#目录)

[Heroic](https://heroicgameslauncher.com/) 是一个适用于Linux、Windows和macOS的开源游戏启动器（适用于使用Crossover的本地和Windows游戏）。它支持使用Legendary从Epic Games Store启动游戏，这是Epic Games Launcher的CLI替代品。 [Flatpak for Heroic Games Launcher](https://flathub.org/apps/details/com.heroicgameslauncher.hgl)

[Epic Games Store](https://www.epicgames.com/store/) 是一个数字视频游戏店面支持微软Windows和macOS相同，由Epic Games运营。

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/111918016-3fed7a00-8a40-11eb-964e-930c801c1c72.png">
</p>

## Game Streaming（游戏串流）
[回到顶部](#目录)

[Geforce NOW](https://www.nvidia.com/en-us/geforce-now/download/) 是 NVIDIA 的云游戏服务

 <img src="https://user-images.githubusercontent.com/45159366/106686391-0f7c7a00-657f-11eb-9d0b-1ebb4d385883.jpeg">

[Moonlight Game Streaming](https://moonlight-stream.org/) 是一个程序，让你从你的PC游戏在互联网上流，不需要配置。无论你是在另一个房间还是在离你的游戏设备很远的地方，都可以从几乎任何设备上流媒体。 [Sunshine](https://github.com/LizardByte/Sunshine) 是应该 **Game stream host for Moonlight** 是一个自托管、低延迟的云游戏解决方案，支持AMD、英特尔和NVIDIA的GPU。

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/106686398-11463d80-657f-11eb-841a-d534829ccc3d.png">
</p>

[Chiaki](https://git.sr.ht/~thestr4ng3r/chiaki) 是一个用于PlayStation 4和PlayStation 5远程播放的自由和开源软件客户端，适用于Linux、FreeBSD、OpenBSD、Android、macOS、Windows、Nintendo Switch以及可能的更多平台。 [Chiaki Flatpak](https://flathub.org/apps/details/re.chiaki.Chiaki)

[Xbox Cloud Gaming](https://www.xbox.com/en-US/xbox-game-pass/cloud-gaming) 云游戏是微软基于云的Xbox游戏流技术 **(目前处于测试阶段)**。 **在你的移动设备或Chrome网络浏览器上玩像《地平线4》、《光环5：守护者》、《战争机器4》、《盗贼之海》、《Cuphead》、《红色生死线2》以及其他100多个游戏**。Xbox云游戏确实需要订阅 [Xbox Game Pass Ultimate](https://www.xbox.com/en-US/xbox-game-pass/cloud-gaming) 。

<img src="https://user-images.githubusercontent.com/45159366/108111388-74d56e00-7049-11eb-8aeb-3e5d65f9e832.png">

[Stadia](https://stadia.google.com/games) 是谷歌的游戏平台 **(谷歌将于2023年1月18日关闭其云游戏服务Stadia)**，可以让你在已经拥有的屏幕上即时玩你喜欢的视频游戏。在带有谷歌电视的Chromecast的电视、笔记本电脑、台式机、平板电脑或兼容手机上进行游戏。[Stadia Pro](https://stadia.google.com/) 订阅价格（每月9.99美元），可以解锁越来越多的免费游戏，在Stadia上玩。

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/162089471-3eb27f98-2366-4117-9af5-93bb126a2c37.png">
</p>

[Parsec](https://parsec.app/cloud-gaming) 是一个视频游戏流媒体平台，它提供各种游戏和类型的选择，并提供高质量和流畅的游戏体验。SParsec的开发目的是为了提供高质量的流畅游戏，同时没有任何广告和游戏内购买。

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/166166858-e70ca081-8931-46f3-9dc3-fe9c719d76f8.png">
</p>

[Amazon Luna](https://www.amazon.com/luna/landing-page) 是亚马逊的云游戏服务。亚马逊Luna在各种设备和浏览器上都是兼容/支持的。兼容列表： [Devices and Browsers](https://www.amazon.com/gp/help/customer/display.html?nodeId=GUFHUSX8X324T4XE).

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/112693072-364b8400-8e3d-11eb-9df0-d58af7ac9c9c.png">
</p>

## Game Emulators（游戏模拟器）
[回到顶部](#目录)

[EmuDeck](https://www.emudeck.com/) 是一个工具，它可以满足你的复古游戏需求，从RetroArch配置、边框、GameCube、Wii、Citra、SNES等的游戏手柄配置等一切。EmuDeck甚至会安装EmulationStation桌面版，并继承他们所有的自定义配置，不需要配置ROM路径或任何东西。

[EmulationStation Desktop Edition (ES-DE)](https://www.es-de.org/) 是一个前端应用程序，用于浏览和启动你的多平台游戏收藏。它可用于Unix/Linux、macOS（M1和Intel）和Windows。

[Pegasus](https://pegasus-frontend.org/) 是一个跨平台、可定制的图形前端，用于启动仿真器和管理你的游戏库（特别是复古游戏），并从一个地方启动它们。它专注于可定制性、跨平台支持（包括嵌入式设备）和高性能。

[RetroPie](https://retropie.org.uk/) 是一个模拟器的前端，允许你把你的Raspberry Pi、ODroid C1/C2或PC变成一个复古游戏机。它建立在Raspbian、 [EmulationStation](https://github.com/Aloshi/EmulationStation), RetroArch和许多其他项目的基础上，使你能够用最少的设置来玩你最喜欢的街机、家用游戏机和经典PC游戏。

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/153087555-e1bde100-6079-4089-a33d-804e29064789.png">
<br />
</p>

[RetroArch](https://www.retroarch.com/) 是一个模拟器、游戏引擎和媒体播放器的前端。它使你能够通过其顺滑的图形界面在各种计算机和游戏机上运行经典游戏。设置也是统一的，所以配置是一劳永逸的。 [RetroArch Flatpak](https://flathub.org/apps/details/org.libretro.RetroArch)

[Cartridge](https://github.com/unclebacon-live/cartridge) 是一个用Laravel+Vue.js制作的自我托管的游戏库。

**Cartridge 功能**

   - 扫描ROM文件并与IGDB游戏信息相匹配
   - 将ROM下载链接与游戏细节一起提供
   - 通过用户创建和权限管理对游戏库的访问(WIP)
   - 允许用户申请游戏 (计划中)
   - 使用JS仿真器在浏览器中播放选定的ROM（计划中）
   - 追踪已玩过的和最喜欢的游戏（即使是那些无法下载的游戏）（已计划）

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/172274231-d691a850-1879-44fb-8fa0-08e549d7bb29.png">
<br />
 Cartridge UI界面
</p>

[Dolphin](https://dolphin-emu.org) 是两个最新的任天堂视频游戏机的模拟器：GameCube和Wii。它允许PC玩家以全高清（1080p）享受这两个游戏机的游戏，并有多项增强功能：与所有PC控制器兼容、涡轮增速、联网多人游戏，甚至更多。 [Dolphin Flatpak](https://flathub.org/apps/details/org.DolphinEmu.dolphin-emu)

[Citra](https://citra-emu.org/) 是一个开源的任天堂3DS模拟器，能够玩许多你喜欢的游戏。[Citra Flatpak](https://flathub.org/apps/details/org.citra_emu.citra)

[yuzu](https://yuzu-emu.org) 是一个实验性的开源模拟器，用于任天堂Switch，由Citra的创造者开发。[Yuzu Flatpak](https://flathub.org/apps/details/org.yuzu_emu.yuzu)

[m64p](https://m64p.github.io/)  是一个任天堂64仿真器。它使用mupen64plus-gui，一个用Qt5编写的全新的mupen64plus前端。它支持所有你期望从一个前台得到的东西（保存状态管理、暂停、屏幕截图）。 [m64p Flatpak](https://flathub.org/apps/details/io.github.m64p.m64p)

[DeSmuME](https://desmume.org/) 是一个任天堂 NDS 模拟器。 [DeSmuME Flatpak](https://flathub.org/apps/details/org.desmume.DeSmuME)

[Snes9x](https://www.snes9x.com/) 是一个便携式、免费的超级任天堂娱乐系统（SNES）模拟器 [Snes9x Flatpak](https://flathub.org/apps/details/com.snes9x.Snes9x) 

[bsnes](https://github.com/bsnes-emu/bsnes) 是一个超级任天堂（SNES）模拟器，专注于性能、功能和易用性。[bsnes flatpak](https://flathub.org/apps/details/dev.bsnes.bsnes)

[mGBA](https://mgba.io/) 是一个运行Game Boy Advance游戏的新模拟器。它的目标是比许多现有的Game Boy Advance模拟器更快、更准确，以及增加其他模拟器所缺乏的功能。 [mGBA Flatpak](https://flathub.org/apps/details/io.mgba.mGBA)

[DOSBox](https://www.dosbox.com/) 是一个开源的DOS模拟器，主要侧重于运行DOS游戏。

[DOSBox Staging](https://github.com/dosbox-staging/dosbox-staging) 是一个完整的x86 CPU模拟器（与主机架构无关），能够运行需要真实或保护模式的DOS程序。 [DOSBox Staging Flatpak](https://flathub.org/apps/details/io.github.dosbox-staging)

[Flycast](https://github.com/flyinghead/flycast) 是一个源自reicast的多平台Sega Dreamcast、Naomi和Atomiswave模拟器。 [Flycast Flatpak](https://flathub.org/apps/details/org.flycast.Flycast)

[DuckStation](https://www.duckstation.org/) 是一个索尼PlayStation 1游戏机的模拟器/仿真器，专注于可玩性、速度和长期可维护性。 [Available as a Flatpak on Flathub](https://flathub.org/apps/details/org.duckstation.DuckStation).

[PCSX2](https://pcsx2.net/)  是一个PlayStation 2 "模拟器"，一个试图复制PlayStation 2控制台的免费程序，使你能够在你的PC上玩PS2游戏。 [PCSX2 Flatpak](https://flathub.org/apps/details/net.pcsx2.PCSX2)

[RPCS3](https://rpcs3.net/) 是一个实验性的开源索尼PlayStation 3模拟器和调试器，用C++语言编写，用于Windows和Linux。RPCS3于2011年5月由其创始人DH和Hykem开始开发。该模拟器目前能够运行超过1800个由Vulkan和OpenGL驱动的商业游戏。 [RPCS3 Flatpak](https://flathub.org/apps/details/net.rpcs3.RPCS3)

[MAME](https://www.mamedev.org/) 是一个街机模拟器。

[xemu](https://xemu.app/) 是一个原始的Xbox模拟器。

[Xenia](https://github.com/xenia-project/xenia) 是一个Xbox 360模拟器。

**还可以查看这些子版块，了解更多优秀的游戏模拟器推荐。**
  
   - [r/emulation](https://www.reddit.com/r/emulation/)
   - [r/emulations](https://www.reddit.com/r/emulators/)
   - [r/RetroArch](https://www.reddit.com/r/RetroArch/)
   - [r/RetroPie](https://www.reddit.com/r/RetroPie/)
   - [r/DolphinEmulator](https://www.reddit.com/r/DolphinEmulator/)
   - [r/Citra](https://www.reddit.com/r/Citra/)
   - [r/cemu](https://www.reddit.com/r/cemu/)
   - [r/yuzu](https://www.reddit.com/r/yuzu/)
   - [r/OpenEmu](https://www.reddit.com/r/OpenEmu/)
   - [r/MAME](https://www.reddit.com/r/MAME/)
   - [r/EmuDev](https://www.reddit.com/r/EmuDev/)
   - [r/Roms](https://www.reddit.com/r/Roms/)

# 游戏开发
[回到顶部](#目录)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/97361059-45151700-185c-11eb-9d12-dae51c79eb8a.png">
  <br />
</p>

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/119279021-ea6b5000-bbdd-11eb-9f59-5251fc3ac751.png">
  <br />
</p>

## Game Engines（游戏引擎）

**[Checkout the Unity Engine](https://unity.com/)**

<img src="https://user-images.githubusercontent.com/45159366/104788113-3432be00-5746-11eb-99b1-49360669f327.png">


**[Checkout the Unreal Engine 4](https://www.unrealengine.com/)**

<img src="https://user-images.githubusercontent.com/45159366/104788122-37c64500-5746-11eb-8f61-48a69b94582d.png">

**[Checkout the Godot Engine](https://godotengine.org/)**

[If you would like to Donate to the Godot Project](https://www.patreon.com/godotengine)

<img src="https://user-images.githubusercontent.com/45159366/104788134-3f85e980-5746-11eb-94c4-d97165ee888b.jpeg">


**[Checkout Blender](https://www.blender.org/)**

[If you would like to Donate to the Blender Project](https://fund.blender.org/)

<img src="https://user-images.githubusercontent.com/45159366/104788139-401e8000-5746-11eb-9647-058dee01a00e.png">


## 游戏开发学习资源

[Unreal Online Learning](https://www.unrealengine.com/en-US/onlinelearning-courses) 是一个免费的学习平台，提供实践视频课程和指导性学习路径。

[Unreal Engine Authorized Training Program](https://www.unrealengine.com/en-US/training-partners)

[Unreal Engine for education](https://www.unrealengine.com/en-US/education/)

[Unreal Engine Training & Simulation](https://www.unrealengine.com/en-US/industry/training-simulation)

[Unity Certifications](https://unity.com/products/unity-certifications)

[Autodesk for Games](https://www.autodesk.com/campaigns/autodesk-for-games)

[Getting Started with DirectX 12 Ultimate](https://devblogs.microsoft.com/directx/directx-12-ultimate-getting-started-guide/)

[Getting Started with Vulkan](https://www.khronos.org/vulkan/)

[Getting Started with Apple Metal](https://developer.apple.com/metal/)

[Game Design Online Courses from Udemy](https://www.udemy.com/courses/Design/Game-Design/)

[Game Design Online Courses from Skillshare](https://www.skillshare.com/browse/game-design)

[Learn Game Design with Online Courses and Classes from edX](https://www.edx.org/learn/game-design)

[Game Design Courses from Coursera](https://www.coursera.org/courses?query=game%20design)

[Game Design and Development Specialization Course from Coursera](https://www.coursera.org/specializations/game-development)

## 游戏开发工具

[Unreal Engine](https://www.unrealengine.com) 虚幻引擎是由Epic Games开发的游戏引擎，是世界上最开放、最先进的实时3D创作工具。持续不断地发展，不仅是为了满足其作为最先进的游戏引擎的最初目的，今天它为各行业的创作者提供了自由和控制，以提供最先进的内容、互动体验和沉浸式虚拟世界。

[Unity](https://unity.com) 是一个跨平台的游戏开发平台。使用Unity构建高质量的3D和2D游戏，在移动、桌面、VR/AR、游戏机或网络上部署这些游戏，并与忠实和热情的玩家和客户联系。

[Unigine](https://unigine.com) 是一个跨平台的游戏引擎，为开发团队（C++/C#程序员、3D艺术家）设计的互动3D应用程序。

[Blender](https://www.blender.org) 是免费和开源的3D创作套件。它支持整个3D管道--建模、索具、动画、模拟、渲染、合成和运动跟踪、视频编辑和2D动画管道。

[Godot](https://godotengine.org) 是一个功能丰富的跨平台游戏引擎，可以从一个统一的界面创建2D和3D游戏。它提供了一套全面的通用工具，因此用户可以专注于制作游戏而不必重新发明轮子。游戏可以一键导出到多个平台，包括主要的桌面平台（Linux、Mac OSX、Windows）以及移动（Android、iOS）和基于网络（HTML5）的平台。

[Panda3D](https://www.panda3d.org/) 是一个游戏引擎，一个用于Python和C++程序的3D渲染和游戏开发的框架，由迪士尼和CMU开发。Panda3D是开源的，可以免费用于任何目的，包括商业投资。

[Source 2](https://developer.valvesoftware.com/wiki/Source_2) 是Valve正在开发的一个3D视频游戏引擎，作为Source的继承者。它被用于《Dota 2》、《Artifact》、《Dota Underlords》、《The Lab》的部分内容、SteamVR Home和《半条命》。Alyx。

[Havok](https://www.havok.com/) 是一个中间件软件套件，为视频游戏提供现实的物理引擎组件和相关功能。它得到了所有主要平台的支持和优化，包括Nintendo Switch、PlayStation®、Stadia和Xbox。随着Unity和虚幻引擎的整合，并被用于无数的专有游戏引擎中。

[AutoDesk 3ds Max](https://www.autodesk.com/products/3ds-max/overview) 是一款用于3D建模、动画、渲染和可视化的专业软件程序。3ds Max允许你创建令人惊叹的游戏环境、设计可视化和虚拟现实体验。

[Houdini](https://www.sidefx.com/) 是一个三维程序软件，用于电影、电视、广告和视频游戏管道中的建模、装配、动画、视觉特效、外观开发、照明和渲染。

[A-Frame](https://aframe.io) 是一个用HTML和Entity-Component在WebVR中构建虚拟现实体验的网络框架。A-Frame可以在Vive、Rift、桌面、移动平台上使用。

[AppGameKit](https://www.appgamekit.com) 是一个强大的游戏开发引擎，是业余爱好者和独立开发者的理想选择。你可以在易于学习的AppGameKit BASIC中开始编码，或使用C++和XCode中的库。

[Open Graphics Library(OpenGL)](https://www.opengl.org/) 是一个跨越多种编程语言和平台的API，用于硬件加速渲染2D/3D矢量图形，目前由 [Khronos Group](https://www.khronos.org/) 开发。

[Open Computing Language (OpenCL)](https://www.khronos.org/opencl/) 是一个开放的标准，用于 [parallel programming](https://www.coursera.org/lecture/parprog1/introduction-to-parallel-computing-zNrIS) 。 由CPU、GPU和其他超级计算机、云服务器、个人电脑、移动设备和嵌入式平台中的硬件加速器组成的异构平台的开放标准。

[OpenGL Shading Language(GLSL)](https://www.khronos.org/opengl/wiki/Core_Language_(GLSL)) 是一种基于C语言的高级着色语言，所以它涵盖了用户对这种语言所期望的大部分功能。如控制结构（for-loops，if-else语句等）在GLSL中存在，包括switch语句。

[High Level Shading Language(HLSL)](https://docs.microsoft.com/en-us/windows/win32/direct3dhlsl/dx-graphics-hlsl) 是DirectX的高级着色语言。使用HLSL，用户可以为Direct3D管道创建类似C语言的可编程着色器。HLSL最初是与DirectX 9一起创建的，用于建立可编程的3D管道。

[DirectX 12 Ultimate](https://github.com/Microsoft/DirectX-Graphics-Samples) 是微软的一个API（用于高性能的2D和3D图形）。DirectX 12 Ultimate带来了对光线追踪、网格着色器、可变速率着色和采样器反馈的支持。在Windows 2004版本中可用（2020年5月更新）。

[Vulkan](https://www.khronos.org/vulkan/) 是一个现代的跨平台图形和计算API，它提供了对现代GPU的高效、跨平台的访问，这些GPU用于从PC和游戏机到移动电话和嵌入式平台的各种设备。Vulkan目前正由Khronos集团联盟开发。

[Mesa 3D Graphics Library](https://docs.mesa3d.org/index.html) 图形库是一个开始作为OpenGL规范的开源实现的项目。一个用于渲染交互式3D图形的系统。Mesa与其他几个开源项目联系在一起： [Direct Rendering Infrastructure](https://dri.freedesktop.org/), [X.org](https://x.org/), 和 [Wayland](https://wayland.freedesktop.org/) ，在Linux、FreeBSD和其他操作系统上提供OpenGL支持。

[OpenGL ES](https://www.khronos.org/opengles/) 是OpenGL的移动子集。它被所有主要的移动平台所支持，也是WebGL的基础。

[OpenCL](https://www.khronos.org/opencl/) 是一个编写程序的框架，可以在由CPU、GPU、DSP、FPGA和其他处理器或硬件加速器组成的异构平台上执行。

[EGL](https://www.khronos.org/egl/) 是Khronos渲染API（如OpenGL或OpenVG）与底层原生平台窗口系统之间的一个接口。

[VDPAU](https://www.freedesktop.org/wiki/Software/VDPAU/) 是UNIX的视频解码和演示API。它为现代GPU中的视频解码加速和演示硬件提供了一个接口。

[VA API](https://freedesktop.org/wiki/Software/vaapi/) 是一个开源的库和API规范，它提供了对视频处理的图形硬件加速能力的访问。

[XvMC](https://en.wikipedia.org/wiki/X-Video_Motion_Compensation) 是X窗口系统的X视频扩展（Xv）的一个扩展。XvMC API允许视频程序将视频解码过程的部分内容卸载到GPU硬件上。

[AMD Radeon ProRender](https://www.amd.com/en/technologies/radeon-prorender) 是一个强大的基于物理的渲染引擎，使创意专业人士能够在几乎任何GPU、任何CPU和任何操作系统上，在十多个领先的数字内容创作和CAD应用程序中产生惊人的逼真图像。

[NVIDIA Omniverse](https://developer.nvidia.com/nvidia-omniverse-platform) 是一个强大的多GPU实时模拟和协作平台，适用于基于皮克斯的通用场景描述和NVIDIA RTX的3D制作管道。

[LibGDX](https://github.com/libgdx/libgdx) 是一个基于OpenGL（ES）的跨平台Java游戏开发框架，可以在Windows、Linux、Mac OS X、Android、支持WebGL的浏览器和iOS上运行。

[cocos2d-x](https://github.com/cocos2d/cocos2d-x) 是一个多平台框架，用于构建2D游戏、交互式书籍、演示和其他图形应用程序。它基于cocos2d-iphone，但没有使用Objective-C，而是使用C++。它可以在iOS、Android、macOS、Windows和Linux上运行。

[MonoGame](https://github.com/MonoGame/MonoGame) 是一个用于创建强大的跨平台游戏的框架。它是XNA的精神继承者，在桌面、移动和控制台平台上有数千款游戏。MonoGame是一个完全管理的.NET开源游戏框架，没有任何黑盒子。
[Three.js](https://threejs.org) 是一个跨浏览器的JavaScript库和应用编程接口，用于在网络浏览器中使用WebGL创建和显示动画的三维计算机图形。

[Superpowers](http://superpowers-html5.com/) 是一个可下载的HTML5应用程序，用于实时协作项目。你可以像普通的离线游戏制作者一样单独使用它，或者设置一个密码，让朋友通过他们的网络浏览器加入到你的项目中。

[URHO3D](https://urho3d.github.io/) 是一个免费的轻量级、跨平台的2D和3D游戏引擎，用C++实现，并在MIT许可下发布。受到OGRE和Horde3D的极大启发。

[Vivox](https://www.vivox.com/) 是一个语音和文本聊天平台，受到世界上最大的游戏品牌和游戏作品的信任，如《堡垒之夜》、《PUBG》、《英雄联盟》和《彩虹六号》。

[HGIG](https://www.hgig.org/) 是一个由游戏和电视显示行业的公司组成的志愿团体，他们开会指定并向公众提供指导方针，以改善消费者在HDR下的游戏体验。

[GameBlocks](https://www.gameblocks.com/) 是一款服务器端反作弊和中间件软件。

# Vulkan 开发
[回到顶部](#目录)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/129622224-8c4cca51-9200-4d70-9d16-2610d704713a.png">
  <br />
</p>

## Vulkan 学习资源

[Vulkan®](https://www.khronos.org/vulkan/) 是一个现代的跨平台图形和计算API，它提供了对现代GPU的高效、跨平台的访问，这些GPU用于从PC和游戏机到移动电话和嵌入式平台的各种设备。Vulkan目前正在由Khronos联盟开发。

[Khronos Group GitHub](https://github.com/KhronosGroup)

[Vulkan Documentation](https://github.com/KhronosGroup/Vulkan-Docs)

[HLSL to SPIR-V Feature Mapping Manual](https://github.com/microsoft/DirectXShaderCompiler/blob/master/docs/SPIR-V.rst)

[Vulkan GLSL Ray Tracing Emulator Tutorial](https://www.gsn-lib.org/docs/nodes/raytracing.php)

[Getting Started with Vulkan](https://vulkan-tutorial.com/)

[Vulkan Samples](https://github.com/KhronosGroup/Vulkan-Samples)

[Khronos Community Forums](https://community.khronos.org/)

## Vulkan 工具、库和框架

[Vulkan SDK](https://vulkan.lunarg.com) 是一套工具，使Vulkan开发者能够开发Vulkan应用程序。

[SPIR-V](https://www.khronos.org/spir/) 是一套工具，使高级语言前端能够以标准化的中间形式发射程序，以便被Vulkan、OpenGL或OpenCL驱动程序接收。它消除了设备驱动程序中对高级语言前端编译器的需求，大大降低了驱动程序的复杂性，使广泛的语言和框架前端能够在不同的硬件架构上运行，并鼓励一个充满活力的开源分析、移植、调试和优化工具的生态系统。

[SPIRV-Reflect](https://github.com/KhronosGroup/SPIRV-Reflect) 是一个轻量级的库，为Vulkan应用程序中的SPIR-V着色器字节码提供C/C++反射API。

[Vulkan® Tools](https://github.com/KhronosGroup/Vulkan-Tools) 是一个项目，为Windows、Linux、Android和macOS提供Khronos集团的官方Vulkan工具和实用程序。

[Vulkan-Hpp](https://github.com/KhronosGroup/Vulkan-Hpp) 是一个API，它为Vulkan C API提供了一个只有头的C++绑定，以改善开发者的Vulkan体验，而不引入CPU运行时间成本。它增加了诸如枚举和比特域的类型安全、STL容器支持、异常和简单枚举等功能。

[Vulkan® Memory Allocator (VMA)](https://gpuopen.com/vulkan-memory-allocator/) 是一个库，它提供了一个简单且易于集成的API，帮助你为Vulkan®缓冲区和图像存储分配内存。

[AMD Open Source Driver for Vulkan®](https://gpuopen.com/amd-open-source-driver-for-vulkan/) 是一个开源的Vulkan驱动程序，用于Linux®上的AMD Radeon™图形适配器。

[NVIDIA® Nsight™ Visual Studio Edition](https://developer.nvidia.com/nsight-visual-studio-edition) 是一个适用于异构平台的应用开发环境，它将GPU计算引入了Microsoft Visual Studio。通过NVIDIA Nsight™ VSE，用户可以构建和调试集成GPU内核和本地CPU代码，并检查GPU和内存的状态。

[Radeon™ GPU Profiler](https://gpuopen.com/rgp/) 是一个性能工具，可供开发人员用于优化DirectX®12、Vulkan®和OpenCL™应用程序，以适应AMD RDNA™和GCN硬件。

[Radeon™ GPU Analyzer](https://gpuopen.com/rga/) 是一款用于Vulkan®、DirectX®、OpenGL®和OpenCL™的编译器和代码分析工具。

[Radeon™ Memory Visualizer (RMV)](https://gpuopen.com/rmv/) 是AMD提供给游戏引擎开发者使用的工具。它允许工程师检查、诊断和了解他们项目中的GPU内存管理。

[DXVK](https://github.com/doitsujin/dxvk) 是一个基于Vulkan的Direct3D 9/10/11翻译层，它允许使用Wine在Linux上运行3D应用程序。

[MoltenVK](https://moltengl.com/moltenvk) 是在iOS和macOS上使用苹果的 [Metal](https://developer.apple.com/metal/) 图形框架运行的Vulkan的一个实现。

[RenderDoc](https://renderdoc.org) 是一个独立的图形调试器，它允许快速和简单的单帧捕获和详细反省任何使用Vulkan、D3D11、OpenGL和OpenGL ES或D3D12的应用程序，跨越Windows、Linux、Android、Stadia或Nintendo Switch™。

[PerfDoc](https://github.com/ARM-software/perfdoc) 是一个跨平台的Vulkan层，用于检查Vulkan应用程序在 [best practices on Arm Mali](https://developer.arm.com/graphics/developer-guides/mali-gpu-best-practices) 设备上。

[GLFW](https://www.glfw.org/) 是一个用于OpenGL、OpenGL ES和Vulkan应用开发的开源、多平台库。它提供了一个简单的、与平台无关的API，用于创建窗口、上下文和表面、读取输入、处理事件等。GLFW原生支持Windows、macOS和Linux及其他类Unix系统。在Linux上，X11和Wayland都被支持。

[VulkanSharp](https://github.com/mono/VulkanSharp) 是一个为Vulkan API提供.NET绑定的项目。

[Vortice.Vulkan](https://github.com/amerkoleci/Vortice.Vulkan) 是一个针对Vulkan API的.NET标准2.0和.NET5低级绑定。

[VKD3D-Proton](https://github.com/HansKristian-Work/vkd3d-proton) 是VKD3D的一个分叉，其目的是在Vulkan之上实现完整的Direct3D 12 API。

[ImGui](https://github.com/ocornut/imgui) 是一个适用于C++的无臃肿的图形用户接口库。它输出优化的顶点缓冲区，你可以在你的支持3D管道的应用程序中随时渲染。它速度快、可移植、与渲染器无关、自成一体（没有外部依赖性）。

[Ash](https://github.com/MaikKlein/ash) 是一个非常轻量级的Vulkan封装器。

[gfx-rs](https://github.com/gfx-rs/gfx) 是一个低级的、跨平台的Rust图形和计算抽象库。

[Vulkan.jl](https://github.com/JuliaGPU/Vulkan.jl) 是一个围绕Vulkan图形和计算库的轻量级包装器。它在底层的C接口上暴露了一些抽象，主要面向那些寻找一种更自然的方式以最小的开销来处理Vulkan的开发者。

# DirectX 开发
[回到顶部](#目录)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/142779599-6a46ab05-c64a-48fe-a775-3e4f46e41f63.png">
  <br />
</p>

## DirectX 学习资源

[Microsoft DirectX®](https://support.microsoft.com/en-us/topic/how-to-install-the-latest-version-of-directx-d1f5ffa5-dae2-246c-91b1-ee1e973ed8c2) 是一个低级别的API，处理与微软平台（Windows和Xbox）上的游戏编程和视频的多媒体有关的任务。

[Getting Started with DirectX 12 Ultimate](https://devblogs.microsoft.com/directx/directx-12-ultimate-getting-started-guide/)

[Getting Started with the DirectX 12 Agility SDK](https://devblogs.microsoft.com/directx/gettingstarted-dx12agility/)

[DirectX 12 and Graphics Education | YouTube](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)

[DirectX— Feature Level 12_2](https://devblogs.microsoft.com/directx/new-in-directx-feature-level-12_2/)

[DirectX 12 Technology | NVIDIA](https://www.nvidia.com/en-us/geforce/technologies/dx12/)

[AMD DirectX® 12 (DX12) Technology | AMD](https://www.amd.com/en/technologies/directx12)

[Top Microsoft DirectX Courses Online | Udemy](https://www.udemy.com/topic/microsoft-directx/)

[DirectX - Learn Microsoft DirectX from Scratch Course | Udemy](https://www.udemy.com/course/directx-learn-microsoft-directx-from-scratch/)

[DirectX 11 Programming Course | Udemy](https://www.udemy.com/course/directx11/)

## DirectX 工具、库和框架

[Visual Studio](https://visualstudio.microsoft.com/) 是微软的一个集成开发环境（IDE）；它是一个功能丰富的应用程序，可用于软件开发的许多方面。Visual Studio使编辑、调试、构建和发布你的应用程序变得容易。通过使用微软的软件开发平台，如Windows API、Windows Forms、Windows Presentation Foundation和Windows Store。

[Visual Studio Code](https://code.visualstudio.com/) 是一个为构建和调试现代网络和云应用程序而重新定义和优化的开源代码编辑器。

[DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) 是一个包含DirectX 12图形样本的项目，演示了如何为Windows 10构建图形密集型应用程序。

[PIX on Windows](https://devblogs.microsoft.com/pix/documentation/) 是一个用于Windows上的DirectX 12游戏的性能调整和调试工具。

[DirectStorage API](https://devblogs.microsoft.com/directx/directstorage-is-coming-to-pc/) 是DirectX系列的一个API，最初是为Windows的 [Velocity Architecture](https://news.xbox.com/en-us/2020/07/14/a-closer-look-at-xbox-velocity-architecture/) DirectX API的设计方式考虑到了所有这些，并在从NVMe驱动器一直到GPU的整个管道中实现了性能最大化。它在几个方面做到了这一点：通过减少每个请求的NVMe开销，实现分批多次的并行IO请求，可以有效地输送到GPU，并让游戏对何时得到IO请求完成的通知有更精细的控制，而不是对每个微小的IO完成做出反应。DirectStorage API将在装有NVMe固态硬盘的 [Windows 11](https://www.microsoft.com/en-us/windows/windows-11) 电脑上使用，但也将在 [Windows 10](https://www.microsoft.com/software-download/windows10) version 1909版和更新的版本中得到支持。

[NVIDIA® Nsight™ Visual Studio Edition](https://developer.nvidia.com/nsight-visual-studio-edition) 是一个适用于异构平台的应用开发环境，它将GPU计算引入了Microsoft Visual Studio。通过NVIDIA Nsight™ VSE，用户可以构建和调试集成GPU内核和本地CPU代码，并检查GPU和内存的状态。

[NVRHI (NVIDIA Rendering Hardware Interface)](https://github.com/NVIDIAGameWorks/nvrhi) 是一个库，它在多个图形API（GAPI）上实现了一个通用抽象层。Direct3D 11、Direct3D 12和Vulkan 1.2。它可以在Windows（仅x64）和Linux（x64和ARM64）上运行。

[RTXMU - RTX Memory Utility SDK](https://github.com/NVIDIAGameWorks/RTXMU) 是一个SDK工具，它将所有加速结构的构建输入批量化，并将其传递给RTXMU，后者将执行所有的子分配内存请求和构建细节，包括压实。然后，SDK将构建后的信息抽象出来，以便在引擎下进行压实。RTXMU返回加速结构的句柄ID，用于引用底层内存缓冲区。这些句柄ID被传递到RTXMU中，以创建压缩拷贝工作负载，取消分配未使用的构建资源或移除与加速结构相关的所有内存。

[Radeon™ GPU Profiler](https://gpuopen.com/rgp/) 是一个性能工具，可供开发人员用于优化DirectX®12、Vulkan®和OpenCL™应用程序，以适应AMD RDNA™和GCN硬件。

[Radeon™ GPU Analyzer](https://gpuopen.com/rga/) 是一款用于Vulkan®、DirectX®、OpenGL®和OpenCL™的编译器和代码分析工具。

[Radeon™ Memory Visualizer (RMV)](https://gpuopen.com/rmv/) 是AMD提供给游戏引擎开发者使用的工具。它允许工程师检查、诊断和了解他们项目中的GPU内存管理。

[FNA](https://fna-xna.github.io/) 是一个XNA4的重新实现，只专注于为桌面开发一个完全准确的XNA4运行时间。

[FAudio](https://fna-xna.github.io/) 是一个XAudio的重新实现，它只专注于为FNA项目开发完全精确的DirectX音频运行库，包括 [XAudio2](https://docs.microsoft.com/en-us/windows/win32/xaudio2/xaudio2-introduction), [X3DAudio](https://docs.microsoft.com/en-us/windows/win32/xaudio2/x3daudio-overview), [XAPO](https://docs.microsoft.com/en-us/windows/win32/xaudio2/xapo-overview), 和 [XACT3](https://en.wikipedia.org/wiki/Cross-platform_Audio_Creation_Tool).

[Simple DirectMedia Layer](https://www.libsdl.org/) 是一个跨平台的开发库，旨在通过OpenGL和Direct3D提供对音频、键盘、鼠标、操纵杆和图形硬件的低水平访问。它被视频播放软件、仿真器和流行的游戏所使用，包括Valve的获奖目录。

[DXVK](https://github.com/doitsujin/dxvk) 是一个基于Vulkan的Direct3D 9/10/11翻译层，它允许使用Wine在Linux上运行3D应用程序。

[VKD3D-Proton](https://github.com/HansKristian-Work/vkd3d-proton) 是VKD3D的一个分叉，其目的是在Vulkan之上实现完整的Direct3D 12 API。

[RenderDoc](https://renderdoc.org) 是一个独立的图形调试器，它允许快速和简单的单帧捕获和详细反省任何使用Vulkan、D3D11、OpenGL和OpenGL ES或D3D12的应用程序，跨越Windows、Linux、Android、Stadia或Nintendo Switch™。

# OpenGL 开发
[回到顶部](#目录)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/131386211-f507b5d4-a3c9-4c21-aadd-2aa5bde94d1e.png">
  <br />
</p>

## OpenGL 学习资源

[Open Graphics Library(OpenGL)™](https://www.opengl.org/) 是一个跨越多种编程语言和平台的API，用于硬件加速渲染2D/3D矢量图形，目前由 [Khronos Group](https://www.khronos.org/)开发。

[OpenGL ES™](https://www.khronos.org/opengles/) 是OpenGL for Embedded Systems（ES）的移动子集。它被所有主要的移动平台所支持，也是WebGL的基础。

[WebGL™](https://www.khronos.org/webgl/) 是一个跨平台、免版税的网络标准，是基于OpenGL ES的低级3D图形API，通过HTML5 Canvas元素暴露给JavaScript。

[Khronos Group | GitHub](https://github.com/KhronosGroup/)

[Khronos Technology Courses and Training](https://www.khronos.org/developers/training/)

[Top OpenGL Courses Online | Coursera](https://www.coursera.org/courses?query=opengl&amp;page=1)

[Top OpenGL Courses Online | Udemy](https://www.udemy.com/topic/opengl/)

[OpenGL Online Training Courses | LinkedIn Learning](https://www.linkedin.com/learning/topics/opengl)

[Getting Started with OpenGL](https://www.khronos.org/opengl/wiki/Getting_Started)

[OpenGL Reference Cards](https://www.khronos.org/developers/reference-cards/)

[Getting Started with OpenGL ES](https://www.khronos.org/opengles/)

[OpenGL ES Reference Cards](https://www.khronos.org/developers/reference-cards/)

[Getting Started with WebGL](https://www.khronos.org/webgl/)

[WebGL 2.0 Specification](https://www.khronos.org/registry/webgl/specs/latest/2.0/)

[WebGL Public Wiki](https://www.khronos.org/webgl/wiki)

[WebGL Reference Cards](https://www.khronos.org/developers/reference-cards/)

## OpenGL 工具、库和框架

[BuGLe](https://www.opengl.org/sdk/tools/BuGLe/) 是一个用于Linux和其他UNIX-like操作系统的调试器。BuGLe将一个图形化的OpenGL调试器与OpenGL命令流的过滤器结合起来。调试器允许查看状态、纹理、帧缓冲器和着色器，而过滤器允许记录、错误检查、视频捕获等。

[gDEBugger](https://www.opengl.org/sdk/tools/gDEBugger/) 是一个全功能的免费调试器和分析器，代表了Windows和Linux上OpenGL和OpenGL ES调试和分析的最先进水平。

[KTX](http://www.khronos.org/opengles/sdk/tools/KTX/) 是一种轻量级的文件格式，用于向OpenGL系列API传递纹理。

[RenderDoc](https://renderdoc.org) 是一个独立的图形调试器，它允许快速和简单的单帧捕获和详细反省任何使用Vulkan、D3D11、OpenGL和OpenGL ES或D3D12的应用程序，跨越Windows、Linux、Android、Stadia或Nintendo Switch™。

[NVIDIA® Nsight™ Visual Studio Edition](https://developer.nvidia.com/nsight-visual-studio-edition) 是一个适用于异构平台的应用开发环境，它将GPU计算引入了Microsoft Visual Studio。通过NVIDIA Nsight™ VSE，用户可以构建和调试集成GPU内核和本地CPU代码，并检查GPU和内存的状态。

[Radeon™ GPU Profiler](https://gpuopen.com/rgp/) 是一个性能工具，可供开发人员用于优化DirectX®12、Vulkan®和OpenCL™应用程序，以适应AMD RDNA™和GCN硬件。

[Radeon™ GPU Analyzer](https://gpuopen.com/rga/) 是一款用于Vulkan®、DirectX®、OpenGL®和OpenCL™的编译器和代码分析工具。

[AMD Radeon ProRender](https://www.amd.com/en/technologies/radeon-prorender) 是一个强大的基于物理的渲染引擎，使创意专业人士能够在几乎任何GPU、任何CPU和任何操作系统上，在十多个领先的数字内容创作和CAD应用程序中产生惊人的逼真图像。

[NVIDIA Omniverse](https://developer.nvidia.com/nvidia-omniverse-platform) 是一个强大的多GPU实时模拟和协作平台，适用于基于皮克斯的通用场景描述和NVIDIA RTX的3D制作管道。

[MoltenGL](https://moltengl.com) 是OpenGL ES 2.0 API的一个实现，在苹果的 [Metal](https://developer.apple.com/metal/) 图形框架上运行。

[EGL](https://www.khronos.org/egl/) 是Khronos渲染API（如OpenGL或OpenVG）与底层原生平台窗口系统之间的一个接口。

[Equalizer](https://www.opengl.org/sdk/libs/Equalizer/) 是一个开源的编程接口和资源管理系统，用于可扩展的OpenGL应用程序。Equalizer应用程序可以部署在任何可视化系统上，从单管工作站到大规模的图形集群。

[GLee](https://www.opengl.org/sdk/libs/GLee/) 是一个免费的跨平台扩展加载库，为您的应用程序减轻负担。GLee使检查OpenGL扩展和核心版本的可用性变得很容易，自动设置入口点，而不需要你的努力。

[GLEW](https://www.opengl.org/sdk/libs/GLEW/) 是一个开源的跨平台扩展加载库，对多个渲染上下文和自动代码生成能力提供线程安全支持。GLEW为检查OpenGL扩展和核心功能提供了易于使用和高效的方法。

[GLUS](https://www.opengl.org/sdk/libs/GLUS) 是一个开源的C语言库，它提供了一个硬件和操作系统的抽象，以及使用OpenGL、OpenGL ES或OpenVG进行图形编程时通常需要的许多功能。

[OpenGL Mathematics (GLM)](http://glm.g-truc.net/) 是一个基于OpenGL着色语言（GLSL）规范的3D软件的C++数学库。

[libktx](http://www.khronos.org/opengles/sdk/tools/KTX/index.php#libktx) 是一个函数库（[KTX工具集](http://www.khronos.org/opengles/sdk/tools/KTX)的一部分），用于编写 [KTX format files](http://www.khronos.org/opengles/sdk/tools/KTX/file_format_spec/) ，并从中实例化GL纹理。

[OpenSceneGraph](https://www.opengl.org/sdk/libs/OpenSceneGraph/) 是一个高水平的3D图形工具包，它暴露了OpenGL的功能，同时提供了许多自己的功能。OpenSceneGraph拥有一个庞大的用户社区，并已被用于视觉模拟、游戏、虚拟现实、科学可视化和建模。

[Mesa 3D Graphics Library](https://docs.mesa3d.org/index.html) 是一个开始作为OpenGL规范的开源实现的项目。一个用于渲染交互式3D图形的系统。Mesa与其他几个开源项目联系在一起： [Direct Rendering Infrastructure](https://dri.freedesktop.org/), [X.org](https://x.org/), 和 [Wayland](https://wayland.freedesktop.org/)，在Linux、FreeBSD和其他操作系统上提供OpenGL支持

# Wayland 开发
[回到顶部](#目录)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/104235197-79cf4e00-5409-11eb-97a6-a12f7bd8ad2a.png">
  <br />
</p>

## Wayland 学习资源

[Wayland](https://wayland.freedesktop.org) 是一个让合成器与其客户端对话的协议，也是该协议的C库实现。合成器可以是运行在Linux内核模式设置和evdev输入设备上的独立显示服务器、X应用程序 [X application](https://www.x.org/wiki/XServer/) 或Wayland客户端本身。

[Wayland Architecture](https://wayland.freedesktop.org/architecture.html)

[Wayland Documentation](https://wayland.freedesktop.org/docs/html/)

[Sotfware Toolkits that have Wayland support right now](https://wayland.freedesktop.org/toolkits.html)

[Contribution instructions for Wayland](https://gitlab.freedesktop.org/wayland/wayland/blob/master/CONTRIBUTING.md)

[Contribution instructions for Weston](https://gitlab.freedesktop.org/wayland/weston/blob/master/CONTRIBUTING.md)

[Reporting Wayland bugs](https://gitlab.freedesktop.org/wayland/wayland/issues)

[Reporting Weston bugs](https://gitlab.freedesktop.org/wayland/weston/issues)

[WSLG: X11 and Wayland Applications in Windows Subsystem for Linux(WSL2)](https://linuxplumbersconf.org/event/9/contributions/611/attachments/702/1298/XDC2020_-_X11_and_Wayland_applications_in_WSL.pdf)

[Qt Wayland Compositor](https://doc.qt.io/qt-5/qtwaylandcompositor-index.html)

[Qt Wayland Compositor Examples](https://doc.qt.io/qt-5/qtwaylandcompositor-examples.html)

[Wayland on ArchWiki](https://wiki.archlinux.org/index.php/Wayland)

[Sway on ArchWiki](https://wiki.archlinux.org/index.php/Sway)

[Wayland on Ubuntu Wiki](https://wiki.ubuntu.com/Wayland)

[Wayland on Debian Wiki](https://wiki.debian.org/Wayland)

[The Wayland Display Server on Fedora Docs](https://docs.fedoraproject.org/en-US/fedora/rawhide/system-administrators-guide/Wayland/)

[Wayland features on Fedora Project Wiki](https://fedoraproject.org/wiki/Wayland_features)

[Wayland on GNOME Wiki](https://wiki.gnome.org/Initiatives/Wayland)

[KWin/Wayland on KDE Community Wiki](https://community.kde.org/index.php?title=KWin/Wayland)

[Wayland Desktop Landscape on Gentoo Wiki](https://wiki.gentoo.org/wiki/Wayland_Desktop_Landscape)

[Wayland in Void Linux Handbook](https://docs.voidlinux.org/config/graphical-session/wayland.html)

[Wayland on Enlightenment DE](https://www.enlightenment.org/about-wayland)

## Wayland 工具

[Weston](https://gitlab.freedesktop.org/wayland/weston) 是一个轻量级和功能性的Wayland合成器。

[XWayland](https://wayland.freedesktop.org/xserver.html) 是一个作为Wayland客户端运行的X服务器(为了向后兼容)，允许 [Xorg server](https://www.x.org/wiki/XServer/) 可以修改为使用wayland输入设备进行输入，并将根窗口或单个顶层窗口作为wayland表面进行转发。

[KWin](https://community.kde.org/KWin/Wayland) 是KDE Plasma桌面的窗口管理器。它让你完全控制你的窗口，确保它们不碍事，而是帮助你完成任务。它绘制了窗口的装饰，每个窗口顶部的栏都有（可配置的）按钮，如关闭、最大化和最小化。

[Qt](https://www.qt.io/) 是创建创新设备、现代UI和多屏幕应用程序的更快、更智能的方式。它是Wayland和X11窗口的最受欢迎的工具包之一。

[GTK](https://www.gtk.org/) 是由 [GNOME Project](https://www.gnome.org/) 项目开发的用于创建图形用户界面的免费和开源的跨平台部件工具包。它是Wayland和X11视窗的最流行工具包之一。

[NVIDIA Wayland EGL External Platform library](https://github.com/NVIDIA/egl-wayland) 是一个正在进行中的EGL外部平台库的实现，用于在EGLDevice和EGLStream系列扩展之上为EGL增加客户端Wayland支持。

[NVIDIA EGL External Platform Interface](https://github.com/NVIDIA/eglexternalplatform) 是一个正在制定的EGL外部平台接口规范，用于在现有的低级EGL平台实现之上编写EGL平台及其与现代窗口系统的互动。通过使用面向应用程序的EGL函数，这使得窗口系统实现的具体细节不在EGL驱动程序中。

[Sway](https://swaywm.org/) 是一个与 [i3](https://i3wm.org/)兼容的Wayland合成器。

[wlroots](https://github.com/swaywm/wlroots) is a modular Wayland compositor library.

[WayfireWM](https://github.com/WayfireWM/wayfire) 是一个3D Wayland合成器，其灵感来自于 [Compiz](https://launchpad.net/compiz) 并基于 [wlroots](https://github.com/swaywm/wlroots).

[SDDM](https://github.com/sddm/sddm) 是一个用于X11和Wayland的现代显示管理器，旨在实现快速、简单和美观。它使用了像QtQuick这样的现代技术，这反过来又使设计者有能力创建流畅的、有动画的用户界面。

[x11docker](https://github.com/mviereck/x11docker) 是一个应用程序，它允许在Docker Linux容器中运行图形化桌面应用程序（和整个桌面）。

[Mako](https://github.com/emersion/mako) 是一个用于Wayland的轻量级通知守护程序。它也可以在 [Sway](https://swaywm.org/) 上工作。

[Wayland-rs](https://github.com/Smithay/wayland-rs) 是wayland协议（客户端和服务器）的Rust实现。

[Wine-wayland](https://github.com/varmd/wine-wayland) 是一个允许你使用纯Wayland和Wine/DXVK运行DX9/DX11和Vulkan游戏的应用程序。

# Audio 音频开发
[回到顶部](#目录)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/142936394-b546784e-231a-4391-9dd8-c686e5a7eee9.png">
  <br />
</p>

## 音频学习资源

[How Audio is implemented with PipeWire](https://docs.pipewire.org/page_audio.html)

[PipeWire Design](https://docs.pipewire.org/page_pipewire.html)

[PipeWire Library](https://docs.pipewire.org/page_library.html)

[DMA-BUF sharing](https://docs.pipewire.org/page_dma_buf.html)

[PipeWire Daemon](https://docs.pipewire.org/page_daemon.html)

[PipeWire Tools](https://docs.pipewire.org/page_tools.html)

[PipeWire Session Manager](https://docs.pipewire.org/page_session_manager.html)

[PipeWire Modules](https://docs.pipewire.org/page_pipewire_modules.html)

[PipeWire API](https://docs.pipewire.org/page_api.html)

   - [Client Implementation（客户端信息）](https://docs.pipewire.org/page_client_impl.html)
   - [Proxy（代理）](https://docs.pipewire.org/page_proxy.html)
   - [Streams（流）](https://docs.pipewire.org/page_streams.html)
   - [Thread Loop（线程池）](https://docs.pipewire.org/page_thread_loop.html)

[WirePlumber 文档](https://pipewire.pages.freedesktop.org/wireplumber/)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/142779615-d631251b-a2d6-48b4-8194-7985604a8563.png">
  <br />
</p>

WirePlumber，PipeWire会话管理器如何工作。来源: [Collabora](https://www.collabora.com/news-and-blog/blog/2020/05/07/wireplumber-the-pipewire-session-manager/)

## Audio Tools（音频工具）

[PipeWire](https://pipewire.org) 是一个处理多媒体管道的服务器和用户空间API。它在音频和视频设备上提供了一个低延迟、基于图形的处理引擎，可以用来支持目前由pulseaudio和JACK处理的用例。PipeWire设计了一个强大的安全模型，使得从容器化应用程序与音频和视频设备的互动变得容易。图中的节点可以作为独立的进程来实现，与套接字进行通信，并使用fd传递来交换多媒体

[WirePlumber](https://pipewire.pages.freedesktop.org/wireplumber/) 是一个用于 [PipeWire](https://pipewire.org/) 的模块化会话/策略管理器和一个基于GObject的高级库，它封装了PipeWire的API，为编写守护进程的模块以及管理PipeWire的外部工具提供了便利。WirePlumber守护进程实现了会话和策略管理服务。它遵循模块化设计，拥有实现实际管理功能的插件。

[Core API](https://docs.pipewire.org/group__api__pw__core.html) 被所有需要与 [PipeWire Daemon](https://docs.pipewire.org/page_daemon.html) 通信的客户使用，并提供必要的结构来与守护程序进行接口。

[Implementation API](https://docs.pipewire.org/group__api__pw__impl.html) 主要由 [PipeWire Daemon](https://docs.pipewire.org/page_daemon.html) 本身使用，但也由 [PipeWire Session Manager](https://docs.pipewire.org/page_session_manager.html) 会话管理器和需要在图中构建对象的模块/扩展使用。

[SPA (Simple Plugin API)](https://docs.pipewire.org/group__api__spa.html) 是一个可扩展的API，可以实现所有类型的插件。

[GStreamer](https://gstreamer.freedesktop.org/) 是一个用于构建媒体处理组件图的库。它支持的应用范围从简单的Ogg/Vorbis播放、音频/视频流到复杂的音频（混合）和视频（非线性编辑）处理。应用程序可以透明地利用编解码器和过滤器技术的进步。

[Media Source Extensions (MSE)](https://www.w3.org/TR/media-source/) is a [W3C specification](https://github.com/w3c/media-source) 是一个W3C规范，允许JavaScript向支持HTML5视频和音频的网络浏览器内的媒体编解码器发送字节流。同时，这也允许完全用JavaScript实现客户端预取和缓冲流媒体的代码。

[WebRTC](https://webrtc.org/) 是一个开源项目，它为你的应用程序增加了实时通信能力，它工作在一个开放标准之上。它支持视频、语音和通用数据在对等体之间发送，使开发者能够建立强大的语音和视频通信解决方案。

## 贡献

- [x] 如果你想为本指南做出贡献，只需提交申请 [Pull Request](https://github.com/mikeroyal/Steam-Deck-Guide/pulls).

## 许可
[回到顶部](#目录)

根据 [知识共享署名4.0国际（CC BY 4.0）公共许可协议发布。](https://creativecommons.org/licenses/by/4.0/).

