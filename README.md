# Bienvenido {#inicio}

En esta página, usted encontrara información relevante asociada al artículo Modelos LSTM para la predicci ́on de calidad de servicios cloud y la metodología de investigación 

## Indice

1. [Datos](#datos)
2. [Modelos LSTM Univariado](#LSTMU)
3. [Modelos LSTM Multivariado](#LSTMM)


## 1. Datos {#Datos}
El conjunto de datos corresponde a la información obtenida de la monitorización del servicio SAlert, el cual esta  compuesto por 16 métricas de calidad como variables de entrada y sus mediciones corresponden en una serie temporal.

- <a href ="./files/datos.csv">  Fuente de datos </a>

### _Datasets_

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

## 2. Modelos LSTM Univariados {#LSTMU}
En esta sección ubicamos el código fuente del modelo LSTM Univariado y el resultado de las cinco ejecuciones

<p align="center">
    <a href="https://colab.research.google.com/drive/1rfBBedaReGYBUKgm2sCVJtxRKFFSPCjE">
        <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
    </a>

</p>

### _ITERACION 1_

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
### _METRICAS DE PRECISION_
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

## 3. Modelos LSTM Multivariados {#LSTMM}
En esta sección ubicamos el código fuente del modelo LSTM Univariado y el resultado de las cinco ejecuciones
<p align="center">
    <a href="https://colab.research.google.com/drive/1cMLcz9DKU_lyPo1y3DXcLfp0N63HbLfr">
        <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
    </a>
</p>

### _ITERACION 1_

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

### _METRICAS DE PRECISION_
 | RMSE                                                                     | MAE                                                                     | MAPE                                                                     | 
|--------------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|
 | ![Memory Used percent_rmse.png](imgs%2Flstmm%2FMemory%20Used%20percent_rmse-result-1.png) | ![Memory Used percent_ma.png](imgs%2Flstmm%2FMemory%20Used%20percent_mae-result-1.png) | ![Memory Used percent_mape.png](imgs%2Flstmm%2FMemory%20Used%20percent_mape-result-1.png) | 

[Inicio](#inicio)

## Contactos 
Si tiene dudas o sugerencias puede contactarse al correo electrónico xiguesan@upv.edu.es 

[Inicio](#inicio)
