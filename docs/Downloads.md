---
title: 下載 SUMO
---

!!! caution "注意"
    因網站限制，無法即時取得 SUMO 的最新版本資訊。如要下載最新版本的 SUMO，請至原文版的 [Downloads](https://sumo.dlr.de/docs/Downloads.php) 了解 SUMO 的最新版本，再依照本頁面進行安裝。安裝方式亦有可能隨著 SUMO 版本迭代而隨時變動。

# 最新的 SUMO 版本

**版本號碼**：{{Version}}。

**發行日期**：{{ReleaseDate}}。

## Windows

每份 SUMO 的發行版內都有執行檔（64 位元）、所有需要的 dll、範例檔案、工具以及 HTML 格式的說明文件。有關於這些內容的介紹與授權（尤其是那些具備 GPL 代碼以支援 GeoTIFFS、shapefile 和 3D 模型等額外的組建），請參閱 [the notes below](Downloads.md#note_on_licensing)。

<ul>
<li>下載 64 位元安裝檔：<a class="no-arrow-link" href="https://sumo.dlr.de/releases/{{Version}}/sumo-win64-{{Version}}.msi">sumo-win64-{{Version}}.msi </a><span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64-{{Version}}.msi","r");?></span></li>
<li>下載 64 位元 zip：<a class="no-arrow-link" href="https://sumo.dlr.de/releases/{{Version}}/sumo-win64-{{Version}}.zip">sumo-win64-{{Version}}.zip </a><span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64-{{Version}}.zip","r");?></span></li>
<li>下載 64 位元安裝檔（包含 GPL 代碼的擴充套件）：<a class="no-arrow-link" href="https://sumo.dlr.de/releases/{{Version}}/sumo-win64extra-{{Version}}.msi">sumo-win64extra-{{Version}}.msi </a><span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64extra-{{Version}}.msi","r");?></span></li>
<li>下載 64 位元 zip（包含 GPL 代碼的擴充套件）：<a class="no-arrow-link" href="https://sumo.dlr.de/releases/{{Version}}/sumo-win64extra-{{Version}}.zip">sumo-win64extra-{{Version}}.zip </a><span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64extra-{{Version}}.zip","r");?></span></li>
</ul>

### SUMO-Game

<ul><li>Windows 執行檔：<a class="no-arrow-link" href="https://sumo.dlr.de/releases/{{Version}}/sumo-game-{{Version}}.zip">sumo-game-{{Version}}.zip </a><span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-game-{{Version}}.zip","r");?></span></li></ul>

## Linux

在 [open build service](https://build.opensuse.org/project/show/science:dlr) 上，由社群維護了數個倉儲 (repository)，有關這些倉儲的列表，請見下方。

另外，也有提供給 Debian 和 Ubuntu 的 Launchpad 專案，以及適用於 Arch Linux 的套件。

- <https://salsa.debian.org/science-team/sumo.git>
- <https://launchpad.net/~sumo>
- <https://aur.archlinux.org/packages/sumo/>

這裡也有一個針對 SUMO 的 [flatpak](https://flathub.org/apps/details/org.eclipse.sumo)。

要把 SUMO 安裝進 Ubuntu，你需要打開終端機並輸入以下指令：

```
sudo add-apt-repository ppa:sumo/stable
sudo apt-get update
sudo apt-get install sumo sumo-tools sumo-doc
```

### 倉儲

如果該倉儲沒有包括某些資源庫（如 proj 和 gdal 等），他們有可能已成為散發套件的一部分；或者你會需要從其他倉儲內取得。你也許可以試試看其中一個建置的服務倉儲，例如 [Application:Geo](https://download.opensuse.org/repositories/Application:/Geo/)。目前這些套件內**沒有**包含說明文件。這些倉儲也包括 nightly 的版本分支（叫做 sumo-git）。

- [openSUSE Leap 42.3 repository](http://download.opensuse.org/repositories/science:/dlr/openSUSE_Leap_42.3/)
- [openSUSE Leap 15.0 repository](http://download.opensuse.org/repositories/science:/dlr/openSUSE_Leap_15.0/)
- [openSUSE Leap 15.1 repository](http://download.opensuse.org/repositories/science:/dlr/openSUSE_Leap_15.1/)
- [openSUSE Leap 15.2 repository](http://download.opensuse.org/repositories/science:/dlr/openSUSE_Leap_15.2/)
- [openSUSE Leap 15.3 repository](http://download.opensuse.org/repositories/science:/dlr/15.3/)
- [openSUSE Leap 15.4 repository](http://download.opensuse.org/repositories/science:/dlr/15.4/)
- [openSUSE Tumbleweed repository](http://download.opensuse.org/repositories/science:/dlr/openSUSE_Tumbleweed/)
- [Fedora 30 repository](http://download.opensuse.org/repositories/science:/dlr/Fedora_30/)
- [Fedora 31 repository](http://download.opensuse.org/repositories/science:/dlr/Fedora_31/)
- [Fedora 32 repository](http://download.opensuse.org/repositories/science:/dlr/Fedora_32/)
- [Fedora 33 repository](http://download.opensuse.org/repositories/science:/dlr/Fedora_33/)
- [Fedora 34 repository](http://download.opensuse.org/repositories/science:/dlr/Fedora_34/)
- [Fedora 35 repository](http://download.opensuse.org/repositories/science:/dlr/Fedora_35/)
- [Fedora Rawhide repository](http://download.opensuse.org/repositories/science:/dlr/Fedora_Rawhide/)
- [CentOS 7 repository](http://download.opensuse.org/repositories/science:/dlr/CentOS_7/)
- [CentOS 8 repository](http://download.opensuse.org/repositories/science:/dlr/CentOS_8/)

你可以加入這些倉儲並快速安裝他們（即不檢查 GPG 金鑰）。

例如，在 CentOS 7 上，使用 yum 來安裝 SUMO：

```
yum-config-manager --add-repo=https://download.opensuse.org/repositories/science:/dlr/CentOS_7/
yum install -y --nogpgcheck epel-release
yum install -y --nogpgcheck sumo-{{Version}}
```

如果在 openSUSE Leap 15.3 上，你可以使用 zypper 安裝：

```
zypper ar http://download.opensuse.org/repositories/science:/dlr/15.3/ science:dlr
zypper in sumo={{Version}}
```

如果你沒有輸入版本號碼，將會直接安裝最新的 nightly 版本分支。

Ubuntu、Debian 和 Arch 使用者請直接參閱上方的社群倉儲。

## macOS

在 macOS 上，你可以使用 Homebrew 來安裝 SUMO。請參閱[這裡](Installing/index.md#macos)來安裝或手動在電腦上編譯、建置。

"Bottles" 將可和 Homebrew 一起安裝，並且他們已經在最新的兩個 macOS 版本上建置。此外，SUMO 將直接在你的電腦上使用原始碼，在最小的系統需求上 (fox、proj、xerces-c) 建置並安裝。如果要使用其他的資源庫安裝 SUMO，你可以在輸入 brew 指令時指定使用這些資源庫，brew 會使用你指定的資源庫來編譯 SUMO。如要了解詳細資訊，請參閱 [Formula's
README](https://github.com/DLR-TS/homebrew-sumo/blob/main/README.md)。

### 應用程式啟動器

macOS 上的 SUMO 是以 X11 為基礎執行的，這導致你安裝好之後，無法在啟動台 (Launchpad.app) 上找到 SUMO 的套件，而必須先打 X11 才能執行。不過沒關係，我們打造了一個小程式，能讓你在 macOS 上以近乎原生（可以在啟動台啟動）的方式開啟 SUMO 套件內的應用程式，我們稱之為**應用程式啟動器**。這個應用程式啟動器和 SUMO 的各版本相同，且安裝好後，未來無需更新。

<ul>
<li><a class="no-arrow-link" href="https://sumo.dlr.de/daily/SUMO_launchers.dmg">下載 SUMO 應用程式啟動器</a><span class="badge badge-pill badge-secondary"><?php getFileSize("SUMO_launchers.dmg","d");?></span></li>
</ul>

這個啟動器可讓你在雙擊`.sumocfg`時，直接以 sumo-gui 啟動、並可將 sumo-gui 設為預設打開`.sumocfg`的應用程式。甚至，你可以把 **sumo-gui**、**netedit** 和 **OSM Web Wizard** 放在 Dock 上。

!!! caution "重要提醒"
    要正常使用啟動器，你必須在安裝啟動器前，先把 SUMO 安裝好；並確定你已經設定好 [SUMO_HOME](Basics/Basic_Computer_Skills.md#sumo_home) 環境變數。

## 原始碼

下載原始碼、範例檔案、給 Visual Studio 使用的 CMake 檔案及可在 Linux 上使用的 Makefile 檔案。這些下載項目不包含測試。

<ul>
<li><a class="no-arrow-link" href="https://sumo.dlr.de/releases/{{Version}}/sumo-src-{{Version}}.tar.gz">sumo-src-{{Version}}.tar.gz </a><span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-src-{{Version}}.tar.gz","r");?></span></li>
<li><a class="no-arrow-link" href="https://sumo.dlr.de/releases/{{Version}}/sumo-src-{{Version}}.zip">sumo-src-{{Version}}.zip </a><span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-src-{{Version}}.zip","r");?></span></li>
</ul>

## Python 套件／虛擬環境

自 SUMO 1.8.0（或在 macOS 上自 SUMO 1.12.0 開始），你也可以從 [Python packaging index](https://pypi.org/project/eclipse-sumo/) 安裝 SUMO。

你可以使用以下語法安裝：

- 安裝 SUMO 套件：`pip install eclipse-sumo` 
- 只安裝 TraCI：`pip install traci`
- 只安裝 lib sumo：`pip install libsumo`
- 只安裝 sumolib：`pip install sumolib`

這些指令可以在 Windows、macOS 和 2014 年之後的 Linux 版本使用，並適用這些作業系統上的 Python 2 和 3，惟 libsumo 需要 Python 3.6 以上版本。有了 pip，你可以很輕鬆地在電腦上建立[虛擬環境](https://docs.python.org/3/library/venv.html)以測試新的 SUMO 版本或最新的 nightly 組建。在 Linux 上輸入以下指令即可建立虛擬環境上的 SUMO：

```
python -m venv sumo_test
cd sumo_test
. bin/activate
pip install eclipse-sumo
```

!!! caution "macOS 依賴元件"
    為了能在 macOS 上使用 Python 元件，你需要利用 brew 安裝好所有依賴元件並更新至最新。請參閱[標準安裝](Installing/index.md#macos)頁面了解詳情。

# SUMO - 最新開發版本

SUMO 正持續活躍開發中。你可以在[版本紀錄](ChangeLog.md)內找到持續更新的 bug 修復及功能強化列表。歡迎你持續從我們的[倉儲](https://github.com/eclipse/sumo/)取得最新版本及[提供我們意見回饋](Contact.md)。

Every push to our main branch also triggers a build for Windows, Linux and macOS. The results can be found
by clicking on the [relevant commit here](https://github.com/eclipse/sumo/actions) and downloading the
appropriate file for your platform (you may need to sign in to GitHub).

## Nightly 快照

<div><span class="badge badge-pill badge-dark"><?php getNightlyFreshness("sumo-win64-git.zip");?></span></div>

在這個倉儲內的代碼為 [nightly 編譯版本](Developer/Nightly_Build.md)。所有 Windows 的組件都是 64 位元。有關於這些內容的介紹與授權（尤其是那些具備 GPL 代碼以支援 GeoTIFFS、shapefile 和 3D 模型等額外的組建），請參閱 [the notes below](Downloads.md#note_on_licensing)。

以下的套件可包含：

<ul>
<li>Sources: <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo-src-git.tar.gz">https://sumo.dlr.de/daily/sumo-src-git.tar.gz </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo-src-git.tar.gz","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-src-git.tar.gz","d");?></span></li>
<li>Sources: <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo-src-git.zip">https://sumo.dlr.de/daily/sumo-src-git.zip </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo-src-git.zip","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-src-git.zip","d");?></span></li>
<li>Sources and static HTML documentation: <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo_git.orig.tar.gz">https://sumo.dlr.de/daily/sumo_git.orig.tar.gz </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo_git.orig.tar.gz","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo_git.orig.tar.gz","d");?></span></li>
<li>Windows installer: <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo-win64-git.msi">https://sumo.dlr.de/daily/sumo-win64-git.msi </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo-win64-git.msi","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64-git.msi","d");?></span></li>
<li>Windows zip: <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo-win64-git.zip">https://sumo.dlr.de/daily/sumo-win64-git.zip </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo-win64-git.zip","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64-git.zip","d");?></span></li>
<li>Windows installer with all extras (contains GPL code): <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo-win64extra-git.msi">https://sumo.dlr.de/daily/sumo-win64extra-git.msi </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo-win64extra-git.msi","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64extra-git.msi","d");?></span></li>
<li>Windows zip with all extras (contains GPL code): <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo-win64extra-git.zip">https://sumo.dlr.de/daily/sumo-win64extra-git.zip </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo-win64extra-git.zip","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64extra-git.zip","d");?></span></li>
<li>Windows 64-bit binaries of the SUMO game: <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo-game-win64-git.zip">https://sumo.dlr.de/daily/sumo-game-win64-git.zip </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo-game-win64-git.zip","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-game-win64-git.zip","d");?></span></li>
<li>Windows 64-bit debug version: <a class="no-arrow-link" href="https://sumo.dlr.de/daily/sumo-win64Debug-git.zip">https://sumo.dlr.de/daily/sumo-win64Debug-git.zip </a><span class="badge badge-pill badge-light"><?php getFileDate("sumo-win64Debug-git.zip","d");?></span> <span class="badge badge-pill badge-secondary"><?php getFileSize("sumo-win64Debug-git.zip","d");?></span></li>
</ul>

你也可以在 [Python packaging indgit ex test instance](https://test.pypi.org/project/eclipse-sumo/) 裡面找到這些 Python 組建。
要安裝最新的 nightly 版本（強烈建議使用虛擬環境安裝）請使用[上方的教學](#python_packages_virtual_environments)，並以下方的安裝命令取代原本指令：

```
pip install -i https://test.pypi.org/simple/ eclipse-sumo
```

另外，儘管它是一個 Python 套件，但它包含所有 SUMO 的程式且確保完全可使用。你可以在[這裡](#python_packages_virtual_environments)找到使用 Python 套件的最低系統需求。

在 open build 上的 Linux [倉儲](#repositories)也有 nightly 組建。但是，這無法使用在 Debian、Ubuntu 和 Arch 版本的 Linux 上面。

[The corresponding documentation](https://sumo.dlr.de/daily/userdoc) is also visible live including [Doxygen docs](https://sumo.dlr.de/daily/doxygen). Additional artifacts such as [tests results](https://sumo.dlr.de/daily) and [code coverage analysis](https://sumo.dlr.de/daily/lcov/html/) are generated every night.

!!! caution "注意"
    因為 Windows 版本一天僅編譯一次（在柏林時間的午夜）的關係，適用於 Windows 的 SUMO 套件 nightly 組建可能無法跟隨[最新的 git 修正版本](https://github.com/eclipse/sumo/commits/main)。

# 較舊的版本及替代下載方式

[發行版資料夾](https://sumo.dlr.de/releases/)內有自 SUMO 1.2.0 及更新的版本。你也可以在 [sourceforge download portal](https://sourceforge.net/projects/sumo/files/sumo/) 內 SUMO 1.2.0 以後或更舊的版本。要在虛擬環境內測試這些舊版本，方式[如同上方所述](#python_packages_virtual_environments)，只要在使用 pip 安裝時指定要安裝的版本即可，如`pip install eclipse-sumo=1.9.0`（適用於 SUMO 1.8.0 以後版本）。

如果你需要壓縮後的較舊版本倉儲快照（包含測試版本），可以在 [GitHub tags](https://github.com/eclipse/sumo/tags) 或本機端倉儲內的 tag 了解。

# 其他

## 直接存取倉儲

你可以在 git 倉儲中直接取得最新的資源，請參閱[有關存取倉儲的常見問題](FAQ.md#how_do_i_access_the_code_repository)文章來了解詳情。正常情況下，它們應該都可以被編譯及成功完成我們一連串的測試。

要了解最新的編譯狀態，可以參閱 [nightly 測試版的數據](https://sumo.dlr.de/daily/)。

## 套件

SUMO 具備很多套件，這些套件的詳細資料陳列在下方。

|                                              | bin        | build    | src (source code) | user docs | developer docs (doxygen) | data     | examples | tutorials | tests | tools (except jars) | jars     |
| -------------------------------------------- | ---------- | -------- | ----------------- | --------- | ------------------------ | -------- | -------- | --------- | ----- | ------------------- | -------- |
| sumo-src-*XXX*.tar.gz<br>sumo-src-*XXX*.zip  |            | &#10004; | &#10004;          |           |                          | &#10004; | &#10004; | &#10004;  |       | &#10004;            |          |
| sumo-win??-*XXX*.zip<br>sumo-win??-*XXX*.msi | &#10004;   |          |                   | &#10004;  |                          | &#10004; | &#10004; | &#10004;  |       | &#10004;            | &#10004; |
| rpm                                          | (&#10004;) |          |                   | &#10004;  |                          | &#10004; | &#10004; | &#10004;  |       | &#10004;            |          |

## SUMO 的依存套件

在 Windows 平台上，如你想要在 Visual Studio 上編譯 SUMO，你可以藉由 clone [GitHub - DLR-TS/SUMOLibraries: A repository with current SUMO Libraries used in Windows compatible with Visual Studio 2019](https://github.com/DLR-TS/SUMOLibraries) 來得所有依存套件。

如果你只是要使用 SUMO 而不是要在電腦上編譯它，只要下載本頁最上方的可執行檔就好囉。

## 情境與其他資料

- [complete scenarios](Data/Scenarios.md)
- [networks](Data/Networks.md)
- [traffic data](Data/Traffic_Data.md)
- [Test cases](Tutorials/index.md#using_examples_from_the_test_suite)

# 授權

SUMO 以 [EPL-2.0](https://eclipse.org/legal/epl-v20.html) 授權釋出。在使用某些[開放原始碼資源庫](Libraries_Licenses.md)下，會使用 GPL 第 2 版或更新版釋出。

標準的 Windows 版本只會包含由 Eclipse 允許授權的原始碼和可執行檔，意思就是不包含 GPL 和 LGPL 授權。如果要使用一些特殊功能（包含 shapefile 匯入、GeoTIFF 處理、OpenSceneGraph 3D 使用者介面或影片生成等等），請下載 extra 版本。

Linux 版本則不包含任何外部資源庫。



<?php
function getFileDate($fname, $type){
    switch($type){
    case "r":
    $file = "/releases/{{Version}}/" . $fname;
    break;
    case "d":
    $file = "/daily/" . $fname;
    break;
}
$file = $_SERVER['DOCUMENT_ROOT']. $file;
if(file_exists($file)){
    echo date ("F d Y H:i:s", filemtime($file)) . " UTC";
}}
function getFileSize($fname, $type){
switch($type){
    case "r":
    $file = "/releases/{{Version}}/" . $fname;
    break;
    case "d":
    $file = "/daily/" . $fname;
    break;
}
$file = $_SERVER['DOCUMENT_ROOT']. $file;
if(file_exists($file)){
echo round(((filesize($file))/1048576),1) . " MB";
}}
function getNightlyFreshness($fname){
$zip = new ZipArchive;
$zip->open($_SERVER['DOCUMENT_ROOT']. "/daily/" . $fname);
$freshnessIs = str_replace("\"","",str_replace("#define VERSION_STRING ","",$zip->getFromName('sumo-git/include/version.h')));
echo $freshnessIs;
$zip->close();
}
?>
