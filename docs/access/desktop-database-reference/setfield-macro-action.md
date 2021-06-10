---
title: Макрокоманда SetField
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314618"
---
# <a name="setfield-macro-action"></a>Макрокоманда SetField

**Область применения**: Access 2013, Office 2013

Действие **SetField** можно использовать для назначения значения для поля.

> [!NOTE]
> Действие **SetField** доступно только в макросах данных.

## <a name="setting"></a>Параметр

Действие **SetField** имеет аргументы, перечисленные в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргументация</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Name</strong></p></td>
<td><p>Строка, определяемая полем.</p></td>
</tr>
<tr class="even">
<td><p><strong>Значение</strong></p></td>
<td><p>Выражение, которое указывает значение, которое необходимо назначить поле.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Действие **SetField** нельзя использовать вне блока **[данных CreateRecord](createrecord-data-block.md)** или **[EditRecord.](editrecord-data-block.md)**

