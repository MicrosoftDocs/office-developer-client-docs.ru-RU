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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306799"
---
# <a name="removealltempvars-macro-action"></a>Макрокоманда RemoveAllTempVars


**Область применения**: Access 2013, Office 2013


Вы можете использовать действие **Макрокоманда removealltempvars** , чтобы удалить все временные переменные, созданные с помощью действия **Макрокоманда SetTempVar** .

## <a name="setting"></a>Параметр

Действие **Макрокоманда removealltempvars** не имеет аргументов.

## <a name="remarks"></a>Примечания

  - Одновременно может быть определено до 255 временных переменных. Если не удалить временную переменную, она останется в памяти до тех пор, пока не будет закрыта база данных или проект. Рекомендуется удалять временные переменные после завершения их использования.

  - Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.

  - Чтобы удалить одну временную переменную, используйте действие **Макрокоманда removetempvar** и задайте для аргумента имя удаляемой временной переменной.

  - Чтобы выполнить действие **Макрокоманда removealltempvars** в модуле VBA, используйте метод **RemoveAll** объекта **TempVars** .

## <a name="example"></a>Пример

В следующем макросе показано, как создать временную переменную, использовать ее в условии и окне сообщения, а затем удалить временную переменную с помощью действия **Макрокоманда removealltempvars** .

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
<td><p><strong>Макрокоманда removealltempvars</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

