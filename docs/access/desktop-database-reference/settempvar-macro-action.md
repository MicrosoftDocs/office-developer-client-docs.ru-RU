---
title: Макрокоманда SetTempVar
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306525"
---
# <a name="settempvar-macro-action"></a>Макрокоманда SetTempVar


**Область применения**: Access 2013, Office 2013



Действие **SetTempVar** можно использовать для создания временной переменной и ее значения. Затем переменная может использоваться в качестве условия или аргумента в последующих действиях, или вы можете использовать переменную на другом макросе, в процедуре событий или в форме или отчете.

## <a name="setting"></a>Параметр

Действие **SetTempVar** имеет следующие аргументы.

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
<td><p>Введите имя временной переменной.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Введите выражение, которое будет использоваться для заданной временной переменной. Не предшествуй выражению с равным <strong>=</strong> () знаком. Кнопку Сборка можно <strong>нажать</strong> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> чтобы установить этот аргумент с помощью конструктора выражений.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

- Одновременно можно определить до 255 временных переменных. Если не удалить временную переменную, она останется в памяти до закрытия базы данных. Это хорошая практика, чтобы удалить временные переменные, когда вы закончите с их использованием. Чтобы удалить одну временную переменную, используйте действие **[RemoveTempVar](removetempvar-macro-action.md)** и установите его аргумент в имя временной переменной, которую необходимо удалить. Если у вас есть несколько временных переменных и вы хотите удалить их все сразу, используйте **действие RemoveAllTempVars.**

- Временные переменные являются глобальными. После создания временной переменной можно обратиться к ней в процедуре события, модуле Visual Basic для приложений (VBA), запросе или выражении. Например, если вы создали временную переменную с именем *MyVar,* вы можете использовать переменную в качестве источника управления для текстового окна, используя следующий синтаксис:
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > В макросах, запросах и процедурах событий не нужно предшествовать выражению с равным знаком.
 
  Вы также можете ссылаться на временные переменные в любых надстройки или ссылаясь баз данных.

- Чтобы выполнить **действие SetTempVar** в модуле VBA, используйте метод **Add** объекта **TempVars.**

## <a name="example"></a>Пример

На следующем макросе показано, как создать временную переменную с помощью действия **SetTempVar,** затем использовать временную переменную в состоянии и поле сообщений, а затем удалить временную переменную.

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
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Имя:</strong>MyVar</p></td>
</tr>
</tbody>
</table>

