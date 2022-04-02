<hTitles >SUMO 使用者文件<hr style="border: 0.5px solid #338033;"></hTitles>

"**S**imulation of **U**rban **MO**bility" (SUMO) 是一個開放原始碼、微觀車流與持續性的交通模擬套件，旨在支援大型的路網模擬。本軟體可對包括行人與各種不同情境下構成的場景進行綜合模擬。本軟體主要是由[德國太空中心](https://www.dlr.de)內的[運輸系統研究所](https://www.dlr.de/ts)進行開發。SUMO 的授權條款為 [EPL 2.0](https://eclipse.org/legal/epl-v20.html)。The source code may also be made available under the following Secondary
Licenses when the conditions for such availability set forth in the EPL 2.0 are satisfied: [GPL2 or later](https://www.gnu.org/licenses/old-licenses/gpl-2.0-standalone.html).

敬請使用[聯絡我們頁面](Contact.md)來分享你使用 SUMO 的結果及詢問問題。針對某些常見問題的答案，或許你可以在[常見問題頁面](FAQ.md)中得到一些幫助。

如果你使用 SUMO，你可以在[出版品](Publications.md)這一頁中告訴我們。

!!! note
    如果你需要引用 SUMO，請參考我們目前的出版格式：["Microscopic Traffic Simulation using SUMO"](https://elib.dlr.de/127994/); Pablo Alvarez Lopez, Michael Behrisch, Laura Bieker-Walz, Jakob Erdmann, Yun-Pang Flötteröd, Robert Hilbrich, Leonhard Lücken, Johannes Rummel, Peter Wagner, and Evamarie Wießner. IEEE Intelligent Transportation Systems Conference (ITSC), 2018.

這份文件的內容可以自由修改。要修改特定頁面，請點選位在網頁右上角的 "Edit on GitHub" 按鈕，並在修改完後提出 pull 要求。這裡有份有關[編輯文章](Editing_Articles.md)的教學頁面。如有需要，你也可以在自己的電腦上[建置 (Build)](Developer/Documentation_Build.md) 這份文件，也可以[下載](https://sumo.dlr.de/sumo_documentation.zip)一份副本到你的電腦中。

這份文件會隨著 SUMO 的版本迭代而隨時更新。特定 SUMO 版本的說明文件會隨著你下載的 SUMO 版本一起提供。請到 {{SUMO}}/docs/userdoc/index.html 查看該 SUMO 版本的說明文件。

本份文件是 SUMO Documentation 於 2022/04/01 版本的快取，旨在將 SUMO Documentation 翻譯成正體中文。如果需要最新的說明文件，歡迎造訪 [SUMO Documentation](https://sumo.dlr.de/docs/) 的官方網站。本說明文件目前由 [Yu-Hsuan Liao](https://emc521.tw) 進行翻譯與維護。

# 簡介

- [SUMO 交通模擬](SUMO_at_a_Glance.md)

# 基本使用

- [這份文件的一些表示方式](Basics/Notation.md)
- [必須要會的基礎電腦技能](Basics/Basic_Computer_Skills.md)
- [安裝 SUMO](Installing/index.md)
- [使用 SUMO 命令列程式](Basics/Using_the_Command_Line_Applications.md)
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
  - [針對高速公路模擬建立路網](Simulation/Motorways.md#building_a_network_for_motorway_simulation)
  - [針對行人模擬建立路網](Simulation/Pedestrians.md#building_a_network_for_pedestrian_simulation)
  - [更多 netconvert 的選項](Networks/Further_Options.md)
  - [更多輸出選項](Networks/Further_Outputs.md)
- [以 netedit 建立與修改路網](Netedit/index.md)
- [納入高度資料](Networks/Elevation.md)
- [地理座標資料](Geo-Coordinates.md)

# 需求模型

- [SUMO 需求模型的介紹](Demand/Introduction_to_demand_modelling_in_SUMO.md)
- [車輛、車種及路徑 (routes) 的定義](Definition_of_Vehicles,_Vehicle_Types,_and_Routes.md)
- [以 netedit 定義需求](Netedit/elementsDemand.md)
- [公共運輸的模擬](Simulation/Public_Transport.md)
- [個人與旅次鏈的模擬](Specification/Persons.md)
- [物流的模擬](Specification/Logistics.md)
- [最短或最佳化路徑](Demand/Shortest_or_Optimal_Path_Routing.md)
- [多車種聯運路徑](IntermodalRouting.md)
- [模擬中的路徑](Demand/Automatic_Routing.md)
- [運算多使用者指派](Demand/Dynamic_User_Assignment.md)
- [建立行人交通需求](Simulation/Pedestrians.md#generating_pedestrian_demand)
- [建立車種分佈並對車隊進行建模](Tools/Misc.md#createvehtypedistributionspy)

### Data sources for demand generation

- [匯入 O/D 矩陣](Demand/Importing_O/D_Matrices.md)
  - [其他 VISUM 需求的匯入器](Demand/Further_Ways_to_import_VISUM_Demand_Definitions.md)
  - [Other Vissim Demand Importers](Demand/Further_Ways_to_import_Vissim_Demand_Definitions.md)
- [Routes from Counting Data (road counts, turn counts)](Demand/Routes_from_Observation_Points.md)
- [Routing by Turn Probabilities](Demand/Routing_by_Turn_Probabilities.md)
- [Activity-based Demand Generation](Demand/Activity-based_Demand_Generation.md)
- [Random Trips](Tools/Trip.md#randomtripspy)
- [Multi-modal random traffic](Tools/Import/OSM.md#osmwebwizardpy)
- [GTFS data](Tools/Import/GTFS.md)

# 模擬

- [Basic Definition](Simulation/Basic_Definition.md)
- [Saving and Loading Simulation State](Simulation/SaveAndLoad.md)

## 輸出
- [Simulation output overview](Simulation/Output/index.md)

## TraCI (On-line Interaction)
- [TraCI overview](TraCI.md) - The **Tra**ffic **C**ontrol **I**nterface
- [Libsumo](Libsumo.md) - Using sumo as a library

## 交通管理與設施

- [Traffic Lights](Simulation/Traffic_Lights.md)
- [Public Transport](Simulation/Public_Transport.md)
- [Variable Speed Signs](Simulation/Variable_Speed_Signs.md)
- [Rerouter / Alternative Route Signage](Simulation/Rerouter.md)
- [Vaporizer](Simulation/Vaporizer.md) (deprecated, use Calibrator instead)
- [Dynamic calibration of flow and speed and type](Simulation/Calibrator.md)
- [Parking areas](Simulation/ParkingArea.md)
- [Turnarounds](Simulation/Turnarounds.md)

## 交通模式

- [Pedestrian simulation](Simulation/Pedestrians.md)
- [Bicycle simulation](Simulation/Bicycles.md)
- [Railway simulation](Simulation/Railways.md)
- [Waterway simulation](Simulation/Waterways.md)

## 其他功能

- [Emissions](Models/Emissions.md)
- [Electric Vehicles](Models/Electric.md)
- [Electric Hybrid Vehicles, overhead lines, power substations](Models/ElectricHybrid.md)
- [Logistics](Specification/Logistics.md)
- [Generic Parameters](Simulation/GenericParameters.md)
- [Shape Visualization](Simulation/Shapes.md)
- [Wireless Device Detection](Simulation/Bluetooth.md)
- [Emergency Vehicles](Simulation/Emergency.md)
- [Simple Platooning (Simpla)](Simpla.md)
- [Demand Responsive Transport (DRT) / Taxis](Simulation/Taxi.md)
- [Green Light Optimal Speed Advisory (GLOSA)](Simulation/GLOSA.md)

## 模型細節

- [Vehicle speed](Simulation/VehicleSpeed.md)
- [Vehicle insertion](Simulation/VehicleInsertion.md)
- [Vehicle permissions (access restrictions)](Simulation/VehiclePermissions.md)
- [Road capacity](Simulation/RoadCapacity.md)
- [Intersection dynamics](Simulation/Intersections.md)
- [Randomness](Simulation/Randomness.md)
- [Routing and Re-routing](Simulation/Routing.md)
- [Sublane Model](Simulation/SublaneModel.md)
- [Opposite Direction Driving](Simulation/OppositeDirectionDriving.md)
- [Safety](Simulation/Safety.md)
- [Mesoscopic model](Simulation/Meso.md)
- [Lengths and Distances](Simulation/Distances.md)

## 常見問題

- [Why Vehicles are teleporting](Simulation/Why_Vehicles_are_teleporting.md)
- [Unexpected jamming](FAQ.md#the_simulation_has_lots_of_jamsdeadlocks_what_can_i_do)
- [Too many turn-arounds](Simulation/Turnarounds.md)
- [Unexpected lane-changing maneuvers?](FAQ.md#why_do_the_vehicles_perform_unexpected_lane-changing_maneuvers)
- [How to get high flows?](FAQ.md#how_do_i_get_high_flowsvehicle_densities)

# 其他工具

除了 SUMO 套件的[主要程式（包括 sumo, sumo-gui, netedit, netconvert 等）](SUMO_at_a_Glance.md#included_applications)外，SUMO 套件尚有 150 多個小應用程式。他們多半與交通路網分析、需求生成、修改需求以輸出分析有關。多數的小程式以 [python](https://www.python.org/) 撰寫而成。這些小程式都可以在 {{SUMO}}/tools 資料夾裡找到。

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
- [已知的檔案副檔名](Other/File_Extensions.md)

