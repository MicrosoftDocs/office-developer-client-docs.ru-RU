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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705233"
---
# <a name="settempvar-macro-action"></a>Макрокоманда SetTempVar


**Применимо к**: Access 2013, Office 2013



Чтобы создать временную переменную и присвойте ей значение определенного значения можно использовать действие **SetTempVar** . Переменная затем использовать как условие или аргумент в последующие действия или в другой макрос, в процедуре события или на форму или отчет можно использовать переменную.

## <a name="setting"></a>Setting

Действие **SetTempVar** состоит из следующих аргументов.

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
<td><p>Введите имя временную переменную.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Введите выражение, которое будет использоваться для задания значения для этой временной переменной. Перед выражением равенства (<strong>=</strong>) входа. Можно нажать кнопку <strong>построения</strong> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> Чтобы использовать построитель выражений для задания аргумента.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

- Может быть длиной до 255 временные переменные, определенные за один раз. Если вы не удалите временную переменную, остается в памяти до закрытия базы данных. Рекомендуется удалить временные переменные после завершения их использования. Чтобы удалить одного временную переменную, используйте действие **[RemoveTempVar](removetempvar-macro-action.md)** и установите аргумента имя временную переменную, которую требуется удалить. Если у вас есть несколько временную переменную, требуется одновременное удаление используйте действие **RemoveAllTempVars** .

- Временные переменные являются глобальными. После создания временную переменную можно обратиться к нему в процедуре события Visual Basic для приложений (VBA) модуля, запроса или выражение. Например при создании временную переменную с именем *MyVar*можно использовать переменной как источник элемента управления для текстовое поле, используя следующий синтаксис:
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > Макросы, запросов и процедур обработки событий перед выражением знак равенства не требуется.
 
  Можно найти временные переменные в любой надстроек или указанной базы данных.

- Чтобы выполнить действие **SetTempVar** в модуле VBA, используйте метод **Add** объекта **в TempVar** .

## <a name="example"></a>Пример

Следующий макрос показано, как создать временную переменную, используя действие **SetTempVar** , а затем временную переменную в окно сообщения и условия и затем удаление временную переменную.

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

