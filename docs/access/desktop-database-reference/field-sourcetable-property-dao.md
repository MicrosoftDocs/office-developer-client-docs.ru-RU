---
title: Свойство Field.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a557a4941f5b4aa511489c5d057871df5fa72c08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292988"
---
# <a name="fieldsourcetable-property-dao"></a>Свойство Field.SourceTable (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для **объекта Field.** Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение .* SourceTable

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Для объекта **Field** использование свойств **SourceField** и **SourceTable** зависит от объекта, который содержит коллекцию **Fields,** к которую применит объект **Field,** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, к</p></th>
<th><p>Использование</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Индекс</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
</tbody>
</table>


Эти свойства указывают исходные имена полей и таблиц, связанных с **объектом Field.** Например, эти свойства можно использовать для определения исходного источника данных в поле запроса, имя которого не связано с именем поля в таблице ниже.


> [!NOTE]
> Свойство **SourceTable** не возвращает понятное имя таблицы, если используется для объекта **Field** в коллекции **Fields** объекта **Recordset таблительного** типа.


