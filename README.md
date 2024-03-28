# [Bienvenido](#inicio)

En esta página, usted encontrara información relevante asociada al artículo _Modelos LSTM para la Predicción de Calidad de Servicios Cloud_.

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

| Free   Memory       | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,15934     | 0,14065     | 0,12946     | 0,10459     | 0,11971     |
| std                 | 0,11323     | 0,11829     | 0,11392     | 0,10321     | 0,11815     |
| min                 | 0,00012     | 0,00023     | 0,00016     | 0,00002     | 0,00003     |
| 25%                 | 0,11003     | 0,08072     | 0,06782     | 0,04869     | 0,06237     |
| 50%                 | 0,14799     | 0,12374     | 0,11651     | 0,07951     | 0,10182     |
| 75%                 | 0,18923     | 0,17579     | 0,15841     | 0,12726     | 0,14624     |
| max                 | 1,52110     | 1,49402     | 1,53980     | 1,38043     | 1,57954     |

[Inicio](#inicio)

| Used Memory         | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,13165     | 0,11855     | 0,12388     | 0,11475     | 0,09401     |
| std                 | 0,11769     | 0,09469     | 0,11848     | 0,12294     | 0,12014     |
| min                 | 0,00007     | 0,00004     | 0,00007     | 0,00018     | 0,00002     |
| 25%                 | 0,07807     | 0,07383     | 0,06620     | 0,04293     | 0,02958     |
| 50%                 | 0,11426     | 0,10426     | 0,10700     | 0,08880     | 0,06583     |
| 75%                 | 0,15894     | 0,14276     | 0,15400     | 0,15408     | 0,11689     |
| max                 | 1,55377     | 1,41339     | 1,54666     | 1,57722     | 1,60782     |

[Inicio](#inicio)

| Free Disk           | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,39327     | 0,26218     | 0,30336     | 0,40992     | 0,33795     |
| std                 | 0,17899     | 0,06748     | 0,08697     | 0,12887     | 0,08782     |
| min                 | 0,08927     | 0,11833     | 0,07839     | 0,12674     | 0,13629     |
| 25%                 | 0,22936     | 0,21448     | 0,23766     | 0,30943     | 0,25806     |
| 50%                 | 0,38243     | 0,26330     | 0,31212     | 0,40692     | 0,34819     |
| 75%                 | 0,53830     | 0,30125     | 0,35737     | 0,52198     | 0,39428     |
| max                 | 0,91217     | 0,57225     | 0,65038     | 0,77156     | 0,65927     |

[Inicio](#inicio)

| Used Disk           | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,37287     | 0,28410     | 0,29853     | 0,30329     | 0,37557     |
| std                 | 0,10981     | 0,07639     | 0,17230     | 0,11061     | 0,10008     |
| min                 | 0,11532     | 0,13148     | 0,00037     | 0,11261     | 0,16461     |
| 25%                 | 0,28941     | 0,23126     | 0,18381     | 0,22036     | 0,30348     |
| 50%                 | 0,37511     | 0,28892     | 0,27027     | 0,28606     | 0,37373     |
| 75%                 | 0,45005     | 0,33608     | 0,41753     | 0,38510     | 0,44398     |
| max                 | 0,69442     | 0,57277     | 0,76552     | 0,67038     | 0,66889     |

[Inicio](#inicio)

| Disk read/s         | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 376,52280   | 250,16479   | 323,42744   | 298,77967   | 429,99931   |
| std                 | 1770,97640  | 1772,82273  | 1763,92616  | 1765,29880  | 1796,11925  |
| min                 | 0,89859     | 1,74948     | 0,09071     | 1,74502     | 0,01975     |
| 25%                 | 167,24944   | 68,46366    | 78,56801    | 125,02401   | 145,20347   |
| 50%                 | 247,79701   | 106,00414   | 226,74315   | 142,04401   | 225,69562   |
| 75%                 | 350,23855   | 109,25307   | 249,12335   | 168,38556   | 454,12071   |
| max                 | 23972,14668 | 23594,87092 | 23616,72048 | 23514,56400 | 24168,01485 |

[Inicio](#inicio)

| Disk write/s        | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 18,37193    | 18,72588    | 16,09431    | 20,33329    | 12,84666    |
| std                 | 10,23192    | 10,32020    | 9,62403     | 12,15374    | 8,51375     |
| min                 | 0,00185     | 0,01326     | 0,00023     | 0,00061     | 0,00900     |
| 25%                 | 7,26342     | 8,11194     | 6,23049     | 6,98521     | 6,17286     |
| 50%                 | 23,85157    | 23,44280    | 20,05036    | 24,62560    | 11,81955    |
| 75%                 | 27,69763    | 27,38998    | 24,01921    | 31,48181    | 17,47082    |
| max                 | 30,42824    | 34,47646    | 33,82572    | 37,81199    | 43,39380    |

[Inicio](#inicio)

| NetBytes In         | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,07687     | 0,07708     | 0,10034     | 0,07777     | 0,07509     |
| std                 | 0,28985     | 0,29107     | 0,28751     | 0,29572     | 0,29418     |
| min                 | 0,02486     | 0,00923     | 0,02478     | 0,00002     | 0,00012     |
| 25%                 | 0,03409     | 0,02704     | 0,06759     | 0,03444     | 0,02923     |
| 50%                 | 0,06292     | 0,06857     | 0,08581     | 0,05342     | 0,05511     |
| 75%                 | 0,08719     | 0,08713     | 0,11216     | 0,09756     | 0,09915     |
| max                 | 4,97514     | 5,01071     | 4,97419     | 5,12155     | 5,09915     |
[Inicio](#inicio)
| NetBytes Out        | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,10284     | 0,09288     | 0,85617     | 0,09631     | 0,08019     |
| std                 | 0,29572     | 0,28913     | 1,59130     | 0,28933     | 0,29587     |
| min                 | 0,00020     | 0,03469     | 0,00055     | 0,03021     | 0,00029     |
| 25%                 | 0,03051     | 0,04230     | 0,02755     | 0,03852     | 0,03664     |
| 50%                 | 0,04529     | 0,07794     | 0,03547     | 0,09710     | 0,06777     |
| 75%                 | 0,18649     | 0,11865     | 0,60215     | 0,12171     | 0,07759     |
| max                 | 5,01326     | 4,96428     | 5,03547     | 4,96979     | 5,12844     |

[Inicio](#inicio)

| NetPackets In       | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,11671     | 0,10788     | 0,09921     | 0,11579     | 0,08025     |
| std                 | 0,29098     | 0,29000     | 0,29213     | 0,29476     | 0,29110     |
| min                 | 0,00546     | 0,00183     | 0,02176     | 0,00020     | 0,00130     |
| 25%                 | 0,05389     | 0,03977     | 0,03702     | 0,05736     | 0,03506     |
| 50%                 | 0,12318     | 0,12863     | 0,09790     | 0,11101     | 0,08299     |
| 75%                 | 0,14915     | 0,13504     | 0,11797     | 0,12930     | 0,08481     |
| max                 | 5,05396     | 4,99812     | 5,03702     | 5,12930     | 4,99870     |

[Inicio](#inicio)

| NetPackets Out      | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,07924     | 0,27205     | 0,07998     | 0,07610     | 0,10305     |
| std                 | 0,29211     | 0,32115     | 0,29142     | 0,29224     | 0,29011     |
| min                 | 0,00002     | 0,00008     | 0,02352     | 0,00095     | 0,01234     |
| 25%                 | 0,01159     | 0,13729     | 0,03429     | 0,02718     | 0,05139     |
| 50%                 | 0,08572     | 0,19236     | 0,05268     | 0,03988     | 0,07475     |
| 75%                 | 0,11187     | 0,41698     | 0,07864     | 0,10758     | 0,13599     |
| max                 | 5,00569     | 5,45223     | 4,97648     | 5,00095     | 5,05139     |

[Inicio](#inicio)

| Rx packets          | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,20660     | 0,19583     | 0,20156     | 0,26065     | 0,30150     |
| std                 | 1,06144     | 1,06290     | 1,06150     | 1,05360     | 1,05078     |
| min                 | 0,00793     | 0,00122     | 0,03235     | 0,00000     | 0,00000     |
| 25%                 | 0,02075     | 0,02380     | 0,04016     | 0,09253     | 0,05322     |
| 50%                 | 0,10455     | 0,07867     | 0,05261     | 0,12976     | 0,19507     |
| 75%                 | 0,11340     | 0,09363     | 0,06055     | 0,15125     | 0,23682     |
| max                 | 20,13794    | 20,11182    | 20,13525    | 20,23218    | 20,32996    |

[Inicio](#inicio)

| Tx packets          | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,18548     | 0,25221     | 0,20455     | 0,17454     | 1,54210     |
| std                 | 1,06482     | 1,05515     | 1,06131     | 1,06682     | 1,80902     |
| min                 | 0,00000     | 0,00000     | 0,00049     | 0,00012     | 0,12085     |
| 25%                 | 0,02002     | 0,07104     | 0,03931     | 0,01855     | 0,21857     |
| 50%                 | 0,04175     | 0,12451     | 0,07959     | 0,03931     | 1,26410     |
| 75%                 | 0,06641     | 0,15747     | 0,08838     | 0,04919     | 2,11060     |
| max                 | 20,11987    | 20,18005    | 20,14136    | 20,06091    | 24,60620    |

[Inicio](#inicio)

| CPU percent         | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 2,86129     | 4,00364     | 2,56774     | 3,06930     | 2,60658     |
| std                 | 5,79159     | 5,32061     | 5,49029     | 5,81085     | 5,92468     |
| min                 | 0,00045     | 0,00273     | 0,00091     | 0,00003     | 0,00094     |
| 25%                 | 1,01011     | 2,13799     | 0,96426     | 1,16127     | 0,48994     |
| 50%                 | 1,52390     | 3,11688     | 1,46192     | 1,73768     | 1,21166     |
| 75%                 | 2,27958     | 5,01545     | 2,39327     | 2,53663     | 2,26611     |
| max                 | 67,60600    | 70,88016    | 66,89603    | 67,77507    | 68,98564    |

[Inicio](#inicio)

| Disk Used percent   | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,26000     | 0,33059     | 0,23415     | 0,22732     | 0,23186     |
| std                 | 0,06458     | 0,17701     | 0,07507     | 0,05661     | 0,05496     |
| min                 | 0,12955     | 0,00230     | 0,09090     | 0,11050     | 0,11852     |
| 25%                 | 0,21823     | 0,12504     | 0,17921     | 0,18716     | 0,19277     |
| 50%                 | 0,25827     | 0,40125     | 0,21868     | 0,22028     | 0,22968     |
| 75%                 | 0,30935     | 0,48333     | 0,29323     | 0,27095     | 0,27218     |
| max                 | 0,45684     | 0,63772     | 0,46931     | 0,43305     | 0,43318     |

[Inicio](#inicio)

| Memory Used percent | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 1,63446     | 1,72703     | 1,82227     | 1,36975     | 1,53849     |
| std                 | 1,34908     | 1,43741     | 1,47484     | 1,41161     | 1,44840     |
| min                 | 0,00215     | 0,00079     | 0,00017     | 0,00003     | 0,00043     |
| 25%                 | 1,04103     | 1,09876     | 0,98697     | 0,68920     | 0,61673     |
| 50%                 | 1,45845     | 1,54736     | 1,58934     | 1,13143     | 1,38038     |
| 75%                 | 1,91233     | 2,06093     | 2,26674     | 1,66176     | 2,07925     |
| max                 | 18,49961    | 19,25271    | 18,49570    | 18,63186    | 18,35070    |

[Inicio](#inicio)

| Uptime              | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5124        | 5124        | 5124        | 5124        | 5124        |
| mean                | 0,09435     | 0,09932     | 0,13298     | 0,11615     | 0,10183     |
| std                 | 0,02619     | 0,02483     | 0,02676     | 0,03830     | 0,02624     |
| min                 | 0,04303     | 0,04596     | 0,07658     | 0,04925     | 0,04055     |
| 25%                 | 0,07466     | 0,08034     | 0,11113     | 0,08768     | 0,08235     |
| 50%                 | 0,09306     | 0,09821     | 0,13266     | 0,11014     | 0,10060     |
| 75%                 | 0,11253     | 0,11775     | 0,15441     | 0,13693     | 0,12286     |
| max                 | 0,16064     | 0,15991     | 0,18964     | 0,22307     | 0,15596     |

[Inicio](#inicio)

# 3. Modelos LSTM Multivariados {#LSTMM}
En esta sección ubicamos el código fuente del modelo LSTM Univariado y el resultado de las cinco ejecuciones
<p align="center">
    <a href="https://colab.research.google.com/drive/1cMLcz9DKU_lyPo1y3DXcLfp0N63HbLfr">
        <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
    </a>
</p>
[Inicio](#inicio)

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

## 3.3. Cálculo MRA

| Free   Memory       | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130,0      | 5130,0      | 5130,0      | 5130,0      | 5130,0      |
| mean                | 0,28241     | 0,31229     | 0,29249     | 0,27462     | 0,32591     |
| std                 | 0,13904     | 0,12656     | 0,13092     | 0,12371     | 0,14492     |
| min                 | 0,00014     | 0,00132     | 0,00005     | 0,00006     | 0,00008     |
| 25%                 | 0,18898     | 0,22021     | 0,21426     | 0,20593     | 0,23342     |
| 50%                 | 0,31256     | 0,34554     | 0,31218     | 0,29005     | 0,34683     |
| 75%                 | 0,36719     | 0,39485     | 0,37707     | 0,34722     | 0,42260     |
| max                 | 1,37501     | 1,31839     | 1,40493     | 1,35324     | 1,40265     |

| Used Memory         | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,26608     | 0,27180     | 0,27624     | 0,27769     | 0,27789     |
| std                 | 0,13830     | 0,12932     | 0,12885     | 0,12665     | 0,13986     |
| min                 | 0,00012     | 0,00074     | 0,00008     | 0,00014     | 0,00001     |
| 25%                 | 0,17455     | 0,18527     | 0,19802     | 0,20443     | 0,17975     |
| 50%                 | 0,29332     | 0,29344     | 0,30371     | 0,29631     | 0,30555     |
| 75%                 | 0,35826     | 0,34915     | 0,35196     | 0,36114     | 0,36558     |
| max                 | 1,45578     | 1,40652     | 1,40197     | 1,37102     | 1,44833     |

[Inicio](#inicio)


| Free Disk           | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,36805     | 0,17266     | 0,12506     | 0,14574     | 0,34290     |
| std                 | 0,08103     | 0,10322     | 0,09427     | 0,08265     | 0,14794     |
| min                 | 0,19581     | 0,00001     | 0,00021     | 0,00013     | 0,07026     |
| 25%                 | 0,32378     | 0,08558     | 0,05204     | 0,07119     | 0,23751     |
| 50%                 | 0,35897     | 0,17366     | 0,10037     | 0,15230     | 0,33271     |
| 75%                 | 0,41740     | 0,25756     | 0,18279     | 0,21678     | 0,46230     |
| max                 | 0,67984     | 0,52658     | 0,51738     | 0,44020     | 0,78773     |

| Used Disk           | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,29358     | 0,14990     | 0,22831     | 0,12628     | 0,27817     |
| std                 | 0,11260     | 0,10822     | 0,09989     | 0,09734     | 0,09514     |
| min                 | 0,05798     | 0,00006     | 0,00480     | 0,00009     | 0,08325     |
| 25%                 | 0,21248     | 0,07428     | 0,16497     | 0,03847     | 0,21269     |
| 50%                 | 0,28448     | 0,12390     | 0,22989     | 0,09561     | 0,26542     |
| 75%                 | 0,37036     | 0,19900     | 0,28158     | 0,21138     | 0,34795     |
| max                 | 0,65849     | 0,56800     | 0,63433     | 0,47738     | 0,61552     |

[Inicio](#inicio)


| Disk read/s         | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 858,58005   | 781,71659   | 928,29864   | 605,39797   | 705,18619   |
| std                 | 1750,87678  | 1770,04091  | 1813,90422  | 1741,27215  | 1787,65748  |
| min                 | 1,00594     | 0,62365     | 0,40980     | 0,06850     | 0,87268     |
| 25%                 | 443,46779   | 211,70404   | 451,69400   | 211,75353   | 202,97284   |
| 50%                 | 632,85129   | 532,56074   | 764,79286   | 411,84323   | 434,95335   |
| 75%                 | 876,44686   | 965,01843   | 1050,08904  | 685,83477   | 702,58633   |
| max                 | 24786,28157 | 23309,02202 | 24985,23677 | 23338,46739 | 23481,95955 |

| Disk write/s        | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 31,35074    | 20,99705    | 15,69074    | 15,18520    | 23,57756    |
| std                 | 20,63969    | 15,24319    | 12,24616    | 10,39073    | 17,56624    |
| min                 | 0,04974     | 0,00834     | 0,00487     | 0,00876     | 0,00049     |
| 25%                 | 14,15917    | 8,94544     | 4,68892     | 7,24938     | 9,98567     |
| 50%                 | 29,79305    | 18,67849    | 12,42525    | 13,21312    | 19,58096    |
| 75%                 | 44,85026    | 30,83503    | 26,06541    | 20,40204    | 34,60907    |
| max                 | 143,85237   | 107,19014   | 80,97169    | 77,47413    | 102,96588   |

[Inicio](#inicio)


| NetBytes In         | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,28429     | 0,37393     | 0,17597     | 0,22538     | 0,20274     |
| std                 | 0,35203     | 0,30155     | 0,31380     | 0,30166     | 0,32113     |
| min                 | 0,00007     | 0,00015     | 0,00001     | 0,00197     | 0,00001     |
| 25%                 | 0,05092     | 0,22439     | 0,06978     | 0,10278     | 0,08115     |
| 50%                 | 0,19854     | 0,35447     | 0,12040     | 0,21361     | 0,15219     |
| 75%                 | 0,47261     | 0,46839     | 0,22231     | 0,28494     | 0,24103     |
| max                 | 5,35303     | 4,85552     | 5,09825     | 4,94060     | 5,28115     |

| NetBytes Out        | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,36880     | 0,18572     | 0,15861     | 0,29979     | 0,35150     |
| std                 | 0,30691     | 0,32039     | 0,30054     | 0,33147     | 0,35249     |
| min                 | 0,00019     | 0,00002     | 0,00004     | 0,00003     | 0,00043     |
| 25%                 | 0,18204     | 0,06051     | 0,05737     | 0,08565     | 0,19311     |
| 50%                 | 0,34408     | 0,12591     | 0,13557     | 0,26924     | 0,25279     |
| 75%                 | 0,48902     | 0,25075     | 0,20152     | 0,43362     | 0,50927     |
| max                 | 4,89125     | 5,13405     | 5,19951     | 5,07257     | 5,25163     |

[Inicio](#inicio)


| NetPackets In       | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,24789     | 0,24025     | 0,20984     | 0,21661     | 0,18865     |
| std                 | 0,33635     | 0,33709     | 0,31503     | 0,33258     | 0,32242     |
| min                 | 0,00001     | 0,00000     | 0,00000     | 0,00012     | 0,00023     |
| 25%                 | 0,06280     | 0,06556     | 0,07196     | 0,06457     | 0,06194     |
| 50%                 | 0,20743     | 0,15665     | 0,17794     | 0,13632     | 0,15291     |
| 75%                 | 0,30660     | 0,37424     | 0,27737     | 0,35654     | 0,24645     |
| max                 | 5,16629     | 5,09533     | 5,38321     | 5,42085     | 5,30424     |

| NetPackets Out      | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,20492     | 0,36761     | 0,20391     | 0,33646     | 0,30003     |
| std                 | 0,30566     | 0,30569     | 0,30511     | 0,31925     | 0,33912     |
| min                 | 0,00004     | 0,07185     | 0,00030     | 0,00009     | 0,00011     |
| 25%                 | 0,09672     | 0,22164     | 0,09002     | 0,17708     | 0,09515     |
| 50%                 | 0,16974     | 0,34030     | 0,16861     | 0,29134     | 0,29640     |
| 75%                 | 0,26556     | 0,41838     | 0,26462     | 0,45725     | 0,38284     |
| max                 | 5,31180     | 4,82230     | 5,13153     | 5,21575     | 5,03333     |

[Inicio](#inicio)


| Rx packets          | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,62119     | 0,40882     | 0,36628     | 0,33130     | 0,45176     |
| std                 | 1,00903     | 1,04530     | 1,06119     | 1,05782     | 1,04194     |
| min                 | 0,00049     | 0,00012     | 0,00000     | 0,00012     | 0,00012     |
| 25%                 | 0,38773     | 0,10916     | 0,10303     | 0,05615     | 0,11121     |
| 50%                 | 0,52539     | 0,23004     | 0,15326     | 0,12274     | 0,25568     |
| 75%                 | 0,60522     | 0,36154     | 0,33902     | 0,29953     | 0,52832     |
| max                 | 20,59973    | 20,28601    | 20,16614    | 20,30127    | 20,59375    |

| Tx packets          | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,45018     | 0,44136     | 0,30894     | 0,45805     | 0,57856     |
| std                 | 1,03897     | 1,03953     | 1,05887     | 1,05086     | 1,03136     |
| min                 | 0,00220     | 0,00000     | 0,00000     | 0,00000     | 0,00012     |
| 25%                 | 0,19727     | 0,10916     | 0,05298     | 0,13586     | 0,27164     |
| 50%                 | 0,29572     | 0,34058     | 0,11084     | 0,27374     | 0,38745     |
| 75%                 | 0,40704     | 0,46982     | 0,25281     | 0,54370     | 0,66470     |
| max                 | 20,28467    | 20,48438    | 20,24292    | 20,70996    | 20,74524    |

[Inicio](#inicio)


| CPU percent         | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 2,92899     | 2,89177     | 3,08422     | 3,18495     | 3,34569     |
| std                 | 6,04896     | 5,86568     | 5,98560     | 5,99578     | 6,09525     |
| min                 | 0,00169     | 0,00100     | 0,00271     | 0,00068     | 0,00000     |
| 25%                 | 0,50200     | 0,61826     | 0,94740     | 0,81709     | 0,73603     |
| 50%                 | 1,27542     | 1,40559     | 1,57665     | 1,79156     | 1,92252     |
| 75%                 | 2,99755     | 2,93024     | 2,74250     | 3,01853     | 3,56947     |
| max                 | 69,24759    | 69,53050    | 69,69336    | 70,47373    | 70,90491    |

| Disk Used percent   | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,21049     | 0,10912     | 0,13542     | 0,08632     | 0,23609     |
| std                 | 0,06754     | 0,06817     | 0,07630     | 0,05745     | 0,05658     |
| min                 | 0,04508     | 0,00000     | 0,00026     | 0,00001     | 0,13394     |
| 25%                 | 0,16177     | 0,05799     | 0,07200     | 0,03171     | 0,20462     |
| 50%                 | 0,20391     | 0,09806     | 0,12704     | 0,10064     | 0,22693     |
| 75%                 | 0,25279     | 0,14415     | 0,19159     | 0,12558     | 0,26765     |
| max                 | 0,44488     | 0,32947     | 0,40548     | 0,32808     | 0,45077     |

[Inicio](#inicio)


| Memory Used percent | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 3,52795     | 3,46815     | 3,42861     | 2,89382     | 3,50163     |
| std                 | 1,70585     | 1,61180     | 1,56475     | 1,51895     | 1,76417     |
| min                 | 0,00033     | 0,00687     | 0,00101     | 0,00029     | 0,00130     |
| 25%                 | 2,35052     | 2,37607     | 2,39385     | 2,07374     | 2,27479     |
| 50%                 | 3,91634     | 3,72931     | 3,68677     | 2,97657     | 3,85445     |
| 75%                 | 4,78203     | 4,54352     | 4,41872     | 3,75646     | 4,77864     |
| max                 | 17,22146    | 17,28366    | 17,05990    | 17,20566    | 17,99937    |

| Uptime              | 1           | 2           | 3           | 4           | 5           |
|---------------------|-------------|-------------|-------------|-------------|-------------|
| count               | 5130        | 5130        | 5130        | 5130        | 5130        |
| mean                | 0,17980     | 0,16420     | 0,16245     | 0,16141     | 0,19284     |
| std                 | 0,02467     | 0,02359     | 0,02637     | 0,02363     | 0,02723     |
| min                 | 0,12506     | 0,10367     | 0,07599     | 0,10571     | 0,12978     |
| 25%                 | 0,16058     | 0,14112     | 0,14312     | 0,13910     | 0,16878     |
| 50%                 | 0,17887     | 0,16768     | 0,16326     | 0,16355     | 0,19350     |
| 75%                 | 0,19856     | 0,18437     | 0,18359     | 0,18086     | 0,21372     |
| max                 | 0,23613     | 0,20921     | 0,21600     | 0,21024     | 0,26147     |


[Inicio](#inicio)


## Contactos 
Si tiene dudas o sugerencias puede contactarse al correo electrónico xiguesan@upv.edu.es 

[Inicio](#inicio)
