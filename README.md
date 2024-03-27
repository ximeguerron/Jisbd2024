# Bienvenido {#inicio}

En esta página, usted encontrara información relevante asociada al artículo Modelos LSTM para la predicci ́on de calidad de servicios cloud y la metodología de investigación 

## Indice

1. [Datos](#datos)
2. [Modelos LSTM Univariado](#LSTMU)
3. [Modelos LSTM Multivariado](#LSTMM)
4. [Estudios primarios seleccionados](#estudios)
5. [Criterios de extracción de datos](#criterios)
6. [Clasificacion de Metricas](#clasificacion)

## 1. Datos {#Datos}
El conjunto de datos corresponde a la información obtenida de la monitorización del servicio SAlert, el cual esta  compuesto por 16 métricas de calidad como variables de entrada y sus mediciones corresponden en una serie temporal.

- <a href ="./files/datos.xls">  Fuente de datos </a>

## 2. Modelos LSTM Univariados {#LSTMU}
En esta sección ubicamos el código fuente del modelo LSTM Univariado y el resultado de las cinco ejecuciones
<p align="center">
    <a href="https://colab.research.google.com/drive/xx">
        <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
    </a>
</p>

| Variable            | Training                                                                            | Testing                                                                                |
|---------------------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Free Memory         | ![Free Memory_train_result.png](imgs%2FFree%20Memory_train_result.png)                   | ![Free Memory_test_result.png](imgs%2FFree%20Memory_test_result.png)                   |
| Used Memory         | ![Used Memory_train_result.png](imgs%2FUsed%20Memory_train_result.png)                   | ![Used Memory_test_result.png](imgs%2FUsed%20Memory_test_result.png)                   |
| Free Disk           | ![Free Disk_train_result.png](imgs%2FFree%20Disk_train_result.png)                       | ![Free Disk_test_result.png](imgs%2FFree%20Disk_test_result.png)                       |
| Used Disk           | ![Used Disk_train_result.png](imgs%2FUsed%20Disk_train_result.png)                       | ![Used Disk_test_result.png](imgs%2FUsed%20Disk_test_result.png)                       |
| Disk read/s         | ![Disk read_s_train_result.png](imgs%2FDisk%20read_s_train_result.png)                   | ![Disk read_s_test_result.png](imgs%2FDisk%20read_s_test_result.png)                   |
| Disk write/s        | ![Disk write_s_train_result.png](imgs%2FDisk%20write_s_train_result.png)                 | ![Disk write_s_test_result.png](imgs%2FDisk%20write_s_test_result.png)                 |
| NetBytes In         | ![NetBytes In_train_result.png](imgs%2FNetBytes%20In_train_result.png)                   | ![NetBytes In_test_result.png](imgs%2FNetBytes%20In_test_result.png)                   |
| NetBytes Out        | ![NetBytes Out_train_result.png](imgs%2FNetBytes%20Out_train_result.png)                 | ![NetBytes Out_test_result.png](imgs%2FNetBytes%20Out_test_result.png)                 |
| NetPackets In       | ![NetPackets In_train_result.png](imgs%2FNetPackets%20In_train_result.png)               | ![NetPackets In_test_result.png](imgs%2FNetPackets%20In_test_result.png)               |
| NetPackets Out      |                                                                                          |                                                                                        |
| Rx packets          | ![Rx packets_train_result.png](imgs%2FRx%20packets_train_result.png)                     | ![Rx packets_test_result.png](imgs%2FRx%20packets_test_result.png)                     |
| Tx packets          | ![Tx packets_train_result.png](imgs%2FTx%20packets_train_result.png)                     | ![Tx packets_test_result.png](imgs%2FTx%20packets_test_result.png)                     |
| CPU percent         | ![CPU percent_train_result.png](imgs%2FCPU%20percent_train_result.png)                   | ![CPU percent_test_result.png](imgs%2FCPU%20percent_test_result.png)                   |
| Memory Used percent | ![Memory Used percent_train_result.png](imgs%2FMemory%20Used%20percent_train_result.png) | ![Memory Used percent_test_result.png](imgs%2FMemory%20Used%20percent_test_result.png) |
| Disk Used percent   | ![Disk Used percent_train_result.png](imgs%2FDisk%20Used%20percent_train_result.png)     | ![Disk Used percent_test_result.png](imgs%2FDisk%20Used%20percent_test_result.png)     |
| Uptime              | ![Uptime_train_result.png](imgs%2FUptime_train_result.png)                               | ![Uptime_test_result.png](imgs%2FUptime_test_result.png)                               |
[Inicio](#inicio)

## 3. Modelos LSTM Multivariados {#LSTMM}
En esta sección ubicamos el código fuente del modelo LSTM Univariado y el resultado de las cinco ejecuciones
<p align="center">
    <a href="https://colab.research.google.com/drive/xx">
        <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
    </a>
</p>

| Variable            | Training                                                                            | Testing                                                                                |
|---------------------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Free Memory         | ![Free Memory_train_result.png](imgs%2FFree%20Memory_train_result-1.png)                   | ![Free Memory_test_result.png](imgs%2FFree%20Memory_test_result-1.png)                   |
| Used Memory         | ![Used Memory_train_result.png](imgs%2FUsed%20Memory_train_result-1.png)                   | ![Used Memory_test_result.png](imgs%2FUsed%20Memory_test_result-1.png)                   |
| Free Disk           | ![Free Disk_train_result.png](imgs%2FFree%20Disk_train_result-1.png)                       | ![Free Disk_test_result.png](imgs%2FFree%20Disk_test_result-1.png)                       |
| Used Disk           | ![Used Disk_train_result.png](imgs%2FUsed%20Disk_train_result-1.png)                       | ![Used Disk_test_result.png](imgs%2FUsed%20Disk_test_result-1.png)                       |
| Disk read/s         | ![Disk read_s_train_result.png](imgs%2FDisk%20read_s_train_result-1.png)                   | ![Disk read_s_test_result.png](imgs%2FDisk%20read_s_test_result-1.png)                   |
| Disk write/s        | ![Disk write_s_train_result.png](imgs%2FDisk%20write_s_train_result-1.png)                 | ![Disk write_s_test_result.png](imgs%2FDisk%20write_s_test_result-1.png)                 |
| NetBytes In         | ![NetBytes In_train_result.png](imgs%2FNetBytes%20In_train_result-1.png)                   | ![NetBytes In_test_result.png](imgs%2FNetBytes%20In_test_result-1.png)                   |
| NetBytes Out        | ![NetBytes Out_train_result.png](imgs%2FNetBytes%20Out_train_result-1.png)                 | ![NetBytes Out_test_result.png](imgs%2FNetBytes%20Out_test_result-1.png)                 |
| NetPackets In       | ![NetPackets In_train_result.png](imgs%2FNetPackets%20In_train_result-1.png)               | ![NetPackets In_test_result.png](imgs%2FNetPackets%20In_test_result-1.png)               |
| NetPackets Out      |                                                                                          |                                                                                        |
| Rx packets          | ![Rx packets_train_result.png](imgs%2FRx%20packets_train_result-1.png)                     | ![Rx packets_test_result.png](imgs%2FRx%20packets_test_result-1.png)                     |
| Tx packets          | ![Tx packets_train_result.png](imgs%2FTx%20packets_train_result-1.png)                     | ![Tx packets_test_result.png](imgs%2FTx%20packets_test_result-1.png)                     |
| CPU percent         | ![CPU percent_train_result.png](imgs%2FCPU%20percent_train_result-1.png)                   | ![CPU percent_test_result.png](imgs%2FCPU%20percent_test_result-1.png)                   |
| Memory Used percent | ![Memory Used percent_train_result.png](imgs%2FMemory%20Used%20percent_train_result-1.png) | ![Memory Used percent_test_result.png](imgs%2FMemory%20Used%20percent_test_result-1.png) |
| Disk Used percent   | ![Disk Used percent_train_result.png](imgs%2FDisk%20Used%20percent_train_result-1.png)     | ![Disk Used percent_test_result.png](imgs%2FDisk%20Used%20percent_test_result-1.png)     |
| Uptime              | ![Uptime_train_result.png](imgs%2FUptime_train_result-1.png)                               | ![Uptime_test_result.png](imgs%2FUptime_test_result-1.png)                               |

[Inicio](#inicio)


## Contactos 
Si tiene dudas o sugerencias puede contactarse al correo electrónico xiguesan@upv.edu.es 

[Inicio](#inicio)
