---
title: SetField Macro Action
TOCTitle: SetField Macro Action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7050065ccb42d5e6cc9347f32df056891f4ed078
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482077"
---
# <a name="setfield-macro-action"></a>SetField Macro Action


**Применимо к**: Access 2013 | Office 2013

Действие **SetField** используется для присвоения значения поля.


> [!NOTE]
> <P><STRONG>SetField</STRONG> действие доступно только в макросов данных.</P>



## <a name="setting"></a>Параметр

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
<td><p><strong>Значение</strong></p></td>
<td><p>Выражение, которое задает значение, задаваемое в поле.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block.md)** или **[ИзменитьЗапись](editrecord-data-block.md)** .
