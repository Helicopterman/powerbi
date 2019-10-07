# Map Center HDI 

Guía Instalación de aplicativo HDI en Samsung Smart Signage Platform (SSSP).

## Empezando

Lo primero a tomar en cuenta es que existen 2 métodos para la instalación de un paquete en el dispositivo SSSP:

- **USB**
- **Red** 

En este documento se sugiere la instalación del aplicativo mediante Red.

## Prerrequisitos

Es necesario que los dispositivos SSSP estén en **modo desarrollador**, para habilitar el modo desarrollador primero habilitaremos **URL Launcher**.

para habilitar URL Launcher: 

```
- Ir a Menú
  - Seleccionar System
  - Cambiar la opción de Playvia a URL Launcher
```
 
para habilitar Modo desarrollador: 

```
- Ir a Home
  - Seleccionar URL Launcher Settings
  - Entrar a Developer mode y cambiar la opción del mismo nombre a ON 
```

## Instalación o despliegue 

Una vez que tengamos el compilado del aplicativo con extensión **.wgt** se debe generar un archivo XML con nombre **sssp_config.xml**

Archivo sssp_config.xml

```
<?xml version="1.0" encoding="UTF-8"?>

<widget>

<ver>1.0.0</ver>

<widgetname>HDI</widgetname>

<webtype>tizen</webtype>

</widget>

```

En este ejemplo el compilado tiene por nombre **HDI.wgt** y su version es la **1.0.0** que hacen referencia en el archivo XML.

Estos archivos deberán ser colocados en una misma ubicación de red visible para la pantalla, para esto se utiliza el Web Server [Apache](https://httpd.apache.org/docs/2.4/es/urlmapping.html)

Una vez los archivos estén listos, debemos acceder al dispositivo SSSP mediante la opción **URL Launcher Settings** y elegimos **Install Web APP** esto abrirá un cuadro de dialogo para ingresar la URL donde se encuentran los archivos.


Ejemplo:

```
http://172.30.0.69/apache-server/TV

```

Para la instalacion con **USB** se debe crear una carpeta en raiz con el nombre SSSP y tener un formato ya sea en **NTFS** o **FAT32**, dentro de la carpeta **SSSP** colocaremos los 2 archivos ( **.wgt** y **sssp_config.xml**), conectamos la USB al dispositivo SSSP y mediante la opción **URL Launcher Settings** elegimos **Install From USB Device**.

### NOTA: el dispositivo SSSP debe contar con conexión a internet para la instalación

## Autores

* **Juan José Olmos Manríquez** *07/10/2019*

