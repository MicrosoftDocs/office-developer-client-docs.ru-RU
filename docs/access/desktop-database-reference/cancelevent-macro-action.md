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

Действие **CancelEvent** можно использовать для отмены события, которое вызвало запуск макроса, содержащего это действие, в Access. Имя макроса — это параметр свойства события, например **BeforeUpdate,** **OnOpen,** **OnUnload** или **OnPrint.**

## <a name="setting"></a>Setting

Действие **CancelEvent** не имеет аргументов.

## <a name="remarks"></a>Заметки

В форме обычно используется действие **CancelEvent** в макросах проверки со свойством события **BeforeUpdate.** Когда пользователь вводит данные в control или запись, Access запускает макрос перед добавлением данных в базу данных. Если данные не удается проверки условий макроса, действие **CancelEvent** отменяет процесс обновления перед его началом.

Часто это действие используется с действием **MessageBox,** чтобы указать, что данные не удалось проверки условий и предоставить полезную информацию о типе данных, которые должны быть введены.

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
<td><p><strong>Фильтр</strong></p></td>
<td><p><strong>Open</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeUpdate</strong></p></td>
<td><p><strong>Формат</strong></p></td>
<td><p><strong>Print</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>DblClick</strong></p></td>
<td><p><strong>KeyPress</strong></p></td>
<td><p><strong>Unload</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>удаление</strong>;</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Действие **CancelEvent** с событием **MouseDown** можно использовать только для отмены события, которое происходит при щелчке правой кнопкой мыши по объекту.

Если параметр свойства события **OnDblClick** для управления указывает макрос, содержащий действие **CancelEvent,** действие отменяет **событие DblClick.**

Для событий, которые можно отменить, поведение по умолчанию для события (то есть, что Access обычно делает при событии) происходит после того, как выполняется макрос для события. Это позволяет отменить поведение по умолчанию. Например, если дважды щелкнуть слово, в которое включена точка вставки в текстовом поле, Access обычно выбирает это слово. Можно отменить это поведение по умолчанию в макросах для события **DblClick** и выполнить какое-либо другое действие, например открытие формы, содержащей сведения о данных в текстовом поле. Для событий, которые не могут быть отменены, поведение по умолчанию происходит перед запуском макроса.

> [!NOTE]
> Если свойство события **OnUnload** формы указывает макрос, который выполняет действие **CancelEvent,** закрыть форму будет нельзя. Необходимо либо исправить условие, из-за чего было выполнено действие **CancelEvent,** либо открыть макрос и удалить действие **CancelEvent.** Если форма является модальной, вы не сможете открыть макрос.

Чтобы выполнить действие **CancelEvent** в модуле Visual Basic для приложений VBA, используйте метод **CancelEvent** объекта **DoCmd.**

## <a name="example"></a>Пример

Проверка данных с помощью макроса

Следующий макрос проверки проверяет почтовые коды, вступив в форму "Поставщики". Здесь показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.** Условное выражение проверяет страну или регион и почтовый код, внося в запись в форме. Если почтовый код не имеет нужного формата для страны или региона, макрос отображает окно сообщения и отменяет сохранение записи. Затем он возвращает вас в почтовый индекс, где можно исправить ошибку. Этот макрос должен быть присоединен к свойству **BeforeUpdate** формы "Поставщики".

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
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
<td><p>Если countryRegion имеет <strong>null,</strong>почтовый код не может быть проверен.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In &quot; &quot; (Франция, &quot; &quot; Италия, &quot; &quot; Испания) и Len([Почтовый индекс]) &lt; &gt; 5</p></td>
<td><p>MessageBox</p></td>
<td><p>Сообщение: почтовый код должен иметь 5 символов. Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</p></td>
<td><p>Если почтовый индекс не имеет 5 символов, отобразить сообщение.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>ОтменитьСобытие</p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Имя управления: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In &quot; &quot; (Australia, &quot; &quot; Singapore) and Len([Postal Code]) &lt; &gt; 4</p></td>
<td><p>MessageBox</p></td>
<td><p>Сообщение: почтовый индекс должен иметь 4 символа. Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</p></td>
<td><p>Если почтовый индекс не имеет 4 символов, отобразить сообщение.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p>ОтменитьСобытие</p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Имя управления: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Канада) и ([Почтовый код] не нравится &quot; &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p>MessageBox</p></td>
<td><p>Сообщение: почтовый индекс не является допустимым. Пример кода для Канады: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</p></td>
<td><p>Если почтовый индекс неправиа для Канады, отобразить сообщение. (Пример кода для Канады: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>ОтменитьСобытие</p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
</tbody>
</table>

