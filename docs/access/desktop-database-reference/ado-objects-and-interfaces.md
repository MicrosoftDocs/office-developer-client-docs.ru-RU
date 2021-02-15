---
title: Интерфейсы и объекты ADO
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 539feb1918877189548d0e7cff6ceb28e50abddc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283263"
---
# <a name="ado-objects-and-interfaces"></a>Интерфейсы и объекты ADO

**Область применения**: Access 2013, Office 2013

Связи между этими объектами представлены в объектной модели ActiveX Data Objects (ADO).

Каждый объект может содержаться в соответствующей коллекции. Например, объект [Error](error-object-ado.md) может содержаться в коллекции [Errors.](errors-collection-ado.md) Дополнительные сведения см. в коллекциях [ADO](ado-collections.md) или в определенной теме коллекции.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Объект</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></p></td>
<td><p>Строит объект записи <strong>ADO</strong> из объекта строки OLE <strong>DB</strong> в приложении C/C++.</p></td>
</tr>
<tr class="even">
<td><p><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></p></td>
<td><p>Строит объект ADO <strong>Recordset</strong> из объекта <strong>rowset</strong> OLE DB в приложении C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Command</a></p></td>
<td><p>Определяет определенную команду, которую вы собираетесь выполнить для источника данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Connection</a></p></td>
<td><p>Представляет открытое подключение к источнику данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Ошибка</a></p></td>
<td><p>Содержит сведения об ошибках доступа к данным, относящихся к одной операции с участием поставщика.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Field</a></p></td>
<td><p>Представляет столбец данных с общим типом данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameter-object-ado.md">Параметр</a></p></td>
<td><p>Представляет параметр или аргумент, связанный с объектом <strong>Command</strong> на основе параметризованного запроса или хранимой процедуры.</p></td>
</tr>
<tr class="even">
<td><p><a href="property-object-ado.md">Property</a></p></td>
<td><p>Представляет динамическую характеристику объекта ADO, определенного поставщиком.</p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p>Представляет строку <strong>recordset</strong>или каталог или файл в файловой системе.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p>Представляет весь набор записей из базовой таблицы или результаты выполнения команды. В любой момент объект <strong>Recordset</strong> ссылается только на одну запись в наборе в качестве текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p>Представляет двоичный поток данных.</p></td>
</tr>
</tbody>
</table>

<br/>

