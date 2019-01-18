---
title: Свойство QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721383"
---
# <a name="querydeftype-property-dao"></a>Свойство QueryDef.Type (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее действующие типа или данных тип объекта. Только для чтения**целое число**.

## <a name="syntax"></a>Синтаксис

*выражение* . Тип

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Для объекта **QueryDef** возможные параметры и возвращаемые значения показаны в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Тип запроса</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbQAction</strong></p></td>
<td><p>Action</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQAppend</strong></p></td>
<td><p>Добавление</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQCompound</strong></p></td>
<td><p>Составные</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQCrosstab</strong></p></td>
<td><p>Перекрестный</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQDDL</strong></p></td>
<td><p>Определение данных</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQDelete</strong></p></td>
<td><p>Delete</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQMakeTable</strong></p></td>
<td><p>Создание таблицы</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQProcedure</strong></p></td>
<td><p>Процедура (только для рабочих областей технология ODBCDirect)</p><p><strong>Примечание</strong>: технология ODBCDirect рабочие области, не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSelect</strong></p></td>
<td><p>Выберите</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSetOperation</strong></p></td>
<td><p>Union</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSPTBulk</strong></p></td>
<td><p>Используется с <strong>dbQSQLPassThrough</strong> для указания запроса, который не возвращает записей (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSQLPassThrough</strong></p></td>
<td><p>К серверу (только для рабочих областей Microsoft Access)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQUpdate</strong></p></td>
<td><p>Update</p></td>
</tr>
</tbody>
</table>


При добавьте новое **[поле](field-object-dao.md)**, **[параметр](parameter-object-dao.md)** или **[свойство](property-object-dao.md)** объекта в коллекцию **[индекса](index-object-dao.md)**, **QueryDef**, **[набора записей](recordset-object-dao.md)** или **[TableDef](tabledef-object-dao.md)** объекта, если основной базы данных не поддерживает возникает ошибка Тип данных, указанный для нового объекта.

