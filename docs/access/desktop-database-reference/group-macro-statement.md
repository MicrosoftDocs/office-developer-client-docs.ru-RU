---
title: Оператор макроса Group
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292113"
---
# <a name="group-macro-statement"></a>Оператор макроса Group


**Область применения**: Access 2013, Office 2013

В **заявлении Group** можно указать блок действий в макрос, который можно расширить или свернуть.

## <a name="setting"></a>Параметр

В **действии Group** есть следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Описание</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строка, которая отображается в качестве названия группы при ее обрушении.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

В **заявлении Group** не определяется область макроса, которую можно выполнять отдельно. Используйте заявление **[Submacro](submacro-macro-statement.md)** для определения набора действий, которые будут выполняться отдельно в окне **Macro Designer.**

