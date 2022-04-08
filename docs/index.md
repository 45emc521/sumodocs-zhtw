<hTitles >SUMO 說明文件 (SUMO User Documentation)<hr style="border: 0.5px solid #338033;"></hTitles>

!!! note "請先看這裡！"
    本份文件是 SUMO Documentation 於 2022/04/01 版本的快取，旨在將 SUMO Documentation 翻譯成正體中文。如果需要最新的說明文件，歡迎造訪 [SUMO Documentation](https://sumo.dlr.de/docs/) 的官方網站。

"**S**imulation of **U**rban **MO**bility (SUMO)" 是一個開放原始碼、微觀車流與持續性的交通模擬套件，旨在支援大型的路網模擬。本軟體可對包括行人或多重情境下進行綜合模擬。

本軟體主要是由[德國航空太空中心 (**D**eutsches Zentrum für **L**uft- und **R**aumfahrt e.V.)](https://www.dlr.de) 內的[運輸系統研究所](https://www.dlr.de/ts)開發。SUMO 的授權條款為 [EPL 2.0](https://eclipse.org/legal/epl-v20.html)。The source code may also be made available under the following Secondary
Licenses when the conditions for such availability set forth in the EPL 2.0 are satisfied: [GPL2 or later](https://www.gnu.org/licenses/old-licenses/gpl-2.0-standalone.html).

歡迎使用[聯絡我們頁面](Contact.md)來分享你使用 SUMO 的結果及詢問問題；針對某些常見問題的答案，或許你可以在[常見問題頁面](FAQ.md)中得到一些幫助。

如果你使用 SUMO 進行車流模擬，你可以在[出版品](Publications.md)這一頁中和我們分享。

!!! note "關於引用"
    如果你需要引用 SUMO，請參考我們目前的出版格式：["Microscopic Traffic Simulation using SUMO"](https://elib.dlr.de/127994/); Pablo Alvarez Lopez, Michael Behrisch, Laura Bieker-Walz, Jakob Erdmann, Yun-Pang Flötteröd, Robert Hilbrich, Leonhard Lücken, Johannes Rummel, Peter Wagner, and Evamarie Wießner. IEEE Intelligent Transportation Systems Conference (ITSC), 2018.

你可以自由修改 SUMO 使用者文件；要修改特定頁面，請點選位在網頁右上角的「在 GitHub 上編輯中文版」按鈕，並在修改完後提出 pull 要求。這裡有份關於[編輯文章](Editing_Articles.md)的教學頁面。如有需要，你也可以在自己的電腦上[建置 (Build)](Developer/Documentation_Build.md) 這份文件，也可以[下載](https://sumo.dlr.de/sumo_documentation.zip)一份副本到你的電腦中。如果你要修改原文版本，請到 [SUMO Documentation](https://sumo.dlr.de/docs/) 了解更多資訊。

SUMO Documentation 會隨著 SUMO 的版本迭代而隨時更新。特定 SUMO 版本的說明文件會隨著你下載的 SUMO 版本一起提供。請到 {{SUMO}}/docs/userdoc/index.html 查看該對應該 SUMO 版本的說明文件。

# 簡介

- [SUMO 模擬軟體概觀](SUMO_at_a_Glance.md)

# 基本使用

- [這份文件的一些表示方式](Basics/Notation.md)
- [必須要會的基礎電腦技能](Basics/Basic_Computer_Skills.md)
- [安裝 SUMO](Installing/index.md)
- [使用 SUMO 命令列程式 (CLI)](Basics/Using_the_Command_Line_Applications.md)
- [教學](Tutorials/index.md)
- [驗證 XML 輸入](XMLValidation.md)

# 建立路網

- 關於 [SUMO 路網](Networks/SUMO_Road_Networks.md)的簡要介紹
- [抽象網路生成](Networks/Abstract_Network_Generation.md)
- 以 [netconvert](netconvert.md) 來匯入路網
  - [用 XML 自定義路網](Networks/PlainXML.md)
  - [匯入非 SUMO 的路網](Networks/Import.md)
    - [從 OpenStreetMap](Networks/Import/OpenStreetMap.md)
      - [三步驟路網生成器](Networks/Import/OpenStreetMap.md#3-click_scenario_generation)
    - [從 VISUM](Networks/Import/VISUM.md)
    - [從 Vissim](Networks/Import/Vissim.md)
    - [從 OpenDRIVE](Networks/Import/OpenDRIVE.md)
    - [從 MATsim](Networks/Import/MATsim.md)
    - [從 ArcView (shapefiles)](Networks/Import/ArcView.md)
    - [從 DlrNavTeq](Networks/Import/DlrNavteq.md)
    - [從 Robocup Simulation League](Networks/Import/RoboCup.md)
  - [匯入 SUMO 路網](Networks/Import/SUMO_Road_Networks.md)
  - [建立高速公路模擬路網](Simulation/Motorways.md#building_a_network_for_motorway_simulation)
  - [建立行人模擬路網](Simulation/Pedestrians.md#building_a_network_for_pedestrian_simulation)
  - [更多 netconvert 的設定](Networks/Further_Options.md)
  - [更多輸出選項](Networks/Further_Outputs.md)
- [以 netedit 建立與修改路網](Netedit/index.md)
- [納入高度資料](Networks/Elevation.md)
- [地理座標資料](Geo-Coordinates.md)

# 需求模型

- [SUMO 需求模型的介紹](Demand/Introduction_to_demand_modelling_in_SUMO.md)
- [車輛、車種及路徑 (routes) 的定義](Definition_of_Vehicles,_Vehicle_Types,_and_Routes.md)
- [以 netedit 定義需求](Netedit/elementsDemand.md)
- [公共運輸模擬](Simulation/Public_Transport.md)
- [個人與旅次鏈模擬](Specification/Persons.md)
- [物流 (Logistics) 模擬](Specification/Logistics.md)
- [最短或最佳化路徑](Demand/Shortest_or_Optimal_Path_Routing.md)
- [多運具聯運（複合運輸）路徑](IntermodalRouting.md)
- [模擬中的路徑](Demand/Automatic_Routing.md)
- [運算多使用者指派](Demand/Dynamic_User_Assignment.md)
- [建立行人交通需求](Simulation/Pedestrians.md#generating_pedestrian_demand)
- [建立車種分佈並對車隊建立模擬](Tools/Misc.md#createvehtypedistributionspy)

### 由資料產生需求

- [匯入 O/D 矩陣](Demand/Importing_O/D_Matrices.md)
  - [匯入 VISUM 需求的其他方式](Demand/Further_Ways_to_import_VISUM_Demand_Definitions.md)
  - [匯入 Vissim 需求的其他方式](Demand/Further_Ways_to_import_Vissim_Demand_Definitions.md)
- [Routes from Counting Data (road counts, turn counts)](Demand/Routes_from_Observation_Points.md)
- [由轉向比推算路徑](Demand/Routing_by_Turn_Probabilities.md)
- [以活動為基礎的需求產生](Demand/Activity-based_Demand_Generation.md)
- [隨機旅次](Tools/Trip.md#randomtripspy)
- [Open Street Map 工具](Tools/Import/OSM.md#osmwebwizardpy)
- [GTFS 資料](Tools/Import/GTFS.md)

# 模擬

- [基本定義](Simulation/Basic_Definition.md)
- [載入或儲存模擬狀態](Simulation/SaveAndLoad.md)

## 輸出

- [模擬輸出概觀](Simulation/Output/index.md)

## TraCI（即時模擬路網互動）

- [TraCI 概觀](TraCI.md) - The **Tra**ffic **C**ontrol **I**nterface
- [Libsumo](Libsumo.md) - 將 sumo 作為資源庫使用

## 交通控制設施

- [交通號誌](Simulation/Traffic_Lights.md)
- [公共運輸](Simulation/Public_Transport.md)
- [速限可變標誌](Simulation/Variable_Speed_Signs.md)
- [Rerouter／替代道路標誌](Simulation/Rerouter.md)
- [Vaporizer](Simulation/Vaporizer.md)（已被棄用，請改用 Calibrator）
- [車流、速度與車種的動態校準](Simulation/Calibrator.md)
- [停車區域](Simulation/ParkingArea.md)
- [迴轉](Simulation/Turnarounds.md)

## 交通模式

- [行人模擬](Simulation/Pedestrians.md)
- [自行車模擬](Simulation/Bicycles.md)
- [鐵道模擬](Simulation/Railways.md)
- [水路模擬](Simulation/Waterways.md)

## 其他功能

- [（污染物）排放](Models/Emissions.md)
- [電力車輛](Models/Electric.md)
- [混合動力車輛、高架橋及變電站](Models/ElectricHybrid.md)
- [物流](Specification/Logistics.md)
- [基礎參數](Simulation/GenericParameters.md)
- [型態視覺化](Simulation/Shapes.md)
- [無線設備偵測](Simulation/Bluetooth.md)
- [緊急車輛](Simulation/Emergency.md)
- [簡易自動駕駛車隊](Simpla.md)
- [需求反應式運輸 (DRT)／計程車](Simulation/Taxi.md)
- [綠燈最佳化速度顧問 (GLOSA)](Simulation/GLOSA.md)

## 模型細節

- [車輛速度](Simulation/VehicleSpeed.md)
- [車輛進入](Simulation/VehicleInsertion.md)
- [車輛權限（進入限制）](Simulation/VehiclePermissions.md)
- [道路容量](Simulation/RoadCapacity.md)
- [路口動態](Simulation/Intersections.md)
- [隨機](Simulation/Randomness.md)
- [路徑和重構路徑](Simulation/Routing.md)
- [子車道模型](Simulation/SublaneModel.md)
- [對向（逆向）行駛](Simulation/OppositeDirectionDriving.md)
- [安全](Simulation/Safety.md)
- [中觀模型](Simulation/Meso.md)
- [長度與距離](Simulation/Distances.md)

## 常見問題

- [為什麼車輛會瞬間消失或出現？](Simulation/Why_Vehicles_are_teleporting.md)
- [未預期的塞車](FAQ.md#the_simulation_has_lots_of_jamsdeadlocks_what_can_i_do)
- [迴轉太多次](Simulation/Turnarounds.md)
- [未預期的變換車道行為？](FAQ.md#why_do_the_vehicles_perform_unexpected_lane-changing_maneuvers)
- [如何提高車流量？](FAQ.md#how_do_i_get_high_flowsvehicle_densities)

# 其他工具

除了 SUMO 套件的[主要程式（包括 sumo, sumo-gui, netedit, netconvert 等）](SUMO_at_a_Glance.md#included_applications)外，SUMO 套件尚有 150 多個小應用程式。他們多半與交通路網分析、需求生成、修改需求以輸出分析有關，多數的小程式以 [python](https://www.python.org/) 撰寫而成。這些小程式都可以在 {{SUMO}}/tools 資料夾裡找到。

要查看這些小程式的清單，請參見：

- [工具索引](Tools/index.md)

以下的連結是一些好用（或重要）的小程式：

- [osmWebWizard](Tools/Import/OSM.md#osmwebwizardpy)：可以使用瀏覽器在極短的時間內，以真實世界的地圖生成路網配置。
- [Interfacing TraCI from Python](TraCI/Interfacing_TraCI_from_Python.md)：用 Python 存取正在進行的 SUMO 模擬。
- [sumolib](Tools/Sumolib.md)：用來與 SUMO 路網和 sumo XML 檔案一同運作的 Python 模組。
- [Xml Tools](Tools/Xml.md)：將 SUMO 模擬結果與 CSV／試算表相互交換的小工具。
- [traceExporter.py](Tools/TraceExporter.md)：輸出移動軌跡到不同的「軌跡檔案」格式。
- [netdiff.py](Tools/Net.md#netdiffpy)：比較兩個路網檔案的不同處。
- [Visualization Tools](Tools/Visualization.md)：將一部分的模擬輸出結果以圖形及友善的形式視覺化。

# 理論

- [常規的交通模擬](Theory/Traffic_Simulations.md)

# 程式操作手冊

- [sumo](sumo.md)
- [sumo-gui](sumo-gui.md)
- [netconvert](netconvert.md)
- [netedit](Netedit/index.md)
- [netgenerate](netgenerate.md)
- [od2trips](od2trips.md)
- [duarouter](duarouter.md)
- [jtrrouter](jtrrouter.md)
- [dfrouter](dfrouter.md)
- [marouter](marouter.md)
- [polyconvert](polyconvert.md)
- [activitygen](activitygen.md)
- [emissionsMap](Tools/Emissions.md#emissionsmap)
- [emissionsDrivingCycle](Tools/Emissions.md#emissionsdrivingcycle)

# 軟體散布

為了讓 SUMO 變得更好用，許多人延伸了 SUMO 的功能或為 SUMO 增加了許多小工具。儘管他們隨著 SUMO 的發行版本一同散布，但並非所有小工具都是 SUMO 核心的一部分。

- [發行版中的套件](Contributed/index.md#included_in_the_distribution)
- [外部套件](Contributed/index.md#external_extensions)

# 附錄

- [版本更新歷程](ChangeLog.md)
- [名詞解釋](Other/Glossary.md)
- [常見問題](FAQ.md)
- [已知檔案的副檔名](Other/File_Extensions.md)
