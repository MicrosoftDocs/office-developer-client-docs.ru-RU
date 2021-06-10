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


Вы можете использовать **действие RemoveAllTempVars** для удаления временных переменных, созданных с помощью **действия SetTempVar.**

## <a name="setting"></a>Параметр

Действие **RemoveAllTempVars** не имеет аргументов.

## <a name="remarks"></a>Примечания

  - Одновременно можно определить до 255 временных переменных. Если не удалить временную переменную, она останется в памяти до закрытия базы данных или проекта. Это хорошая практика, чтобы удалить временные переменные, когда вы закончите с их использованием.

  - При закрытии базы данных или проекта доступ автоматически удаляет все временные переменные.

  - Чтобы удалить одну временную переменную, используйте **действие RemoveTempVar** и установите его аргумент в имя временной переменной, которая необходимо удалить.

  - Чтобы выполнить **действие RemoveAllTempVars** в модуле VBA, используйте метод **RemoveAll** объекта **TempVars.**

## <a name="example"></a>Пример

На следующем макросе показано, как создать временную переменную, использовать ее в состоянии и поле сообщений, а затем удалить временную переменную с помощью действия **RemoveAllTempVars.**

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
<td><p><strong>SetTempVar</strong></p></td>
<td><p><strong>Имя:</strong>Выражение<strong>MyVar:</strong>InputBox &quot; (Введите номер без нуля. &quot; )</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]! [MyVar] &lt; &gt; 0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: = &quot; Вы &quot; &amp; ввели [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Звуковой сигнал:</strong> <strong>YesType</strong>: <strong>Информация</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveAllTempVars</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

