# [Bienvenido](#inicio)

En esta página, usted encontrara información relevante asociada al artículo Modelos LSTM para la predicción de calidad de servicios cloud.

## Indice

1. [Datos](#datos)
2. [Modelos LSTM Univariado](#LSTMU)
3. [Modelos LSTM Multivariado](#LSTMM)


# 1. Datos {#Datos}
El conjunto de datos corresponde a la información obtenida de la monitorización del servicio SAlert, el cual esta  compuesto por 16 métricas de calidad como variables de entrada y sus mediciones corresponden en una serie temporal.

- <a href ="./files/datos.csv">  Fuente de datos </a>

## 1.1. Datasets

| Variable            | Dataset                                                                  |
|---------------------|----------------------------------------------------------------------------|
| Free Memory         | ![Free Memory_dataset.png](imgs%2Flstmu%2FFree%20Memory_dataset.png)               |
| Used Memory         | ![Used Memory_dataset.png](imgs%2Flstmu%2FUsed%20Memory_dataset.png)               |
| Free Disk           | ![Free Disk_dataset.png](imgs%2Flstmu%2FFree%20Disk_dataset.png)                   |
| Used Disk           | ![Used Disk_dataset.png](imgs%2Flstmu%2FUsed%20Disk_dataset.png)                   |
| Disk read/s         | ![Disk read_s_dataset.png](imgs%2Flstmu%2FDisk%20read_s_dataset.png)               |
| Disk write/s        | ![Disk write_s_dataset.png](imgs%2Flstmu%2FDisk%20write_s_dataset.png)             |
| NetBytes In         | ![NetBytes In_dataset.png](imgs%2Flstmu%2FNetBytes%20In_dataset.png)               |
| NetBytes Out        | ![NetBytes Out_dataset.png](imgs%2Flstmu%2FNetBytes%20Out_dataset.png)             |
| NetPackets In       | ![NetPackets In_dataset.png](imgs%2Flstmu%2FNetPackets%20In_dataset.png)           |
| NetPackets Out      | ![NetPackets In_dataset.png](imgs%2Flstmu%2FNetPackets%20Out_dataset.png)                                                                             |
| Rx packets          | ![Rx packets_dataset.png](imgs%2Flstmu%2FRx%20packets_dataset.png)                 |
| Tx packets          | ![Tx packets_dataset.png](imgs%2Flstmu%2FTx%20packets_dataset.png)                 |
| CPU percent         | ![CPU percent_dataset.png](imgs%2Flstmu%2FCPU%20percent_dataset.png)                           |
| Memory Used percent | ![Used Memory_dataset.png](imgs%2Flstmu%2FUsed%20Memory_dataset.png)               |
| Disk Used percent   | ![Disk Used percent_dataset.png](imgs%2Flstmu%2FDisk%20Used%20percent_dataset.png) |
| Uptime              | ![Uptime_dataset.png](imgs%2Flstmu%2FUptime_dataset.png)                           |

# 2. Modelos LSTM Univariados {#LSTMU}
En esta sección ubicamos el código fuente del modelo LSTM Univariado y el resultado de las cinco ejecuciones

<p align="center">
    <a href="https://colab.research.google.com/drive/1rfBBedaReGYBUKgm2sCVJtxRKFFSPCjE">
        <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
    </a>

</p>

## 2.1. Iteración 1

| Variable            | Entrenamiento                                                                           | Pruebas                                                                                |
|---------------------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Free Memory         | ![Free Memory_train_result.png](imgs%2Flstmu%2FFree%20Memory_train_result-1.png)                   | ![Free Memory_test_result.png](imgs%2Flstmu%2FFree%20Memory_test_result-result-1.png)                   |
| Used Memory         | ![Used Memory_train_result.png](imgs%2Flstmu%2FUsed%20Memory_train_result-1.png)                   | ![Used Memory_test_result.png](imgs%2Flstmu%2FUsed%20Memory_test_result-result-1.png)                   |
| Free Disk           | ![Free Disk_train_result.png](imgs%2Flstmu%2FFree%20Disk_train_result-1.png)                       | ![Free Disk_test_result.png](imgs%2Flstmu%2FFree%20Disk_test_result-result-1.png)                       |
| Used Disk           | ![Used Disk_train_result.png](imgs%2Flstmu%2FUsed%20Disk_train_result-1.png)                       | ![Used Disk_test_result.png](imgs%2Flstmu%2FUsed%20Disk_test_result-result-1.png)                       |
| Disk read/s         | ![Disk read_s_train_result.png](imgs%2Flstmu%2FDisk%20read_s_train_result-1.png)                   | ![Disk read_s_test_result.png](imgs%2Flstmu%2FDisk%20read_s_test_result-result-1.png)                   |
| Disk write/s        | ![Disk write_s_train_result.png](imgs%2Flstmu%2FDisk%20write_s_train_result-1.png)                 | ![Disk write_s_test_result.png](imgs%2Flstmu%2FDisk%20write_s_test_result-result-1.png)                 |
| NetBytes In         | ![NetBytes In_train_result.png](imgs%2Flstmu%2FNetBytes%20In_train_result-1.png)                   | ![NetBytes In_test_result.png](imgs%2Flstmu%2FNetBytes%20In_test_result-result-1.png)                   |
| NetBytes Out        | ![NetBytes Out_train_result.png](imgs%2Flstmu%2FNetBytes%20Out_train_result-1.png)                 | ![NetBytes Out_test_result.png](imgs%2Flstmu%2FNetBytes%20Out_test_result-result-1.png)                 |
| NetPackets In       | ![NetPackets In_train_result.png](imgs%2Flstmu%2FNetPackets%20In_train_result-1.png)               | ![NetPackets In_test_result.png](imgs%2Flstmu%2FNetPackets%20In_test_result-result-1.png)               |
| NetPackets Out      |                                                                                          |                                                                                        |
| Rx packets          | ![Rx packets_train_result.png](imgs%2Flstmu%2FRx%20packets_train_result-1.png)                     | ![Rx packets_test_result.png](imgs%2Flstmu%2FRx%20packets_test_result-result-1.png)                     |
| Tx packets          | ![Tx packets_train_result.png](imgs%2Flstmu%2FTx%20packets_train_result-1.png)                     | ![Tx packets_test_result.png](imgs%2Flstmu%2FTx%20packets_test_result-result-1.png)                     |
| CPU percent         | ![CPU percent_train_result.png](imgs%2Flstmu%2FCPU%20percent_train_result-1.png)                   | ![CPU percent_test_result.png](imgs%2Flstmu%2FCPU%20percent_test_result-result-1.png)                   |
| Memory Used percent | ![Memory Used percent_train_result.png](imgs%2Flstmu%2FMemory%20Used%20percent_train_result-1.png) | ![Memory Used percent_test_result.png](imgs%2Flstmu%2FMemory%20Used%20percent_test_result-result-1.png) |
| Disk Used percent   | ![Disk Used percent_train_result.png](imgs%2Flstmu%2FDisk%20Used%20percent_train_result-1.png)     | ![Disk Used percent_test_result.png](imgs%2Flstmu%2FDisk%20Used%20percent_test_result-result-1.png)     |
| Uptime              | ![Uptime_train_result.png](imgs%2Flstmu%2FUptime_train_result-1.png)                               | ![Uptime_test_result.png](imgs%2Flstmu%2FUptime_test_result-result-1.png)                               |

[Inicio](#inicio)

## 2.2. Métricas de Precisión

| Variable            | RMSE                                                                     | MAE                                                                     | MAPE                                                                     | 
|---------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Free Memory         | ![Free Memory_mrse.png](imgs%2Flstmu%2FFree%20Memory_mrse-result-1.png)                   | ![Free Memory_mae.png](imgs%2Flstmu%2FFree%20Memory_mae-result-1.png)                    | ![Free Memory_mape.png](imgs%2Flstmu%2FFree%20Memory_mape-result-1.png)                   | 
| Used Memory         | ![Used Memory_rsme.png](imgs%2Flstmu%2FUsed%20Memory_mrse-result-1.png)                   | ![Used Memory_mae.png](imgs%2Flstmu%2FUsed%20Memory_mae-result-1.png)                    | ![Used Memory_mape.png](imgs%2Flstmu%2FUsed%20Memory_mape-result-1.png)                   |
| Free Disk           | ![Free Disk_mrse.png](imgs%2Flstmu%2FFree%20Disk_mrse-result-1.png)                       | ![Free Disk_mae.png](imgs%2Flstmu%2FFree%20Disk_mae-result-1.png)                        | ![Free Disk_mase.png](imgs%2Flstmu%2FFree%20Disk_mape-result-1.png)                       |                       |
| Used Disk           | ![Used Disk_mrse.png](imgs%2Flstmu%2FUsed%20Disk_mrse-result-1.png)                       | ![Used Disk_mae.png](imgs%2Flstmu%2FUsed%20Disk_mae-result-1.png)                        | ![Used Disk_mape.png](imgs%2Flstmu%2FUsed%20Disk_mape-result-1.png)                       |                       |
| Disk read/s         | ![Disk read_s_mrse.png](imgs%2Flstmu%2FDisk%20read_s_mrse-result-1.png)                   | ![Disk read_s_mae.png](imgs%2Flstmu%2FDisk%20read_s_mae-result-1.png)                    | ![Disk read_s_mape.png](imgs%2Flstmu%2FDisk%20read_s_mape-result-1.png)                   |                   |
| Disk write/s        | ![Disk write_s_rmse.png](imgs%2Flstmu%2FDisk%20write_s_mrse-result-1.png)                 | ![Disk write_s_mae.png](imgs%2Flstmu%2FDisk%20write_s_mae-result-1.png)                 | ![Disk write_s_mape.png](imgs%2Flstmu%2FDisk%20write_s_mape-result-1.png)                 |                 |
| NetBytes In         | ![NetBytes In_mrse.png](imgs%2Flstmu%2FNetBytes%20In_mrse-result-1.png)                   | ![NetBytes In_mrse.png](imgs%2Flstmu%2FNetBytes%20In_mae-result-1.png)                   | ![NetBytes In_mrse.png](imgs%2Flstmu%2FNetBytes%20In_mape-result-1.png)                   |                  |
| NetBytes Out        | ![NetBytes Out_mrse.png](imgs%2Flstmu%2FNetBytes%20Out_mrse-result-1.png)                 | ![NetBytes Out_mrse.png](imgs%2Flstmu%2FNetBytes%20Out_mae-result-1.png)                 | ![NetBytes Out_mrse.png](imgs%2Flstmu%2FNetBytes%20Out_mape-result-1.png)                 |                 |
| NetPackets In       | ![NetPackets In_mrse.png](imgs%2Flstmu%2FNetPackets%20In_mrse-result-1.png)               | ![NetPackets In_mrse.png](imgs%2Flstmu%2FNetPackets%20In_mae-result-1.png)               | ![NetPackets In_mape.png](imgs%2Flstmu%2FNetPackets%20In_mape-result-1.png)               |               |
| NetPackets Out      |   ![NetPackets Out_rmse.png](imgs%2Flstmu%2FNetPackets%20Out_mrse-result-1.png)               | ![NetPackets Out_mae.png](imgs%2Flstmu%2FNetPackets%20Out_mae-result-1.png)               | ![NetPackets Out_mape.png](imgs%2Flstmu%2FNetPackets%20Out_mape-result-1.png)               |               |
| Rx packets          | ![Rx packets_mrse.png](imgs%2Flstmu%2FRx%20packets_mrse-result-1.png)                     | ![Rx packets_mrse.png](imgs%2Flstmu%2FRx%20packets_mae-result-1.png)                     | ![Rx packets_mrse.png](imgs%2Flstmu%2FRx%20packets_mape-result-1.png)                     |                    |
| Tx packets          | ![Tx packets_mrse.png](imgs%2Flstmu%2FTx%20packets_mrse-result-1.png)                     | ![Tx packets_mrse.png](imgs%2Flstmu%2FTx%20packets_mae-result-1.png)                     | ![Tx packets_mrse.png](imgs%2Flstmu%2FTx%20packets_mape-result-1.png)                     |                   |
| CPU percent         | ![CPU percent_mrse.png](imgs%2Flstmu%2FCPU%20percent_mrse-result-1.png)                   | ![CPU percent_mrse.png](imgs%2Flstmu%2FCPU%20percent_mae-result-1.png)                   | ![CPU percent_mrse.png](imgs%2Flstmu%2FCPU%20percent_mape-result-1.png)                   |                 |
| Memory Used percent | ![Memory Used percent_mrse.png](imgs%2Flstmu%2FMemory%20Used%20percent_mrse-result-1.png) | ![Memory Used percent_mrse.png](imgs%2Flstmu%2FMemory%20Used%20percent_mae-result-1.png) | ![Memory Used percent_mrse.png](imgs%2Flstmu%2FMemory%20Used%20percent_mape-result-1.png) | 
| Disk Used percent   | ![Disk Used percent_mrse.png](imgs%2Flstmu%2FDisk%20Used%20percent_mrse-result-1.png)     | ![Disk Used percent_mrse.png](imgs%2Flstmu%2FDisk%20Used%20percent_mae-result-1.png)     | ![Disk Used percent_mrse.png](imgs%2Flstmu%2FDisk%20Used%20percent_mape-result-1.png)     | 
| Uptime              | ![Uptime_mrse.png](imgs%2Flstmu%2FUptime_mrse-result-1.png)                               | ![Uptime_mrse.png](imgs%2Flstmu%2FUptime_mae-result-1.png)                               | ![Uptime_mrse.png](imgs%2Flstmu%2FUptime_mape-result-1.png)                               | 



[Inicio](#inicio)

## 2.3. Cálculo MRA

| Free   Memory | 1          | 2          | 3          | 4          | 5          |
|---------------|------------|------------|------------|------------|------------|
| count         | 5124 | 5124 | 5124 | 5124 | 5124 |
| mean          | 0,15934    | 0,14065    | 0,12946    | 0,10459    | 0,11971    |
| std           | 0,11323    | 0,11829    | 0,11392    | 0,10321    | 0,11815    |
| min           | 0,00012    | 0,00023    | 0,00016    | 0,00002    | 0,00003    |
| 25%           | 0,11003    | 0,08072    | 0,06782    | 0,04869    | 0,06237    |
| 50%           | 0,14799    | 0,12374    | 0,11651    | 0,07951    | 0,10182    |
| 75%           | 0,18923    | 0,17579    | 0,15841    | 0,12726    | 0,14624    |
| max           | 1,52110    | 1,49402    | 1,53980    | 1,38043    | 1,57954    |


| Used   Memory | 1       | 2       | 3       | 4       | 5       |
|---------------|---------|---------|---------|---------|---------|
| count         | 5124    | 5124    | 5124    | 5124    | 5124    |
| mean          | 0,13165 | 0,11855 | 0,12388 | 0,11475 | 0,09401 |
| std           | 0,11769 | 0,09469 | 0,11848 | 0,12294 | 0,12014 |
| min           | 0,00007 | 0,00004 | 0,00007 | 0,00018 | 0,00002 |
| 25%           | 0,07807 | 0,07383 | 0,06620 | 0,04293 | 0,02958 |
| 50%           | 0,11426 | 0,10426 | 0,10700 | 0,08880 | 0,06583 |
| 75%           | 0,15894 | 0,14276 | 0,15400 | 0,15408 | 0,11689 |
| max           | 1,55377 | 1,41339 | 1,54666 | 1,57722 | 1,60782 |

| Free Disk | 1       | 2       | 3       | 4       | 5       |
|-----------|---------|---------|---------|---------|---------|
| count     | 5124,00 | 5124,00 | 5124,00 | 5124,00 | 5124,00 |
| mean      | 0,39327 | 0,26218 | 0,30336 | 0,40992 | 0,33795 |
| std       | 0,17899 | 0,06748 | 0,08697 | 0,12887 | 0,08782 |
| min       | 0,08927 | 0,11833 | 0,07839 | 0,12674 | 0,13629 |
| 25%       | 0,22936 | 0,21448 | 0,23766 | 0,30943 | 0,25806 |
| 50%       | 0,38243 | 0,26330 | 0,31212 | 0,40692 | 0,34819 |
| 75%       | 0,53830 | 0,30125 | 0,35737 | 0,52198 | 0,39428 |
| max       | 0,91217 | 0,57225 | 0,65038 | 0,77156 | 0,65927 |


| Used   Disk         | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,37287     | 0,28410     | 0,29853     | 0,30329           | 0,37557     |
| std                 | 0,10981     | 0,07639     | 0,17230     | 0,11061           | 0,10008     |
| min                 | 0,11532     | 0,13148     | 0,00037     | 0,11261           | 0,16461     |
| 25%                 | 0,28941     | 0,23126     | 0,18381     | 0,22036           | 0,30348     |
| 50%                 | 0,37511     | 0,28892     | 0,27027     | 0,28606           | 0,37373     |
| 75%                 | 0,45005     | 0,33608     | 0,41753     | 0,38510           | 0,44398     |
| max                 | 0,69442     | 0,57277     | 0,76552     | 0,67038           | 0,66889     |


| Disk read/s         | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 376,5227951 | 250,1647866 | 323,4274358 | 298,7796718       | 429,9993135 |
| std                 | 1770,976397 | 1772,822727 | 1763,92616  | 1765,298796       | 1796,119245 |
| min                 | 0,898586121 | 1,749480667 | 0,090709546 | 1,745024414       | 0,019746933 |
| 25%                 | 167,2494366 | 68,4636557  | 78,56801056 | 125,0240063       | 145,2034747 |
| 50%                 | 247,7970056 | 106,0041418 | 226,74315   | 142,0440118       | 225,695618  |
| 75%                 | 350,2385461 | 109,2530737 | 249,1233466 | 168,3855591       | 454,1207068 |
| max                 | 23972,14668 | 23594,87092 | 23616,72048 | 23514,564         | 24168,01485 |

| Disk write/s        | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 18,37193398 | 18,72588396 | 16,09431174 | 20,33329436       | 12,84665948 |
| std                 | 10,23192268 | 10,32020347 | 9,624030082 | 12,15374468       | 8,513752716 |
| min                 | 0,001849823 | 0,013256989 | 0,000231018 | 0,00061264        | 0,008995514 |
| 25%                 | 7,263417473 | 8,111938057 | 6,230493507 | 6,985214424       | 6,172863884 |
| 50%                 | 23,85156521 | 23,44280025 | 20,05036091 | 24,62560371       | 11,8195546  |
| 75%                 | 27,69763229 | 27,38998165 | 24,01921421 | 31,48180801       | 17,47081766 |
| max                 | 30,42824249 | 34,47645645 | 33,82572006 | 37,81199097       | 43,39380402 |

| NetBytes In         | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,076871765 | 0,0770763   | 0,100335811 | 0,077765218       | 0,075085877 |
| std                 | 0,289848036 | 0,291067105 | 0,287511685 | 0,295724701       | 0,294184111 |
| min                 | 0,024864197 | 0,00922966  | 0,024775505 | 2,09808E-05       | 0,000118256 |
| 25%                 | 0,034086227 | 0,027038574 | 0,067594528 | 0,034444809       | 0,029230118 |
| 50%                 | 0,062921524 | 0,068569183 | 0,085813522 | 0,053415298       | 0,055107117 |
| 75%                 | 0,08718586  | 0,087132454 | 0,112161636 | 0,097557068       | 0,099147797 |
| max                 | 4,975135803 | 5,010707855 | 4,974185944 | 5,121547699       | 5,099147797 |

| NetBytes Out        | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,102843798 | 0,092878961 | 0,856169632 | 0,09631041        | 0,080190329 |
| std                 | 0,295724167 | 0,289132343 | 1,591303623 | 0,289328426       | 0,295870189 |
| min                 | 0,000202179 | 0,034685135 | 0,000552177 | 0,030207634       | 0,000294685 |
| 25%                 | 0,030506134 | 0,042303085 | 0,027551651 | 0,038517952       | 0,036644936 |
| 50%                 | 0,045294762 | 0,077943802 | 0,035467148 | 0,097103119       | 0,067769527 |
| 75%                 | 0,186486244 | 0,118654251 | 0,602146149 | 0,121712685       | 0,077587128 |
| max                 | 5,013263702 | 4,964280128 | 5,035467148 | 4,969792366       | 5,128442764 |

| NetPackets In       | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,116708315 | 0,107875747 | 0,099208437 | 0,115788467       | 0,080249534 |
| std                 | 0,290978992 | 0,290000832 | 0,292131085 | 0,294762705       | 0,291096481 |
| min                 | 0,005456924 | 0,001834869 | 0,021760941 | 0,000200272       | 0,001302719 |
| 25%                 | 0,053893089 | 0,039772034 | 0,037021637 | 0,057364464       | 0,03506279  |
| 50%                 | 0,123180389 | 0,128626823 | 0,097903252 | 0,111009598       | 0,082990646 |
| 75%                 | 0,149150848 | 0,13503933  | 0,11797142  | 0,129301071       | 0,084810257 |
| max                 | 5,053956985 | 4,998121262 | 5,037021637 | 5,129301071       | 4,998695374 |

| NetPackets Out      | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,079239501 | 0,272054016 | 0,079978019 | 0,076098203       | 0,103054837 |
| std                 | 0,292108569 | 0,321154727 | 0,29142228  | 0,292241877       | 0,290108354 |
| min                 | 1,90735E-05 | 8,2016E-05  | 0,023516655 | 0,00094986        | 0,012336731 |
| 25%                 | 0,011585236 | 0,137292862 | 0,034286499 | 0,027181625       | 0,051388741 |
| 50%                 | 0,085716248 | 0,192358017 | 0,052677155 | 0,039881706       | 0,0747509   |
| 75%                 | 0,111870766 | 0,416976929 | 0,078636169 | 0,107582092       | 0,135994911 |
| max                 | 5,005693436 | 5,452227592 | 4,976483345 | 5,000951767       | 5,051388741 |

| Rx packets          | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,206599573 | 0,19582601  | 0,201564006 | 0,260653517       | 0,301503261 |
| std                 | 1,06144246  | 1,062903696 | 1,061495036 | 1,053600541       | 1,050775946 |
| min                 | 0,00793457  | 0,001220703 | 0,032348633 | 0                 | 0           |
| 25%                 | 0,020751953 | 0,023803711 | 0,040161133 | 0,092529297       | 0,053222656 |
| 50%                 | 0,104553223 | 0,078674316 | 0,052612305 | 0,129760742       | 0,195068359 |
| 75%                 | 0,11340332  | 0,09362793  | 0,060546875 | 0,151245117       | 0,236816406 |
| max                 | 20,13793945 | 20,11181641 | 20,13525391 | 20,23217773       | 20,32995605 |

| Tx packets          | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,185475643 | 0,252212822 | 0,20454527  | 0,174536104       | 1,542102394 |
| std                 | 1,064821404 | 1,055151742 | 1,061311254 | 1,066817329       | 1,80901587  |
| min                 | 0           | 0           | 0,000488281 | 0,00012207        | 0,120849609 |
| 25%                 | 0,020019531 | 0,071044922 | 0,039306641 | 0,018554688       | 0,218566895 |
| 50%                 | 0,041748047 | 0,124511719 | 0,079589844 | 0,039306641       | 1,264099121 |
| 75%                 | 0,06640625  | 0,157470703 | 0,088378906 | 0,049194336       | 2,110595703 |
| max                 | 20,11987305 | 20,18005371 | 20,14135742 | 20,06091309       | 24,60620117 |

| CPU percent         | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 2,86129     | 4,00364     | 2,56774     | 3,06930           | 2,60658     |
| std                 | 5,79159     | 5,32061     | 5,49029     | 5,81085           | 5,92468     |
| min                 | 0,00045     | 0,00273     | 0,00091     | 0,00003           | 0,00094     |
| 25%                 | 1,01011     | 2,13799     | 0,96426     | 1,16127           | 0,48994     |
| 50%                 | 1,52390     | 3,11688     | 1,46192     | 1,73768           | 1,21166     |
| 75%                 | 2,27958     | 5,01545     | 2,39327     | 2,53663           | 2,26611     |
| max                 | 67,60600    | 70,88016    | 66,89603    | 67,77507          | 68,98564    |

| Disk Used percent   | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,259999716 | 0,330586734 | 0,234154998 | 0,22732025        | 0,23186061  |
| std                 | 0,064575655 | 0,177006749 | 0,075067711 | 0,05661001        | 0,054958305 |
| min                 | 0,129551392 | 0,002296906 | 0,090897064 | 0,110502701       | 0,118519287 |
| 25%                 | 0,218227482 | 0,125038261 | 0,179212189 | 0,187156963       | 0,192772961 |
| 50%                 | 0,258266106 | 0,401253204 | 0,218677406 | 0,220283623       | 0,229684982 |
| 75%                 | 0,309353943 | 0,483326759 | 0,293228855 | 0,270952549       | 0,272180901 |
| max                 | 0,456837387 | 0,637720795 | 0,469313354 | 0,433047028       | 0,433176727 |

| Memory Used percent | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 1,634460435 | 1,727028001 | 1,822268852 | 1,369745787       | 1,538493502 |
| std                 | 1,349076813 | 1,437409192 | 1,474835675 | 1,41160957        | 1,448397087 |
| min                 | 0,002147217 | 0,000792847 | 0,000168152 |       0,00002945  | 0,000433655 |
| 25%                 | 1,041033173 | 1,098759193 | 0,986967773 | 0,689202347       | 0,616725769 |
| 50%                 | 1,458450165 | 1,547357407 | 1,589340286 | 1,131428223       | 1,380378494 |
| 75%                 | 1,912325287 | 2,060930214 | 2,266736259 | 1,661757851       | 2,079248924 |
| max                 | 18,49960861 | 19,25271454 | 18,49569977 | 18,63186493       | 18,3506955  |

| Uptime              | 1           | 2           | 3           | 4                 | 5           |
|---------------------|-------------|-------------|-------------|-------------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124              | 5124        |
| mean                | 0,09435074  | 0,099319926 | 0,132983628 | 0,11614759        | 0,101827882 |
| std                 | 0,02619201  | 0,024826179 | 0,026762162 | 0,038299892       | 0,026241027 |
| min                 | 0,043028979 | 0,045956213 | 0,076580603 | 0,049254565       | 0,040546155 |
| 25%                 | 0,074659479 | 0,080342691 | 0,111127661 | 0,087683762       | 0,082349423 |
| 50%                 | 0,093058575 | 0,098211359 | 0,132655511 | 0,110137042       | 0,100598456 |
| 75%                 | 0,112532977 | 0,117749203 | 0,154411096 | 0,136926398       | 0,122862885 |
| max                 | 0,160644934 | 0,159905701 | 0,189638269 | 0,223073816       | 0,155959668 |

# 3. Modelos LSTM Multivariados {#LSTMM}
En esta sección ubicamos el código fuente del modelo LSTM Univariado y el resultado de las cinco ejecuciones
<p align="center">
    <a href="https://colab.research.google.com/drive/1cMLcz9DKU_lyPo1y3DXcLfp0N63HbLfr">
        <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
    </a>
</p>

## 3.1. Iteración 1

| Variable            | Entrenamiento                                                                          | Pruebas                                                                               |
|---------------------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Free Memory         | ![Free Memory_train_result.png](imgs%2Flstmm%2FFree%20Memory_train_result-1.png)                   | ![Free Memory_test_result.png](imgs%2Flstmm%2FFree%20Memory_test_result-1.png)                   |
| Used Memory         | ![Used Memory_train_result.png](imgs%2Flstmm%2FUsed%20Memory_train_result-1.png)                   | ![Used Memory_test_result.png](imgs%2Flstmm%2FUsed%20Memory_test_result-1.png)                   |
| Free Disk           | ![Free Disk_train_result.png](imgs%2Flstmm%2FFree%20Disk_train_result-1.png)                       | ![Free Disk_test_result.png](imgs%2Flstmm%2FFree%20Disk_test_result-1.png)                       |
| Used Disk           | ![Used Disk_train_result.png](imgs%2Flstmm%2FUsed%20Disk_train_result-1.png)                       | ![Used Disk_test_result.png](imgs%2Flstmm%2FUsed%20Disk_test_result-1.png)                       |
| Disk read/s         | ![Disk read_s_train_result.png](imgs%2Flstmm%2FDisk%20read_s_train_result-1.png)                   | ![Disk read_s_test_result.png](imgs%2Flstmm%2FDisk%20read_s_test_result-1.png)                   |
| Disk write/s        | ![Disk write_s_train_result.png](imgs%2Flstmm%2FDisk%20write_s_train_result-1.png)                 | ![Disk write_s_test_result.png](imgs%2Flstmm%2FDisk%20write_s_test_result-1.png)                 |
| NetBytes In         | ![NetBytes In_train_result.png](imgs%2Flstmm%2FNetBytes%20In_train_result-1.png)                   | ![NetBytes In_test_result.png](imgs%2Flstmm%2FNetBytes%20In_test_result-1.png)                   |
| NetBytes Out        | ![NetBytes Out_train_result.png](imgs%2Flstmm%2FNetBytes%20Out_train_result-1.png)                 | ![NetBytes Out_test_result.png](imgs%2Flstmm%2FNetBytes%20Out_test_result-1.png)                 |
| NetPackets In       | ![NetPackets In_train_result.png](imgs%2Flstmm%2FNetPackets%20In_train_result-1.png)               | ![NetPackets In_test_result.png](imgs%2Flstmm%2FNetPackets%20In_test_result-1.png)               |
| NetPackets Out      |                                                                                          |                                                                                        |
| Rx packets          | ![Rx packets_train_result.png](imgs%2Flstmm%2FRx%20packets_train_result-1.png)                     | ![Rx packets_test_result.png](imgs%2Flstmm%2FRx%20packets_test_result-1.png)                     |
| Tx packets          | ![Tx packets_train_result.png](imgs%2Flstmm%2FTx%20packets_train_result-1.png)                     | ![Tx packets_test_result.png](imgs%2Flstmm%2FTx%20packets_test_result-1.png)                     |
| CPU percent         | ![CPU percent_train_result.png](imgs%2Flstmm%2FCPU%20percent_train_result-1.png)                   | ![CPU percent_test_result.png](imgs%2Flstmm%2FCPU%20percent_test_result-1.png)                   |
| Memory Used percent | ![Memory Used percent_train_result.png](imgs%2Flstmm%2FMemory%20Used%20percent_train_result-1.png) | ![Memory Used percent_test_result.png](imgs%2Flstmm%2FMemory%20Used%20percent_test_result-1.png) |
| Disk Used percent   | ![Disk Used percent_train_result.png](imgs%2Flstmm%2FDisk%20Used%20percent_train_result-1.png)     | ![Disk Used percent_test_result.png](imgs%2Flstmm%2FDisk%20Used%20percent_test_result-1.png)     |
| Uptime              | ![Uptime_train_result.png](imgs%2Flstmm%2FUptime_train_result-1.png)                               | ![Uptime_test_result.png](imgs%2Flstmm%2FUptime_test_result-1.png)                               |

[Inicio](#inicio)

## 3.2. Métricas de Precisión

 | RMSE                                                                     | MAE                                                                     | MAPE                                                                     | 
|--------------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|
 | ![Memory Used percent_rmse.png](imgs%2Flstmm%2FMemory%20Used%20percent_rmse-result-1.png) | ![Memory Used percent_ma.png](imgs%2Flstmm%2FMemory%20Used%20percent_mae-result-1.png) | ![Memory Used percent_mape.png](imgs%2Flstmm%2FMemory%20Used%20percent_mape-result-1.png) | 

[Inicio](#inicio)

## Contactos 
Si tiene dudas o sugerencias puede contactarse al correo electrónico xiguesan@upv.edu.es 

[Inicio](#inicio)
