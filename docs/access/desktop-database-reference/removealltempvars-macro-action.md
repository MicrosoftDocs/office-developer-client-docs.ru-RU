---
title: Макрокоманда RemoveAllTempVars
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: eade809a6e3982dc0dc4cf94ae382af72e8f454e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705080"
---
# <a name="removealltempvars-macro-action"></a>Макрокоманда RemoveAllTempVars


**Применимо к**: Access 2013, Office 2013


Чтобы удалить все временные переменные, которые созданы с помощью действия **SetTempVar** можно использовать действие **RemoveAllTempVars** .

## <a name="setting"></a>Setting

Действие **RemoveAllTempVars** не имеет каких-либо аргументов.

## <a name="remarks"></a>Замечания

  - Может быть длиной до 255 временные переменные, определенные за один раз. Если вы не удалите временную переменную, остается в памяти до закрытия базы данных или проекта. Рекомендуется удалить временные переменные после завершения их использования.

  - Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.

  - Чтобы удалить одного временную переменную, используйте действие **RemoveTempVar** и установите аргумента имя временную переменную, которые вы хотите удалить.

  - Чтобы выполнить действие **RemoveAllTempVars** в модуле VBA, используйте метод **RemoveAll** объекта **в TempVar** .

## <a name="example"></a>Пример

Следующий макрос показано, как создать временную переменную, используйте в окне сообщения и условия и затем удалить временную переменную с помощью действия **RemoveAllTempVars** .

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
<td><p><strong>RemoveAllTempVars</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

