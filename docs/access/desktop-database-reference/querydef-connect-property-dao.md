---
title: QueryDef. Подключение (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 009e49a96ea1cd5ee3db0b96adb9cae4a6bce21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301087"
---
# <a name="querydefconnect-property-dao"></a>QueryDef. Подключение (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое предоставляет сведения об источнике базы данных, используемом в сквозной запрос. Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*expression* .Connect

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Параметры свойства **Connect** сохранены в **String**, состоящей из указателя типа базы данных и нуля либо нескольких параметров, разделенных точкой с запятой. Свойство **Connect** передает дополнительные сведения для ODBC и определенным драйверам ISAM при необходимости.

Чтобы выполнить SQL сквозной запрос на таблице, связанной с файлом базы данных  Microsoft Access, сначала необходимо Подключение свойству базы данных связанной таблицы допустимую строку подключения ODBC.

Путь, как показано в приведенной ниже таблице, содержит полный путь к каталогу, содержащему файлы базы данных, и должен иметь впереди идентификатор DATABASE=. В некоторых случаях (как в случае с базами данных Microsoft Excel и ядра СУБД Microsoft Access) следует включить конкретное имя файла в аргумент пути к базе данных.

Таблица ниже содержит возможные типы базы данных и соответствующие указатели базы данных и пути к параметрам свойства **Connect**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип базы данных</p></th>
<th><p>Указатель</p></th>
<th><p>Пример</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>База данных Microsoft Access</p></td>
<td><p>[database];</p></td>
<td><p>диск: \путь\имяфайла</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>диск: \путь</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>диск: \путь</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>диск: \путь</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>диск: \путь</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>диск: \путь</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>диск: \путь</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>диск: \путь\имяфайла.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>диск: \путь\имяфайла.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 или Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>диск: \путь\имяфайла.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>диск: \путь\имяфайла.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS и WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>диск: \путь\имяфайла.wk1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>диск: \путь\имяфайла.wk3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>диск: \путь\имяфайла.wk4</p></td>
</tr>
<tr class="odd">
<td><p>HTML Import</p></td>
<td><p>HTML Import;</p></td>
<td><p>диск: \путь\имяфайла</p></td>
</tr>
<tr class="even">
<td><p>HTML Export</p></td>
<td><p>HTML Export;</p></td>
<td><p>диск: \путь</p></td>
</tr>
<tr class="odd">
<td><p>Text</p></td>
<td><p>Text;</p></td>
<td><p>диск: \путь</p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</p></td>
<td><p>диск: \путь\имяфайла</p></td>
</tr>
</tbody>
</table>


Если указание только "ODBC;", драйвер ODBC отображает диалоговое окно с перечислением всех зарегистрированных имен источников данных ODBC, чтобы пользователь мог выбрать базу данных.

Если пароль необходим, но не указан в параметрах свойства **Connect**, диалоговое окно входа отображается при первой попытке доступа к таблице со стороны драйвера ODBC и еще раз при закрытии и повторном установлении подключения.

Для данных в Microsoft Exchange обязательный ключ MAPILEVEL должен иметь полностью разрешенный путь к папке (например, "Mailbox - Pat SmithIAlpha/Today"). Путь не включает имя папки, которая будет открываться в качестве таблицы; вместо этого необходимо указать имя этой папки в качестве имени аргумента для метода **CreateTable**. Для ключа TABLETYPE должно быть установлено значение «0», чтобы открыть папку (по умолчанию) или «1», чтобы открыть адресную книгу. Ключ PROFILE по умолчанию относится к профилю, который в настоящее время используется.

На **объекте QueryDef** в рабочей области Microsoft Access можно использовать свойство **Подключение** с свойством ReturnsRecords для создания сквозного запроса SQL ODBC. Тип базы данных строки подключения — "ODBC;", а остальная строка содержит сведения, определенные драйверу ODBC, используемой для доступа к удаленным данным. Дополнительные сведения см. в документации по конкретному драйверу.

> [!NOTE]
> - Необходимо задать значение свойства **Connect** перед настройкой свойства **ReturnsRecords**.
> - Необходимо иметь разрешения на доступ к компьютеру, который содержит сервер базы данных, доступ к которому вы пытаетесь получить доступ.


