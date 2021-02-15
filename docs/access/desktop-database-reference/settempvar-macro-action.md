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



С помощью действия **SetTempVar можно** создать временную переменную и установить для нее определенное значение. Затем переменную можно использовать в качестве условия или аргумента в последующих действиях, или вы можете использовать переменную в другом макросе, в процедуре события или в форме или отчете.

## <a name="setting"></a>Setting

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
<td><p>Введите выражение, которое будет использоваться для ввода значения для этой временной переменной. Не запишите перед выражением знак "равно" <strong>=</strong> (). Можно нажать кнопку <strong>"Построить"</strong> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> чтобы использовать построитель выражений для этого аргумента.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

- Одновременно можно определить до 255 временных переменных. Если не удалить временную переменную, она останется в памяти до закрытия базы данных. По завершению использования временных переменных мы по-настоящему удаляем их. Чтобы удалить одну временную переменную, используйте действие **[RemoveTempVar](removetempvar-macro-action.md)** и установите в качестве аргумента имя временной переменной, которую необходимо удалить. Если у вас несколько временных переменных и вы хотите удалить их все одновременно, используйте действие **RemoveAllTempVars.**

- Временные переменные являются глобальными. После создания временной переменной можно сослаться на нее в процедуре события, модуле Visual Basic для приложений VBA, запросе или выражении. Например, если вы создали временную переменную с именем *MyVar,* вы можете использовать ее в качестве источника управления для текстового окна, используя следующий синтаксис:
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > В макросах, запросах и процедурах событий нет необходимости предварять выражение равным знаком.
 
  Вы также можете ссылаться на временные переменные в любых надстройки или базах данных, на которые есть ссылки.

- Чтобы запустить действие **SetTempVar** в модуле VBA, используйте метод **Add** объекта **TempVars.**

## <a name="example"></a>Пример

В следующем макросе показано, как создать временную переменную с помощью действия **SetTempVar,** затем использовать временную переменную в условии и в окне сообщения, а затем удалить временную переменную.

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

