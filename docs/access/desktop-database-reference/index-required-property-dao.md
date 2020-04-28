---
title: Свойство index. Required (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291701"
---
# <a name="indexrequired-property-dao"></a>Свойство index. Required (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, требуется ли для объекта **[field](field-object-dao.md)** значение, отличное от NULL.

## <a name="syntax"></a>Синтаксис

*Expression* . Обязательно

*Expression (выражение* ) Переменная, представляющая объект **индекса** .

## <a name="remarks"></a>Примечания

> [!NOTE]
> Если вы можете задать это свойство для объекта **индекса** или объекта **field** , задайте для объекта **field** . Срок действия параметра свойства для объекта **field** проверяется до объекта **index** .

Доступность **обязательного** свойства зависит от объекта, содержащего коллекцию [Fields](fields-collection-dao.md) , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к элементу</p></th>
<th><p>Затем необходимо</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>Index</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>Recordset</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>Relation</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>

