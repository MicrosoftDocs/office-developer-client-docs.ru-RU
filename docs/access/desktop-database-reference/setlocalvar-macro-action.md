---
title: Действия макроса SetLocalVar
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
ms.openlocfilehash: 299227553481c4f149827c31078111db7b427f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886643"
---
# <a name="setlocalvar-macro-action"></a>Действия макроса SetLocalVar


**Применимо к**: Access 2013, Office 2013

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


