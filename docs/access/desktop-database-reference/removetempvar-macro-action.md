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



Вы можете использовать действие **Макрокоманда removetempvar** для удаления одной временной переменной, созданной с помощью действия **Макрокоманда SetTempVar** .

## <a name="setting"></a>Параметр

Действие **Макрокоманда removetempvar** имеет следующий аргумент.

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
<td><p>Введите имя временной переменной, которую необходимо удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

  - Одновременно может быть определено до 255 временных переменных. Если не удалить временную переменную, она останется в памяти до тех пор, пока не будет закрыта база данных. Рекомендуется удалять временные переменные после завершения их использования.

  - Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.

  - Если вы неправильно задаете имя удаляемой переменной, Access не отобразит сообщение об ошибке. Переменная, которую вы хотите удалить, остается в памяти до закрытия базы данных.

  - Если вы создали более одной временной переменной и хотите удалить их все сразу, используйте действие **Макрокоманда removealltempvars** .

  - Чтобы выполнить действие **Макрокоманда removetempvar** в модуле VBA, используйте метод **Remove** объекта **TempVars** .

## <a name="example"></a>Пример

В следующем макросе показано, как создать временную переменную, использовать ее в условии и окне сообщения, а затем удалить временную переменную с помощью действия **Макрокоманда removetempvar** .

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Условие</p></th>
<th><p>Action</p></th>
<th><p>Аргументы</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Макрокоманда SetTempVar</strong></p></td>
<td><p><strong>Name</strong>:<strong>выражение</strong>мивар: InputBox (&quot;введите ненулевое значение).&quot;</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]! [Мивар] &lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: =&quot;вы ввели &quot; &amp; [TempVars]! [Мивар] &amp; &quot;. &quot; <strong>Гудок</strong>: <strong>естипе</strong>: <strong>Information</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Макрокоманда removetempvar</strong></p></td>
<td><p><strong>Name</strong>: мивар</p></td>
</tr>
</tbody>
</table>

