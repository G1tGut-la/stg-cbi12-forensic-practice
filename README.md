# (CIB-12) Forénsica Digital
# Caso #1

### 1.	¿Cuál es el hash (SHA1 O SHA256) de los dispositivos analizados?

![Hash DSK1](/img/1/DSK1.png)

![Hash DSK1](/img/1/RMV1.png)

![Hash DSK1](/img/1/RMV2.png)

![Hash DSK1](/img/1/RMV3.png)

### 2.	¿Qué sistema operativo tenía la computadora instalada? ¿En qué fecha y en qué hora se instaló?

![OS Version](/img/2/OSVer.png)
```
Description: untitled
Acquired Date: Thu Mar  5 14:41:43 2020
System Date: Thu Mar  5 14:41:43 2020
Acquiry Operating System: Win 201x
Acquiry Software Version: ADI4.2.0.13
```

### 3.	¿Quién es el propietario del sistema?

Se muestra una lista con los usuarios locales del sistema

![OS Version](/img/3/List.png)

De estos, el nombre del usuario principal del sistema es `informant`.

Aunque el nombre real del usuario se puede ver en documentos oficiales de su empresa como:
`Iaman Informant`

### 4.	¿Cuál es el ajuste horario del equipo o formato de hora Latino o americano?

`Timezone	America/Los_Angeles`

### 5.	Enumere todas las cuentas de usuario del sistema (excepto las propias del Sistema Operativo como: Administrador, Invitado, etc.).

![OS Accounts](/img/3/List.png)

### 6.	¿Quién fue el último usuario en iniciar sesión en el equipo?

Quedan registros en el reporte SAM de Autopsy que el ultimo usuario de logearse fue el *Administrador* el `Sun Nov 21 03:47:20 2010 Z`, el segundo ultimo (que no era usuario por defecto del sistema) fue *informant* el `Wed Mar 25 13:06:08 2015 Z`

### 7.	¿Cuándo fue la última fecha y hora de apagado del equipo?

Segun el archivo de registro de Windows, el valor seria `Wed, 25 Mar 2015 15:31:05`

![OS Version](/img/7/image.png)

### 8.	¿Cuál fue la última dirección IP asignada al equipo? ¿Se asignó por DHCP o estáticamente?

La ultima IP se obtuvo por DHCP, y fue la `10.11.11.129`

![OS Version](/img/8/image.png)

### 9.	¿Qué aplicaciones instaladas tenía el equipo?

[Se pueden consultar la lista exportada aqui](/Programs.md)

### 10.	¿Qué navegadores de Internet se utilizaban?

Se puede visualizar en el historial extraido el uso de los navegadores:
- Google Chrome
- Internet Explorer
- Microsoft Edge

### 11.	¿A qué sitios web se accedió y en qué hora?

[Se pueden consultar la lista exportada aqui](/WebHistory.md)

### 12.	¿Qué búsquedas se realizaron a través de los buscadores de Internet?

[Se pueden consultar la lista exportada aqui](/WebSeach.md)

### 13.	¿Qué búsquedas realizó el usuario a través de la barra de búsqueda del explorador de Windows?

Segun los datos del registro de windows, el ultimo valor buscado fue la palabra `s e c r e t`

![Search](/img/13/image.png)

### 14.	¿Qué aplicación utilizaba para el envío y la recepción de correos electrónicos?

El programa utilizado por defecto para los correos encontrados fue `Microsoft Outlook`

![Search](/img/14/image.png)

### 15.	¿Qué cuentas de correo se encontraban configuradas?

Unicamente se encuentra rgistrada la cuenta `spy.conspirator@nist.gov`

![Search](/img/15/image.png)

### 16.	¿Qué dispositivos de almacenamiento externo se conectaron al equipo?

[Se pueden consultar la lista exportada aqui](/AtachDevice.md)

### 17.	¿Cuál es la dirección IP de la unidad de red compartida de la empresa?

Se puden visualizar el acceso hacia algunos archivos alojados en `10.11.11.128`

### 18.	Enumere todos los archivos que se abrieron en la unidad de red de la empresa.

![Search](/img/17/image.png)

### 19.	Encuentre en el PC rastros relacionados con los servicios en la nube (nombre del servicio, archivos de registro…).

Se encuentran los ejecutables de Google Drive y archivos de registro

![Search](/img/19/CloudStg.png)

![Search](/img/19/CloudTegFiles.png)

### 20.	¿Qué archivos se eliminaron de Google Drive? (Sugerencia: busca un archivo de registro de transacciones de Google Drive).

Se borraron los propios archivos de configuracion y registro de Google Drive

![Search](/img/20/CloudDelete.png)


### 21.	Identificar la información de la cuenta utilizada para sincronizar Google Drive.

Se detecta en los archivo de registro el nombre del usuario `iaman.informant.personal@gmail.com`

### 22.	¿Qué software se utilizó para grabar el CD?

No se detecta el programa de grabacion dentro de el resgistro de programas instalados. Se da a entender, que se utilizo el propio Windows Explorer para la transferencia de archivos a disco.

### 23.	¿Cuándo grabó el sospechoso el CD?

Se detecta su fecha de creacion el:
```
Acquired Date: Thu Mar  5 16:19:48 2020
System Date: Thu Mar  5 16:19:48 2020
```

### 24.	Identifique todas las marcas de tiempo relacionadas con un archivo de renuncia (en formato DOCX) en el escritorio de Windows.

![ResignationLetterTimestamp](/img/24/image.png)

### 25.	¿Cómo y cuándo imprimió el sospechoso un archivo de renuncia?

No se pudo encontrar el dato de impresion del Resignation_Letter....docx

### 26.	¿Dónde se encuentran los archivos de la aplicación Sticky Note (notas)? Identifique las notas almacenadas.

![Sticky Notes](/img/26/image.png)

```
Tomorrow...

Everything will be OK...
```

### 27.	¿Qué acciones se llevaron a cabo para complicar el análisis forense del equipo el día 25 de marzo de 2015?

Se llevaron a cabo varias acciones de limpieza de evidencias, se borraron archivos, se ejecuto software de limpieza como Eraser y Ccleaner.

### 28.	Recupere los archivos borrados de los USB. ¿Hay algún archivo de interés?

Existen varios archivos eliminados en el sistema de USBs

![Deleted Files](/img/28/image.png)

Ningun archivo en particular es de interes, sino mas bien, un conjunto de archivos que referencian un llamado `secret_project` el cual aparenta ser un conjunto de datos confidenciales de varias universidades y agencias federales de EEUU.

### 29.	¿Qué archivos se copiaron del PC a los USB?

Los archivos relacionados al `secret_project`.

### 30.	Recupere los archivos ocultos del CD. ¿Hay algún archivo de interés?

Igual que en los USBs, varios archivos relacionados al `secret_project`.

![CD Files](/img/30/image.png)

### 31.	Examine la papelera de reciclaje del PC. ¿Hay algún archivo de interés?

Unicamente se encuentran los archivos de la ruta `AppData\Local\Microsoft\Windows\Burn\Burn` la cual es la ruta temporal de los archivos que se copian a disco (a la hora de quemar un disco).
