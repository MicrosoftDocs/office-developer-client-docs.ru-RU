---
title: GoToRecord Macro Action
TOCTitle: GoToRecord Macro Action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f7094d95053e97180526523fd41862dfeb100c86
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482375"
---
# <a name="gotorecord-macro-action"></a>GoToRecord Macro Action


**Применимо к**: Access 2013 | Office 2013

Можно использовать действие **НаЗапись** чтобы сделать указанной записи текущей открытой таблицы, формы или набора результатов запроса.

## <a name="setting"></a>Параметр

Действие **НаЗапись** имеет следующие аргументы.

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
<td><p><strong>Тип объекта</strong></p></td>
<td><p>Тип объекта, который содержит запись, которую следует сделать текущей. Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>Представление</strong>, <strong>Хранимую процедуру</strong>или <strong>функцию</strong> в поле <strong>Тип объекта</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов. Оставьте данный аргумент пустым, чтобы выбрать активный объект.</p></td>
</tr>
<tr class="even">
<td><p><strong>Имя объекта</strong></p></td>
<td><p>Имя объекта, содержащую запись, который требуется сделать текущей записи. В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа. Если <strong>Тип объекта</strong> аргумента оставлено пустым, оставьте аргумент пустым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Запись</strong></p></td>
<td><p>Сделать текущей запись. Нажмите кнопку <strong>Назад</strong>, <strong>Далее</strong>, <strong>первый</strong>, <strong>последний</strong>, <strong>Перейдите к</strong>или <strong>Создать</strong> в поле <strong>записи</strong> . Значение по умолчанию — <strong>Далее</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Смещение</strong></p></td>
<td><p>Целое число или выражение, которое оценивается как целое число. Выражение должно предшествовать знак равенства (<strong>=</strong>). Этот аргумент определяет записи, чтобы сделать текущей. Аргумент <strong>смещение</strong> можно использовать двумя способами:</p>
<ul>
<li><p>Если аргумент <strong>запись</strong> <strong>следующий</strong> или <strong>Предыдущий</strong>, Microsoft Office Access 2007 перемещает число записей вперед или назад, указанный в аргументе <strong>смещение</strong> .</p></li>
<li><p>При <strong>записи</strong> аргумент <strong>Перейти к</strong>Access перемещает записи с номером равен <strong>смещение</strong> . Номер записи отображается в поле номер записи в нижней части окна.</p></li>
</ul>

> [!NOTE]
> <P>Если используется параметр <STRONG>первого</STRONG>, <STRONG>последнего</STRONG>или <STRONG>Создать</STRONG> <STRONG>запись</STRONG> аргумента <STRONG>смещение</STRONG> игнорируется. Если аргумент <STRONG>смещение</STRONG> слишком большого размера, Access отображает сообщение об ошибке. Нельзя вводить отрицательные числа для аргумента <STRONG>смещение</STRONG> .</P>


<p></p>
<ul>
<li><p>Если аргумент <strong>запись</strong> <strong>следующий</strong> или <strong>Предыдущий</strong>, Microsoft Office Access 2007 перемещает число записей вперед или назад, указанный в аргументе <strong>смещение</strong> .</p></li>
<li><p>При <strong>записи</strong> аргумент <strong>Перейти к</strong>Access перемещает записи с номером равен <strong>смещение</strong> . Номер записи отображается в поле номер записи в нижней части окна.</p></li>
</ul></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Если фокус находится в конкретный элемент управления в запись, это действие оставляет его в тот же элемент управления для новой записи.

Параметр **Создать** **запись** для перемещения в пустую запись в конце формы или таблицы, которые можно ввести новые данные.

Это действие аналогично щелкнув стрелку под кнопкой **Найти** на вкладке **Главная** и затем нажав кнопку **Перейти**. **Первый**, **последний**, **Далее**, **Назад**и команд **Новую запись** команды **Перейти к** имеют такой же эффект на выбранный объект, как **первый**, **последний**, **Далее**, **Назад** **Создать** параметры и **запись** . Вы также можете переместить в записи с помощью кнопок перехода в нижней части окна.

Можно использовать **НаЗапись** , чтобы сделать запись в скрытой форме текущей записи при указании скрытые формы в аргументах **Тип** и **Имя объекта** .

Чтобы запустить **НаЗапись** в Visual Basic для приложений (VBA) модуль, используйте метод **НаЗапись** **объекта** .
