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



Вы можете использовать действие **Макрокоманда SetTempVar** , чтобы создать временную переменную и присвоить ей определенное значение. Переменную можно использовать в качестве условия или аргумента в последующих действиях или можно использовать переменную в другом макросе, в процедуре обработки события или в форме или отчете.

## <a name="setting"></a>Параметр

Макрокоманда **Макрокоманда SetTempVar** имеет следующие аргументы.

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
<td><p>Введите выражение, которое будет использоваться для задания значения для этой временной переменной. Не ставьте перед выражением знак равенства (<strong>=</strong>). Вы можете нажать кнопку <strong>построить</strong> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> Использование построителя выражений для задания этого аргумента.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

- Одновременно может быть определено до 255 временных переменных. Если не удалить временную переменную, она останется в памяти до тех пор, пока не будет закрыта база данных. Рекомендуется удалять временные переменные после завершения их использования. Чтобы удалить одну временную переменную, используйте действие **[Макрокоманда removetempvar](removetempvar-macro-action.md)** и задайте для аргумента имя временной переменной, которую необходимо удалить. Если у вас есть несколько временных переменных и вы хотите удалить их все сразу, используйте действие **Макрокоманда removealltempvars** .

- Временные переменные являются глобальными. После создания временной переменной можно ссылаться на нее в процедуре обработки события, модуле Visual Basic для приложений (VBA), запросе или выражении. Например, если вы создали временную переменную с именем *мивар*, вы можете использовать переменную в качестве источника элемента управления для текстового поля, используя следующий синтаксис:
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > В макросах, запросах и процедурах обработки событий перед выражением не должно быть знака равенства.
 
  Вы также можете ссылаться на временные переменные в любых надстройках или базах данных, на которые имеются ссылки.

- Чтобы выполнить действие **Макрокоманда SetTempVar** в модуле VBA, используйте метод **Add** объекта **TempVars** .

## <a name="example"></a>Пример

В следующем макросе показано, как создать временную переменную с помощью действия **Макрокоманда SetTempVar** , а затем с помощью временной переменной в условии и окне сообщения, а затем удалить временную переменную.

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

