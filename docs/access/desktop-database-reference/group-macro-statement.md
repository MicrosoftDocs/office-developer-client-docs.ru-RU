---
title: Group Macro Statement
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 189744d228db0dadd3260ce77457daf8724828f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481257"
---
# <a name="group-macro-statement"></a>Group Macro Statement


**Применимо к**: Access 2013 | Office 2013

Оператор **группы** позволяет указать блок действия макроса, который можно развернуть или свернуть.

## <a name="setting"></a>Параметр

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

