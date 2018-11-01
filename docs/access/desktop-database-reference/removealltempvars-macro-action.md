---
title: Действия макроса RemoveAllTempVars
TOCTitle: RemoveAllTempVars Macro Action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 49b92f90fb26ea1f7ad5f0878a7479267b35bdaf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870795"
---
# <a name="removealltempvars-macro-action"></a>Действия макроса RemoveAllTempVars


**Применимо к**: Access 2013, Office 2013


Чтобы удалить все временные переменные, которые созданы с помощью действия **SetTempVar** можно использовать действие **RemoveAllTempVars** .

## <a name="setting"></a>Параметр

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
<th><p>Condition</p></th>
<th><p>Действие</p></th>
<th><p>Аргументы</p></th>
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

