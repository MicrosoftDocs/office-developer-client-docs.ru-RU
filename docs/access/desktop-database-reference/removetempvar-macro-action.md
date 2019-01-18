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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716308"
---
# <a name="removetempvar-macro-action"></a>Макрокоманда RemoveTempVar


**Применимо к**: Access 2013, Office 2013



Действие **RemoveTempVar** можно использовать для удаления одного временную переменную, созданный с помощью действия **SetTempVar** .

## <a name="setting"></a>Setting

Действие **RemoveTempVar** использует следующий аргумент.

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
<td><p>Введите имя временную переменную, которые вы хотите удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

  - Может быть длиной до 255 временные переменные, определенные за один раз. Если вы не удалите временную переменную, остается в памяти до закрытия базы данных. Рекомендуется удалить временные переменные после завершения их использования.

  - Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.

  - Если неправильно введено имя переменной удаляемых доступа не отображает ошибку. Переменная, которую вы хотите удалить будет оставаться в памяти до закрытия базы данных.

  - Если были созданы более одного временную переменную, требуется одновременное удаление используйте действие **RemoveAllTempVars** .

  - Чтобы выполнить действие **RemoveTempVar** в модуле VBA, используйте метод **Remove** объекта **в TempVar** .

## <a name="example"></a>Пример

Следующий макрос показано, как создать временную переменную, используйте в окне сообщения и условия и затем удалить временную переменную с помощью действия **RemoveTempVar** .

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
<th><p>Arguments</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>SetTempVar</strong></p></td>
<td><p><strong>Имя</strong>: MyVar<strong>выражение</strong>: InputBox (&quot;введите ненулевое число.&quot;)</p></td>
</tr>
<tr class="even">
<td><p>[В TempVar]! [MyVar] &lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: =&quot;вы ввели &quot; &amp; [в TempVar]! [MyVar] &amp; &quot;. &quot; <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>сведения</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Имя</strong>: MyVar</p></td>
</tr>
</tbody>
</table>

