---
title: Tutorials
---

!!! note
    這些教學假設你已經有基礎的電腦技能。如果你有任何關於電腦操作上的疑問，你可以參閱[基礎／基礎電腦技能](../Basics/Basic_Computer_Skills.md)。

# 初心者教學
* [Hello World](Hello_World.md)－利用 netedit 建立路網及車流需求，並用 [sumo-gui](../sumo-gui.md) 進行模擬。
* [OSMWebWizard](OSMWebWizard.md)－使用 osmWebWizard.py 以便在短時間內建立一場景，從 OpenStreetMap 取得路網資料。
* [快速入門](quick_start.md)－更詳細的 [netedit](../Netedit/index.md) 教學；SUMO 套件的第一步。
* [在圓環駕駛](Driving_in_Circles.md)－使用 [netedit](../Netedit/index.md)；定義車流；利用 rerouters 讓車輛在圓環行駛。
* [SUMOlympics](SUMOlympics.md) - Create special lanes and simple traffic lights in netedit, more about flows and vehicle types, working with vehicle
* [Autobahn](Autobahn.md) - Build a highway, create a mixed highway flow, visualize vehicle speed, save view settings
* [Manhattan](Manhattan.md) - Build a [Manhattan mobility model](https://en.wikipedia.org/wiki/Manhattan_mobility_model)
* [Public Transport](PublicTransport.md) - Build a public transport scenario from scratch
* [TaxiService](TaxiService.md) - Build a taxi service from scratch

# SUMO User Conference 教學

**SUMO User Conference** 是由德國航空太空中心在柏林主辦的年會。

自 2015 年開始，每年大會都有 SUMO 的教學。以下你可以找到所有的教材（包含簡報檔案與輸入檔案）；自 2019 年開始，這些教學會錄影存放。

## 檔案

!!! note "注意"
    以下內容為原文。

* [SUMO 2015](http://sumo.dlr.de/daily/sumo2015_tutorial.zip): network editing with xml patch, persons, 
* [SUMO 2016](http://sumo.dlr.de/daily/sumo2016_tutorial.zip): network editing, meso, containers, [New Features 2016 (Slides)](http://sumo.dlr.de/daily/SUMO2016_new_features.pdf)
* [SUMO 2017](http://sumo.dlr.de/daily/sumo2017_tutorial.zip): network editing, randomTrips, calibrators (xml only), public transport (obsolete)
* [SUMO 2018](http://sumo.dlr.de/daily/sumo2018_tutorial.zip): fixing intermodal junctions, calibrators in netedit, junction model paramters, editing shapes
* [SUMO 2019](http://sumo.dlr.de/daily/sumo2019_tutorial.zip): network editing, visualizing traffic data, public transport from OSM, parking, netgenerate
* [SUMO 2020](http://sumo.dlr.de/daily/sumo2020_tutorial.zip): turn lanes, routeSampler.py, defining counting data in netedit, taxi/DRT
* [SUMO 2021](http://sumo.dlr.de/daily/sumo2021_tutorial.zip): traffic light layout, indirect left turn, TAZ, OD-traffic, GTFS

## Videos

<iframe width="560" height="315" src="https://www.youtube.com/embed/UeaeCdLt_1o" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/aiOQbaB-pWo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/tlshWdzFWpY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# 進階教學
* [Hello SUMO](Hello_SUMO.md) - The simplest net and a single car set up "by hand"
* [ScenarioGuide](ScenarioGuide.md) - High level outline of the steps needed to build a simulation scenario
* [HighwayDetector](HighwayDetector.md) - How to create a highway scenario based on induction loop data
* [FundamentalDiagram](FundamentalDiagram.md) - How to compute a fundamental diagram with SUMO
* [PT from OpenStreetMap](PT_from_OpenStreetMap.md) - Shows how to create a runnable public transit scenario entirely from [OpenStreetMap](https://www.openstreetmap.org/)
* [Importing GTFS](GTFS.md) - Importing public transport schedules from public sources using the General Transit Feed Specification
* [Port](port.md) - Creating a scenario that simulates the port logistics of an arbitrary port from [OpenStreetMap](https://www.openstreetmap.org/)

# TraCI 教學
These tutorials use the [Python-TraCI Library](../TraCI/Interfacing_TraCI_from_Python.md) for interfacing a python script with a running [sumo](../sumo.md) simulation.

* [TraCI4Traffic Lights](TraCI4Traffic_Lights.md) - An example for how to connect an external application to SUMO via TraCI for traffic lights control
* [TraCIPedCrossing](TraCIPedCrossing.md) - An example for building a pedestrian-actuated traffic light via TraCI

# 其他資源

## Curso de Simulação em Mobilidade
[Udemy tutorial](https://www.udemy.com/ferramenta-de-microssimulacao-de-trafego-sumo/learn/v4/overview) in Portuguese courtesy of Ednardo Ferreira.

## ITSC 2015

* Download the Tutorial Files at [http://sumo.dlr.de/daily/ITSC2015_tutorial.zip](http://sumo.dlr.de/daily/ITSC2015_tutorial.zip)

## Im- and Export
* [Trace File Generation](Trace_File_Generation.md) - Shows how to obtain vehicular trace files, usable for simulating vehicular communication

## Calibration/Validation
* [Calibration/San Pablo Dam](Calibration/San_Pablo_Dam.md) - Calibration of car-following parameter using vehicle passing times on observation points as used during the NEARCTIS summer school
<!--* [[Calibration/Berlin]] - Validation of a small inner-urban scenario of Berlin-->

<!-- ==Traffic Light Signal Control with MultiAgent Network== -->
<!--* [[MultiAgentControl]] - MultiAgent Control of Traffic Light Signals with Python -->

## Misc

- [Railway Tutorial](https://sumo.dlr.de/daily/workshop_rail_db2019.7z)

# Further Sources for Examples
## Using Examples from the Test Suite
SUMO comes with a large set of tests, just browse them at [{{SUMO}}/tests](https://github.com/eclipse/sumo/blob/main/tests). They are set up to be running by using a testing environment, but it is also possible to extract them and execute using [sumo](../sumo.md) and/or the other tools of the package. In order to do so you can either [download the complete sumo package](../Downloads.md#all-inclusive-tarball) or use the [online test extraction](https://sumo.dlr.de/extractTest.php). In the online tool you enter the path to the test you like (e.g. [{{SUMO}}/tests/sumo/extended/rerouter/use_routing_device](https://github.com/eclipse/sumo/blob/main/tests/sumo/extended/rerouter/use_routing_device) into the form and get a zip containing all the files.

If you have downloaded and unzipped the all inclusive package, you do not need the online form. Just go into the folder and execute the "extractTest.py" script. For example, you may get the same example of using rerouters as following:

```
cd <SUMO_HOME>/tests
../tools/extractTest.py -o /tmp/test sumo/extended/rerouter/use_routing_device
```

will extract you an example for [rerouting vehicles](../Simulation/Rerouter.md) into /tmp/test.

# Unfinished Tutorials
The following tutorials are not yet completed

* [Output Parsing](Output_Parsing.md) - A complex tutorial using rerouters to drive in circles and analyzing simulation output

# Outdated Tutorials
The following tutorials are kept for completeness but are superseded by other tutorials/documentation

* [Import from OpenStreetMap](Import_from_OpenStreetMap.md) - Shows how to prepare a map from [OpenStreetMap](https://www.openstreetmap.org/) for traffic simulation
* [Quick_Start_old_style](Quick_Start_old_style.md) - Build a scenario by editing the edge and node files in a text editor instead of [netedit](../Netedit/index.md)
* [CityMobil](CityMobil.md) - Simulation of a parking lot management using automated buses. This TraCI tutorial was written before the implementation of pedestrians and parkingAreas
