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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300947"
---
# <a name="querydeftype-property-dao"></a>Свойство QueryDef.Type (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, указывающее операционный тип или тип данных объекта. Только для **чтения, integer**.

## <a name="syntax"></a>Синтаксис

*выражение* .Type

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

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
<td><p>Append</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQCompound</strong></p></td>
<td><p>Составные</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQCrosstab</strong></p></td>
<td><p>Перекрестная</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQDDL</strong></p></td>
<td><p>Data-definition</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQDelete</strong></p></td>
<td><p>Удаление</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQMakeTable</strong></p></td>
<td><p>Make-table</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQProcedure</strong></p></td>
<td><p>Процедура (только для рабочей области ODBCDirect)</p><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSelect</strong></p></td>
<td><p>Выбор</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSetOperation</strong></p></td>
<td><p>Union</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSPTBulk</strong></p></td>
<td><p>Используется с <strong>dbQSQLPassThrough</strong> для указания запроса, который не возвращает записи (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSQLPassThrough</strong></p></td>
<td><p>Сквозной доступ (только для рабочей области Microsoft Access)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQUpdate</strong></p></td>
<td><p>Update</p></td>
</tr>
</tbody>
</table>


При приложении нового объекта **[Field,](field-object-dao.md)** **[Parameter](parameter-object-dao.md)** или **[Property](property-object-dao.md)** в коллекцию объекта **[Index,](index-object-dao.md)** **QueryDef,** **[Recordset](recordset-object-dao.md)** или **[TableDef](tabledef-object-dao.md)** возникает ошибка, если базовая база данных не поддерживает тип данных, указанный для нового объекта.

