---
title: Свойство Index.Required (DAO)
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
# <a name="indexrequired-property-dao"></a>Свойство Index.Required (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, требуется ли **[объекту Field](field-object-dao.md)** значение non-Null.

## <a name="syntax"></a>Синтаксис

*выражения* . Обязательно

*выражение* Переменная, представляюная объект **Index.**

## <a name="remarks"></a>Примечания

> [!NOTE]
> Если вы можете установить это свойство для объекта **Index** или объекта **Field,** установите его для **объекта Field.** Достоверность параметра свойства объекта **Field** проверяется до проверки объекта **Index.**

Доступность **требуемого** свойства зависит от объекта, который содержит коллекцию [Полей,](fields-collection-dao.md) как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит</p></th>
<th><p>Затем требуется</p></th>
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

