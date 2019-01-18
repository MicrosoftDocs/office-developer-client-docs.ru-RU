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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722321"
---
# <a name="setfield-macro-action"></a>Макрокоманда SetField

**Применимо к**: Access 2013, Office 2013

Действие **SetField** используется для присвоения значения поля.

> [!NOTE]
> **SetField** действие доступно только в макросов данных.

## <a name="setting"></a>Setting

Действие **SetField** содержит аргументы, перечисленные в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Name</strong></p></td>
<td><p>Строка, идентифицирующая поле.</p></td>
</tr>
<tr class="even">
<td><p><strong>Value</strong></p></td>
<td><p>Выражение, которое задает значение, задаваемое в поле.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block.md)** или **[ИзменитьЗапись](editrecord-data-block.md)** .

