---
title: Макрокоманда RemoveTempVar
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5051cfd74f2a745ee430f2ed8a20445d2f9965f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306757"
---
# <a name="removetempvar-macro-action"></a>Макрокоманда RemoveTempVar


**Область применения**: Access 2013, Office 2013



С помощью действия **RemoveTempVar можно** удалить одну временную переменную, созданную с помощью действия **SetTempVar.**

## <a name="setting"></a>Setting

Действие **RemoveTempVar** имеет следующий аргумент.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Name</strong></p></td>
<td><p>Введите имя временной переменной, которая будет удаляться.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

  - Одновременно можно определить до 255 временных переменных. Если не удалить временную переменную, она останется в памяти до закрытия базы данных. По завершению использования временных переменных лучше удалить.

  - Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.

  - Если вы опечатка имени удаляемой переменной, Access не отображает ошибку. Удаляемая переменная останется в памяти до закрытия базы данных.

  - Если вы создали несколько временных переменных и хотите удалить их все одновременно, используйте действие **RemoveAllTempVars.**

  - Чтобы запустить действие **RemoveTempVar** в модуле VBA, используйте метод **Remove** объекта **TempVars.**

## <a name="example"></a>Пример

Следующий макрос демонстрирует, как создать временную переменную, использовать ее в условии и в окне сообщения, а затем удалить временную переменную с помощью действия **RemoveTempVar.**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Action</p></th>
<th><p>Аргументы</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>SetTempVar</strong></p></td>
<td><p><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox( &quot; Enter a non-zero number. &quot; )</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]! [MyVar] &lt; &gt; 0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: = &quot; You entered &quot; &amp; [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Name</strong>: MyVar</p></td>
</tr>
</tbody>
</table>

