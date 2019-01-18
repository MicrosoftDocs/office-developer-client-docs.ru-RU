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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713998"
---
# <a name="group-macro-statement"></a>Оператор макроса Group


**Применимо к**: Access 2013, Office 2013

Оператор **группы** позволяет указать блок действия макроса, который можно развернуть или свернуть.

## <a name="setting"></a>Setting

Действие **группы** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Описание</strong></p></td>
<td><p>НЕТ</p></td>
<td><p>Строка, которая отображается как заголовок группы, когда она свернута.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Оператор **группы** не определяет область макрос, который может выполняться отдельно. Оператор **[Вложенный макрос](submacro-macro-statement.md)** используется для определения набора действия для выполнения отдельно в окне **Конструктор макросов** .

