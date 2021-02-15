---
title: Свойство Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a3ecf8b6655bb9f1dd2b25d264708112834e8a90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292673"
---
# <a name="field2sourcetable-property-dao"></a>Свойство Field2.SourceTable (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для **объекта Field2.** Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение .* SourceTable

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Заметки

Для объекта **Field2** использование свойств **SourceField** и **SourceTable** зависит от объекта, который содержит коллекцию **Fields,** к которую применит объект **Field2,** как показано в следующей таблице.

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


Эти свойства указывают исходные имена полей и таблиц, связанных с **объектом Field2.** Например, эти свойства можно использовать для определения исходного источника данных в поле запроса, имя которого не связано с именем поля в таблице ниже.


> [!NOTE]
> Свойство **SourceTable** не возвращает понятное имя таблицы, если используется для объекта **Field2** в коллекции **Fields** объекта **Recordset таблительного** типа.


