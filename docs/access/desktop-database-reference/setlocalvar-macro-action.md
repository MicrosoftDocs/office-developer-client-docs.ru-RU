---
title: SetLocalVar Macro Action
TOCTitle: SetLocalVar Macro Action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fb2b3aabb4736c0deee57dafb36e32730fb95f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483266"
---
# <a name="setlocalvar-macro-action"></a>SetLocalVar Macro Action


**Применимо к**: Access 2013 | Office 2013

**ЗадатьЛокПеременную** создает временную переменную и присвойте ей значение определенного значения.

## <a name="setting"></a>Параметр

**ЗадатьЛокПеременную** имеет следующие аргументы.

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
<td><p><strong>Name</strong></p></td>
<td><p>Да</p></td>
<td><p>Строка, задающая имя переменной.</p></td>
</tr>
<tr class="even">
<td><p><strong>Выражение</strong></p></td>
<td><p>Да</p></td>
<td><p>Выражение, которое будет использоваться для задания значения для этой временной переменной. Перед выражением знак равенства (=). Можно нажмите кнопку <strong>Построить</strong> для задания аргумента с помощью <strong>Построителя выражений</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Переменные, созданные **ЗадатьЛокПеременную** можно использовать только в макросе, в котором они определены. Действие **[SetTempVar](settempvar-macro-action.md)** используется для определения переменной, которая может использоваться в другого макроса в процедуре события или на форму или отчет.

После создания временную переменную в выражении можно обратиться к нему. Например при создании временную переменную с именем TotalAmount можно использовать переменной как источник элемента управления для текстовое поле, используя следующий синтаксис.

`=[LocalVars]![TotalAmount]`


> [!NOTE]
> <P>Макрос данных не нужно использовать коллекцию LocalVars для ссылки на переменную. К примеру при создании временную переменную в макросе данных с именем TotalAmount можно использовать переменной как источник элемента управления для текстового поля, используя следующий синтаксис<BR>= [TotalAmount]</P>


