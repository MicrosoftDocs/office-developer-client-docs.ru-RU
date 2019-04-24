---
title: Элементы индекса (DAO)
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
# <a name="index-members-dao"></a>Элементы индекса (DAO)


**Область применения**: Access 2013, Office 2013

Объект index указывает порядок записей, доступ к которым осуществляется из таблиц базы данных, а также сведения о том, принимаются ли повторяющиеся записи, что обеспечивает эффективный доступ к данным. Для внешних баз данных объекты index описывают индексы, установленные для внешних таблиц (только для рабочих областей Microsoft Access).

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
<td><p>Создает новый объект <strong><a href="field-object-dao.md">field</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создает новый объект определяемого пользователем <strong><a href="property-object-dao.md">Свойства</a></strong> (только для рабочих областей Microsoft Access).</p></td>
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
<td><p><strong><a href="index-clustered-property-dao.md">Сгруппирован</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, представляет ли объект <strong>index</strong> кластеризованный индекс для таблицы (только для рабочих областей Microsoft Access). Для чтения и записи, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">Дистинкткаунт</a></strong></p></td>
<td><p>Возвращает значение, которое указывает количество уникальных значений для объекта <strong><a href="index-object-dao.md">index</a></strong> , включенных в связанную таблицу (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта. Для чтения и записи.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Правительства</a></strong></p></td>
<td><p>Возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">index</a></strong> внешний ключ в таблице (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-ignorenulls-property-dao.md">Игноренуллс</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, имеют ли записи индекса значения NULL в полях индекса (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. <strong>Строка</strong> для чтения и записи, если объект не был добавлен в коллекцию. <strong>Строка</strong> , доступная только для чтения, если объект добавлен в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-primary-property-dao.md">Primary</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> первичный индекс ключа для таблицы (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-required-property-dao.md">Обязательно</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли для объекта <strong><a href="field-object-dao.md">field</a></strong> значение, отличное от NULL.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-unique-property-dao.md">Уникальные</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> уникальный (ключ) индекс для таблицы (только для рабочих областей Microsoft Access).</p></td>
</tr>
</tbody>
</table>

