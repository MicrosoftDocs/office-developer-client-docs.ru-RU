---
title: Свойство Field. ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47bd400469bc17ac2b57bb249198f7609d7d0801
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292932"
---
# <a name="fieldvalidationtext-property-dao"></a>Свойство Field. ValidationText (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, определяющее текст сообщения, которое отображает ваше приложение, если значение объекта **Field** не удовлетворяют правилу проверки, задаваемому настройкой параметра **ValidationRule** (только для рабочих областей Microsoft Access). Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*Expression* . ValidationText

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Комментарии

Параметр или возвращаемое значение — это **строка** , указывающая текст, который отображается, если пользователь пытается ввести недопустимое значение для поля. Для объекта, который еще не добавлен в коллекцию, это свойство предназначено для чтения и записи.

Для объекта **field** использование свойства **ValidationText** зависит от объекта, содержащего коллекцию Fields, к которой **[](fields-collection-dao.md)** добавляется объект **field** , как показано в следующей таблице.

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
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>

