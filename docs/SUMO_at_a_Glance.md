---
title: SUMO 概觀
---

## 關於 SUMO

"**S**imulation of **U**rban **MO**bility"，或簡稱 SUMO，是一個開放原始碼、微觀、多種模式的車流模擬軟體。SUMO 可以在給定的路網及車流需求之下，進行車流模擬，並可將模擬應用在交通管理方面。

這是一個微觀 (microscopic) 模擬軟體——每部車都有詳細的參數、車流模型、屬於該車輛的路徑 (route)，且在路網中各自移動；模擬不完全是隨機的，如需更詳細的隨機資訊與設定，請到 SUMO 的[隨機性概觀文件](Simulation/Randomness.md)閱覽。

下載 SUMO 套件後，你會發現裡頭包含了很多小程式；這些小程式多半是為了提供既有路網的匯入和準備，你可以在 [SUMO 包含的程式](#included_applications)頁面中找到這些應用程式的列表與詳細資訊。

## 功能

- 包含所有用來準備和執行車流模擬的應用程式（路網和路徑匯入、DUA 以及模擬）。
- 模擬
  - 連續空間及離散時間的車流移動。
  - 不同車種模擬。
  - 多車道下，變換車道模擬。
  - 多種優先路權規則、建立交通號誌。
  - 易於使用且快速的 OpenGL 圖形化使用者介面。
  - 可管理內含諸多路段 (edge) 的巨大路網。
  - 極高的執行速度 （在 CPU 時脈為 1GHz 的電腦上，每秒可更新達 100.000 輛車）
  - 在 SUMO 執行時，讓 SUMO 與其他應用程式互動。
  - 以路網為基礎、路段為基礎、車輛為基礎，或以偵測器為基礎的模擬結果輸出。
  - 支援以個人為主體的複合運輸（多運具）旅次。
- 路網匯入
  - 匯入來自 VISUM, Vissim, Shapefiles, OSM, RoboCup, MATsim,
    OpenDRIVE 和 XML 格式的文件。
  - 遺失參數嗎？沒關係，系統將透過演算法嘗試補正。
- 路徑
  - 微觀路徑——每一輛車皆有獨一無二的路徑。
  - 不同的動態使用者指派演算法。
- 跨平台可執行
  - SUMO 使用標準 C++ 和跨平台的函式庫來開發。
  - 多數套件可在 Windows 和主要的 Linux 發行版執行。
- 只有 XML 資料的情況下仍有高度互操作性 (interoperability)。
- 開放原始碼 ([EPL 2.0](https://eclipse.org/legal/epl-v20.html))。

## 使用範例

自 2001 年以來，SUMO 套件已經被許多國內外的[研究計畫](Other/Projects.md)採用。這些應用包括：

- 交通號誌評估
- 路徑選擇與重新規劃路徑
- 交通監督方式評估
- [車輛通訊模擬](Topics/V2X.md)
- 交通預測

## 包含在 SUMO 中的應用程式

SUMO 套件包含了以下應用程式：

| 應用程式名稱                                                            | 簡要介紹                                                                                                                                                    |
| ----------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sumo](sumo.md)                                                   | The microscopic simulation with no visualization; command line application                                                                              |
| [sumo-gui](sumo-gui.md)                                           | The microscopic simulation with a graphical user interface                                                                                              |
| [netconvert](netconvert.md)                                       | Network importer and generator; reads road networks from different formats and converts them into the SUMO-format                                       |
| [netedit](Netedit/index.md)                                       | A graphical network editor.                                                                                                                             |
| [netgenerate](netgenerate.md)                                     | Generates abstract networks for the SUMO-simulation                                                                                                     |
| [duarouter](duarouter.md)                                         | Computes the fastest routes through the network, importing different types of demand description. Performs the DUA                                      |
| [jtrrouter](jtrrouter.md)                                         | Computes routes using junction turning percentages                                                                                                      |
| [dfrouter](dfrouter.md)                                           | Computes routes from induction loop measurements                                                                                                        |
| [marouter](marouter.md)                                           | Performs macroscopic assignment                                                                                                                         |
| [od2trips](od2trips.md)                                           | Decomposes O/D-matrices into single vehicle trips                                                                                                       |
| [polyconvert](polyconvert.md)                                     | Imports points of interest and polygons from different formats and translates them into a description that may be visualized by [sumo-gui](sumo-gui.md) |
| [activitygen](activitygen.md)                                     | Generates a demand based on mobility wishes of a modeled population                                                                                     |
| [emissionsMap](Tools/Emissions.md#emissionsmap)                   | Generates an emission map                                                                                                                               |
| [emissionsDrivingCycle](Tools/Emissions.md#emissionsdrivingcycle) | Calculates emission values based on a given driving cycle                                                                                               |
| [Additional Tools](Tools/index.md)                                | There are some tasks for which writing a large application is not necessary. Several solutions for different problems may be covered by these tools.    |

某些有志之士一同貢獻了他們的作品給 SUMO，並讓 SUMO 套件的功能更上層樓。這些由志願者延伸的功能也許未經測試、也有可能已經過時。如要參閱 SUMO 有哪些由志願者延伸的功能，請[按這裡](Contributed/index.md)了解詳細資訊。

## SUMO 的歷史

在公元 2000 年時，SUMO 誕生並開始發展。SUMO 的發展，主要是為了幫助交通研究社群評估他們自己設計的演算法，而製作一個開放原始碼的微觀車流模擬軟體。

SUMO 不需要取得所有需要用在交通模擬的資料，如引入或設定處理道路路網、車流需求及交通控制的方法。藉由 SUMO 這個工具，DLR（德國航空太空中心）想要達成以下目標：

1. 讓應用於 SUMO 的演算法，在使用共同架構與模型下更具可比較性。

2. 向來自世界各地的貢獻者中取得協助。

## Software design criteria

Two major design goals are approached: the software shall be fast and it
shall be portable. Due to this, the very first versions were developed
to be run from the command line only - no graphical interface was
supplied at first and all parameter had to be inserted by hand. This
should increase the execution speed by leaving off slow visualization.
Also, due to these goals, the software was split into several parts.
Each of them has a certain purpose and must be run individually. This is
something that makes SUMO different to other simulation packages where,
for instance, the dynamical user assignment is made within the
simulation itself, not via an external application like here. This split
allows an easier extension of each of the applications within the
package because each is smaller than a monolithic application that does
everything. Also, it allows the usage of faster data structures, each
adjusted to the current purpose, instead of using complicated and
ballast-loaded ones. Still, this makes the usage of SUMO a little bit
uncomfortable in comparison to other simulation packages. As there are
still other things to do, we are not thinking of a redesign towards an
integrated approach by now.

## Contributors and Participants

<table>
<thead>
<tr class="header">
<th><p>Org.</p></th>
<th><p>Name</p></th>
<th><p>Topics / Contribution</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><figure>
<img src="images/Zaik_small.gif" alt="Zaik_small.gif" />
</figure></td>
<td><p>Christian Rössel</p></td>
<td><p>Initial microsimulation core; initial detectors implementation</p></td>
</tr>
<tr class="even">
<td rowspan="11"><figure>
<img src="images/Dlr_small.gif" title="dlr_small.gif" alt="" />
</figure></td>
<td><p>Peter Wagner</p></td>
<td><p>Models, organization, spiritual lead</p></td>
</tr>
<tr class="odd">
<td><p>Daniel Krajzewicz</p></td>
<td><p>Everything</p></td>
</tr>
<tr class="even">
<td><p>Julia Ringel</p></td>
<td><p>Traffic Light & WAUT Algorithms</p></td>
</tr>
<tr class="odd">
<td><p>Eric Nicolay</p></td>
<td><p>Everything</p></td>
</tr>
<tr class="even">
<td><p>Michael Behrisch</p></td>
<td><p>Everything</p></td>
</tr>
<tr class="odd">
<td><p>Yun-Pang Wang</p></td>
<td><p>User Assignment</p></td>
</tr>
<tr class="even">
<td><p>Danilot Teta Boyom</p></td>
<td><p>Vehicular Communication Model (removed from the source)</p></td>
</tr>
<tr class="odd">
<td><p>Sascha Krieg</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Lena Kalleske</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Laura Bieker</p></td>
<td><p>Tests, Python scripts</p></td>
</tr>
<tr class="even">
<td><p>Jakob Erdmann</p></td>
<td><p>network import, <a href="netedit/index.html">netedit</a></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>Andreas Gaubatz</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>Maik Drozdzynski</p></td>
<td></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>Uni Lübeck</p></td>
<td><p>Axel Wegener</p></td>
<td><p>TraCI initiator</p></td>
</tr>
<tr class="even">
<td><p>Thimor Bohn</p></td>
<td><p>TraCI</p></td>
</tr>
<tr class="odd">
<td><p>Friedemann Wesner</p></td>
<td><p>TraCI</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>Felix Brack</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>Tino Morenz</p></td>
<td></td>
</tr>
<tr class="even">
<td rowspan="4"><p><img src="images/Uni_erlangen.png" title="fig:uni_erlangen.png" width="149" alt="uni_erlangen.png" /><br />
<br />
<img src="images/Uibk-small.png" title="fig:uibk-small.png" width="64" alt="uibk-small.png" /><br />
<br />
<img src="images/Logo_cmu.png" title="fig:logo_cmu.png" width="100" alt="logo_cmu.png" /><br />
<br />
<img src="images/Logo_ucla.png" title="fig:logo_ucla.png" width="100" alt="logo_ucla.png" /></p></td>
<td><p>Christoph Sommer</p></td>
<td><p>TraCI merge with <a href="http://veins.car2x.org/">Veins</a>, Subscription Interface, Misc.</p></td>
</tr>
<tr class="odd">
<td><p>David Eckhoff</p></td>
<td><p>TraCI, deterministic simulation behavior</p></td>
</tr>
<tr class="even">
<td><p>Falko Dressler</p></td>
<td><p>TraCI</p></td>
</tr>
<tr class="odd">
<td><p>Tobias Mayer</p></td>
<td><p>Traffic model abstraction, IDM model port</p></td>
</tr>
<tr class="even">
<td><p>HU Berlin</p></td>
<td><p>Matthias Heppner</p></td>
<td><p>Unittests</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><figure>
<img src="images/Tum-logo.png" title="tum-logo.png" alt="" />
</figure></td>
<td><p>Piotr Woznica</p></td>
<td><p><a href="activitygen.html">activitygen</a></p></td>
</tr>
<tr class="even">
<td><p>Walter Bamberger</p></td>
<td><p>Development of <a href="activitygen.html">activitygen</a> as a base for the evaluation of trust scenarios in VANETs. The work is part of the project <a href="http://www.ldv.ei.tum.de/fidens/">Fidens: Trust between Cooperative Systems</a> featuring trusted probabilistic knowledge processing in vehicular networks.</p></td>
</tr>
<tr class="odd">
<td><p>Matthew Fullerton</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>IIT Bombay, India</p></td>
<td><p>Ashutosh Bajpai</p></td>
<td><p>randomDepart.py, a python script to generate the real traffic pattern by exponential Distribution.</p></td>
</tr>
<tr class="odd">
<td><figure>
<img src="images/Torino_small.gif" title="torino_small.gif" alt="" />
</figure></td>
<td><p>Enrico Gueli</p></td>
<td><p><a href="http://sourceforge.net/projects/traci4j/">TraCI4J</a></p></td>
</tr>
<tr class="even">
<td></td>
<td><p>Leontios Papaleontiou</p></td>
<td><p><a href="Contributed/SUMO_Traffic_Modeler.html">Contributed/SUMO Traffic Modeler</a></p></td>
</tr>
<tr class="odd">
<td><figure>
<img src="images/Wroclaw_university_small.jpg" title="Wroclaw_university_small.jpg" alt="" />
</figure></td>
<td><p>Karol Stosiek</p></td>
<td><p>Documentation, network building</p></td>
</tr>
</tbody>
</table>

and many [other contributors]({{Source}}AUTHORS).