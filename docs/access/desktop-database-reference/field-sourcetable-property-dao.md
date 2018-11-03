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
ms.openlocfilehash: 1236b606f81533922844026d87644b7724e68977
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937570"
---
# <a name="fieldsourcetable-property-dao"></a>Свойство Field.SourceTable (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта **поля** . Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Таблица

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Примечания

Для объекта **поля** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , используется в качестве объекта **поля** "Кому", как показано в следующей таблице.

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
<td><p><strong>Индекс</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><strong>Набор записей</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Связь</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
</tbody>
</table>


Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поля** . Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.


> [!NOTE]
> Свойство **Таблица** не возвращает имя удобной для восприятия таблицы при использовании объекта **поля** в коллекции **полей** объекта **набора записей** в таблице тип.


