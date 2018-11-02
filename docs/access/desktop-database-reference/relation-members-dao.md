---
title: Члены отношения (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d4b1b1a3a06d0605793667f8c9258ea5b6336f5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923730"
---
# <a name="relation-members-dao"></a>Члены отношения (DAO)


**Применимо к**: Access 2013, Office 2013

Объект связи представляет связь между полями в таблицах и запросах (Microsoft Access базами данных, ядро только).

## <a name="methods"></a>Методы

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="field-object-dao.md">поля</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="relation-attributes-property-dao.md">Атрибуты</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, один или несколько характеристик объект <strong>связи</strong> . Чтение и запись <strong>времени</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-fields-property-dao.md">Поля</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-foreigntable-property-dao.md">Таблицавнешнегоключа</a></strong></p></td>
<td><p>Возвращает или задает имя таблицы внешнего в отношении (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию. Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-partialreplica-property-dao.md">Значений этих</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, следует ли этого отношения учитывать при заполнении реплику из полной реплики объекта <strong>связи</strong> . (База данных ядра базы данных Microsoft Access только). Для чтения и записи, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-table-property-dao.md">В таблице</a></strong></p></td>
<td><p>Указывает имя таблицы основной объект <strong><a href="relation-object-dao.md">связи</a></strong> . Это должен быть равен <strong><a href="connection-name-property-dao.md">свойства Name объекта <strong><a href="tabledef-object-dao.md">TableDef</a></strong> или <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (только для рабочих областей Microsoft Access)</a></strong> .</p></td>
</tr>
</tbody>
</table>

