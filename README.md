# Map Center HDI 

Guia Instalacion de aplicativo HDI en Samsung Smart Signage Platform (SSSP).

## Empezando

Lo primero a tomar en cuenta es que existen 2 metodos para la instalacion de un paquete en el dispositivo SSSP:

- **USB**
- **Red** 

este documento Sugiere la instalacion del aplicativo mediante Red.

## Prerrequisitos

Es necesario que los dispositivos SSSP esten en modo **desarrollador**, para habilitar el modo desarrollador se requiere tambien que el modo **URL Launcher** este habilitado.

para habilitar URL Launcher: 

```
- Ir a Menu
  - Seleccionar System
  - Cambiar la opcion de Playvia a URL Launcher
```
 
para habilitar Modo desarrollador: 

```
- Ir a Home
  - Seleccionar URL Launcher Settings
  - Entrar a Developer mode y cambiar la opcion del mismo nombre a ON 
```

## Instalacion o despliegue 

Una ves que tengamos el compilado del aplicativo con extension **.wgt** y el archivo XML con nombre **sssp_config.xml**

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

Estos archivos deberan ser colocados en una ubicacion de red visible para la pantalla, para esto se utiliza un Web Server **Apache** y se deben colocar juntos.

Una vez los archivos esten listos, debemos acceder al dispositivo SSSP mediante la opcion **URL Launcher settings** y elegimos **install Web APP** esto abrira un cuadro de dialogo donde debemos ingresar la URL donde se encuentran los archivos.

Ejemplo:

```
http://localhost/apache-server/TV

```

## NOTA: el dispositivo SSSP debe contar con conexión a internet para la instalacion

## Autores

* **Juan José Olmos Manríquez** *07/10/2019*

