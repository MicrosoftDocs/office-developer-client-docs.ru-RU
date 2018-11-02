---
title: Объекты и интерфейсы ADO
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa301974b4b417d09b0439b3970ee366eeb5d06e
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910729"
---
# <a name="ado-objects-and-interfaces"></a>Объекты и интерфейсы ADO

**Применимо к**: Access 2013, Office 2013

Отношения между эти объекты, представленные в объектной модели ActiveX Data Objects (ADO).

Каждый объект может содержаться в соответствующие коллекции. Например объект [Error](error-object-ado.md) может содержаться в семейство [Errors](errors-collection-ado.md) . Для получения дополнительных сведений см [ADO семейств сайтов](ado-collections.md) или раздела конкретной коллекции.

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
<td><p>Создает объект ADO <strong>записи</strong> из объекта OLE DB <strong>строки</strong> в приложении C/C++.</p></td>
</tr>
<tr class="even">
<td><p><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></p></td>
<td><p>Создает объект ADO <strong>записей</strong> из объекта OLE DB <strong>строк</strong> в приложении C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Команда</a></p></td>
<td><p>Определяет определенной команде, которые планируется выполнить в источнике данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Подключение</a></p></td>
<td><p>Представляет открытое подключение к источнику данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Ошибка</a></p></td>
<td><p>Содержит сведения об ошибках доступа к данным, которые относятся к одной операции, включающие использование поставщика.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Поле</a></p></td>
<td><p>Представляет столбец данных с типом данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameter-object-ado.md">Параметр</a></p></td>
<td><p>Представляет параметр или аргумент, связанной с объектом <strong>команды</strong> на основе параметризованный запрос или хранимую процедуру.</p></td>
</tr>
<tr class="even">
<td><p><a href="property-object-ado.md">Свойство</a></p></td>
<td><p>Представляет характеристику динамического объекта ADO, определяемый поставщиком.</p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Запись</a></p></td>
<td><p>Представляет строку <strong>записей</strong>каталогов или файлов в файловой системе.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Набор записей</a></p></td>
<td><p>Представляет полного набора записей из базовой таблицы или результаты выполнения команды. В любое время в объект <strong>набора записей</strong> называется только одной записи в наборе текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p>Представляет двоичный поток данных.</p></td>
</tr>
</tbody>
</table>

<br/>

