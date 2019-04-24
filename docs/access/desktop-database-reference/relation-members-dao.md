---
title: Элементы отношений (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84e18afe4a11e53d68397efad71ac6136c779143
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307039"
---
# <a name="relation-members-dao"></a>Элементы отношений (DAO)


**Область применения**: Access 2013, Office 2013

Объект relation представляет связь между полями в таблицах или запросах (только базы данных ядра СУБД Microsoft Access).

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
<td><p>Создает новый объект <strong><a href="field-object-dao.md">field</a></strong> (только для рабочих областей Microsoft Access).</p></td>
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
<td><p><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает одну или несколько характеристик объекта <strong>связи</strong> . Для чтения и записи, <strong>Long</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></p></td>
<td><p>Задает или возвращает имя внешней таблицы в отношении (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. <strong>Строка</strong> для чтения и записи, если объект не был добавлен в коллекцию. <strong>Строка</strong> , доступная только для чтения, если объект добавлен в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-partialreplica-property-dao.md">Партиалреплика</a></strong></p></td>
<td><p>Задает или возвращает значение объекта <strong>relation</strong> , указывающее, следует ли учитывать это отношение при заполнении частичной реплики из полной реплики. (Только базы данных ядра СУБД Microsoft Access). Для чтения и записи, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-table-property-dao.md">Приведен</a></strong></p></td>
<td><p>Указывает имя основной таблицы объекта <strong><a href="relation-object-dao.md">связи</a></strong> . Это значение должно совпадать с параметром свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> объекта <strong><a href="tabledef-object-dao.md">tabledef</a></strong> или <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
</tbody>
</table>

