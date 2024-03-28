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

## Contactos 
Si tiene dudas o sugerencias puede contactarse al correo electrónico xiguesan@upv.edu.es 

[Inicio](#inicio)
