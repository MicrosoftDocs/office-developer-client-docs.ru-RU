---
title: Свойство Field. Саурцефиелд (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dabfa13bac6973cea4bd69e0867292c4a6967
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292995"
---
# <a name="fieldsourcefield-property-dao"></a>Свойство Field. Саурцефиелд (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает имя поля, которое является исходным источником данных для объекта **field** . Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*Expression* . Саурцефиелд

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Комментарии

Для объекта **field** использование свойств **саурцефиелд** и **саурцетабле** зависит от объекта, содержащего коллекцию Fields, в которую **** добавляется объект **field** , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, добавленный в</p></th>
<th><p>Использование</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
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


Эти свойства указывают исходное имя поля и таблицы, связанные с объектом **field** . Например, эти свойства можно использовать для определения исходного источника данных в поле запроса с именем, не связанным с именем поля в базовой таблице.

