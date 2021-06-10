---
title: Участники индекса (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291798"
---
# <a name="index-members-dao"></a>Участники индекса (DAO)


**Область применения**: Access 2013, Office 2013

Объекты index указывают порядок записей, доступных из таблиц баз данных, и принимаются ли дублирующиеся записи, обеспечивая эффективный доступ к данным. Для внешних баз данных объекты Index описывают индексы, установленные для внешних таблиц (только для рабочей области Microsoft Access).

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
<td><p><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="field-object-dao.md">Field</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создает новый объект Свойства, определенный <strong><a href="property-object-dao.md">пользователем</a></strong> (только рабочие пространства Microsoft Access).</p></td>
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
<td><p><strong><a href="index-clustered-property-dao.md">Кластеризация</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, представляет ли объект <strong>Index</strong> кластерный индекс для таблицы (только в рабочей области Microsoft Access). Для чтения и записи, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></p></td>
<td><p>Возвращает значение, которое указывает количество уникальных значений для объекта <strong><a href="index-object-dao.md">Index,</a></strong> включенных в связанную таблицу (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта. Для чтения и записи.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></p></td>
<td><p>Возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">Index</a></strong> иностранный ключ в таблице (только в рабочей области Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, имеют ли записи с значениями Null в своих полях индексов записи индексов (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Строка <strong>read/write,</strong> если объект не был придан коллекции. Строка <strong>только для</strong> чтения, если объект был придан коллекции.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-primary-property-dao.md">Основной</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">Index</a></strong> основной индекс ключа для таблицы (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-required-property-dao.md">Обязательно</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли <strong><a href="field-object-dao.md">объекту Field</a></strong> значение non-Null.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-unique-property-dao.md">Уникальный</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">Index</a></strong> уникальный (ключевой) индекс для таблицы (только в рабочей области Microsoft Access).</p></td>
</tr>
</tbody>
</table>

