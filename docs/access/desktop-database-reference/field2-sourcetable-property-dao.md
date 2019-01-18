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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717946"
---
# <a name="field2sourcetable-property-dao"></a>Свойство Field2.SourceTable (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта **поле2** . Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Таблица

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Для объекта **поле2** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , добавляется объект **поле2** , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, добавляемый в конец</p></th>
<th><p>Применение</p></th>
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


Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поле2** . Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.


> [!NOTE]
> Свойство **Таблица** не возвращает имя удобной для восприятия таблицы при использовании объекта **поле2** в коллекции **полей** объекта **набора записей** в таблице тип.


