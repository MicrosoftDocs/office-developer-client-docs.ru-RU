---
title: Макрокоманда CancelEvent
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b55fc51f70bcc2c9d2f7e93cf9c79228cd2fe440
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296635"
---
# <a name="cancelevent-macro-action"></a>Макрокоманда CancelEvent

**Область применения**: Access 2013, Office 2013

Действие **CancelEvent** можно использовать для отмены события, из-за чего Access запускал макрос, содержащий это действие. Имя макроса — это параметр свойства события, например **BeforeUpdate,** **OnOpen,** **OnUnload** или **OnPrint.**

## <a name="setting"></a>Параметр

Действие **CancelEvent** не имеет аргументов.

## <a name="remarks"></a>Примечания

В форме обычно используется действие **CancelEvent** в макрос проверки с свойством **событий BeforeUpdate.** Когда пользователь вводит данные в управление или запись, Access запускает макрос перед добавлением данных в базу данных. Если данные не справят условия проверки в макрос, действие **CancelEvent** отменяет процесс обновления перед его началом.

Часто вы используете это действие с действием **MessageBox,** чтобы указать, что данные не удалось с условиями проверки, и предоставить полезную информацию о том, какие данные должны быть введены.

Следующие события могут быть отменены **действием CancelEvent.**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Dirty</strong></p></td>
<td><p><strong>MouseDown</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeDelConfirm</strong></p></td>
<td><p><strong>Exit</strong></p></td>
<td><p><strong>NoData</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>BeforeInsert</strong></p></td>
<td><p><strong>Filter</strong></p></td>
<td><p><strong>Open</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeUpdate</strong></p></td>
<td><p><strong>Format</strong></p></td>
<td><p><strong>Print</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>DblClick</strong></p></td>
<td><p><strong>KeyPress</strong></p></td>
<td><p><strong>Unload</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Delete</strong></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Вы можете использовать **действие CancelEvent** с событием **MouseDown** только для отмены события, которое происходит при правой кнопке мыши объекта.

Если параметр свойства **событий OnDblClick** управления указывает макрос, содержащий действие **CancelEvent,** действие отменяет **событие DblClick.**

Для событий, которые можно отменить, поведение по умолчанию для события (то есть то, что access обычно делает при событии) возникает после того, как выполняется макрос для события. Это позволяет отменить поведение по умолчанию. Например, если дважды щелкнуть слово, на которое включена точка вставки в текстовом окне, Access обычно выбирает слово. Вы можете отменить это поведение по умолчанию в макрос для **события DblClick** и выполнить некоторые другие действия, например открытие формы, содержащей сведения о данных в текстовом окне. Для событий, которые нельзя отменить, поведение по умолчанию происходит перед запуском макроса.

> [!NOTE]
> Если свойство события **OnUnload** формы указывает макрос, который выполняет действие **CancelEvent,** вы не сможете закрыть форму. Необходимо либо исправить условие, из-за чего было выполнено действие **CancelEvent,** либо открыть макрос и удалить **действие CancelEvent.** Если форма является модальной формой, вы не сможете открыть макрос.

Чтобы выполнить действие **CancelEvent** в модуле Visual Basic для приложений (VBA), используйте метод **CancelEvent** объекта **DoCmd.**

## <a name="example"></a>Пример

Проверка данных с помощью макроса

Следующий макрос проверки проверяет почтовые коды, вступив в форму Поставщики. В нем показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.** Условное выражение проверяет страну/регион и почтовый код, вписаный в запись в форме. Если почтовый код не находится в нужном формате для страны или региона, макрос отображает окно сообщений и отменяет сохранение записи. Затем возвращается управление почтовым кодом, где можно исправить ошибку. Этот макрос должен быть присоединен к свойству **BeforeUpdate** формы Поставщики.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Условие</p></th>
<th><p>Макрокоманда</p></th>
<th><p>Аргументы: параметр</p></th>
<th><p>Примечание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IsNull([CountryRegion])</p></td>
<td><p>StopMacro</p></td>
<td><p></p></td>
<td><p>Если CountryRegion <strong>является Null,</strong>почтовый код не может быть проверен.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] В ( &quot; &quot; Франция, &quot; &quot; Италия, &quot; Испания &quot; ) и Len ([Почтовый код]) &lt; &gt; 5</p></td>
<td><p>MessageBox</p></td>
<td><p>Сообщение. Почтовый код должен быть 5 символов. Звуковой сигнал: <strong>Да</strong> тип: <strong>название</strong> информации: ошибка почтового кода</p></td>
<td><p>Если почтовый код не имеет 5 символов, отобразить сообщение.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>ОтменитьСобытие</p></td>
<td><p></p></td>
<td><p>Отмена события.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Имя управления: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] В ( &quot; Австралия , Сингапур ) и &quot; &quot; &quot; Len ([Почтовый код]) &lt; &gt; 4</p></td>
<td><p>MessageBox</p></td>
<td><p>Сообщение. Почтовый код должен быть 4 символа. Звуковой сигнал: <strong>Да</strong> тип: <strong>название</strong> информации: ошибка почтового кода</p></td>
<td><p>Если почтовый код не 4 символа, отобразить сообщение.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p>ОтменитьСобытие</p></td>
<td><p></p></td>
<td><p>Отмена события.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Имя управления: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Канада ) и &quot; ([Почтовый код] Не нравится &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p>MessageBox</p></td>
<td><p>Сообщение. Почтовый код не является допустимым. Пример канадского кода: звуковой сигнал H1J 1C3: <strong>Да</strong> <strong>тип:</strong> название информации: ошибка почтового кода</p></td>
<td><p>Если почтовый код не является правильным для Канады, отобразить сообщение. (Пример канадского кода: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>ОтменитьСобытие</p></td>
<td><p></p></td>
<td><p>Отмена события.</p></td>
</tr>
</tbody>
</table>

