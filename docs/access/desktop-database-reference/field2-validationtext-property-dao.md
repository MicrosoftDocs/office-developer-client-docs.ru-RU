---
title: Свойство Field2.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4d58cb6bd32bd46b0a6bcec40ff68cdc52eebc31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292624"
---
# <a name="field2validationtext-property-dao"></a>Свойство Field2.ValidationText (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает текст сообщения, отображаемого приложением, если значение объекта **Field2** не удовлетворяет правилу проверки, указанному параметром **validationRule** (только в рабочей области Microsoft Access). Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражения* . ValidationText

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

Значение параметра или возврата — **строка,** которая указывает текст, отображаемый при попытках пользователя ввести недействительное значение для поля. Для объекта, который еще не добавлен в коллекцию, это свойство предназначено для чтения и записи.

Для объекта Field2 использование свойства **ValidationText** зависит от объекта, **[](fields-collection-dao.md)** который содержит коллекцию Полей, к которой примыкает объект **Field2,** как показано в следующей таблице. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, приданный</p></th>
<th><p>Usage</p></th>
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

