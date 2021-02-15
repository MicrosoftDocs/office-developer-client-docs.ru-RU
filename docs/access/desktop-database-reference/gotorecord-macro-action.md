---
title: Макрокоманда GoToRecord
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292141"
---
# <a name="gotorecord-macro-action"></a>Макрокоманда GoToRecord


**Область применения**: Access 2013, Office 2013

С помощью действия **GoToRecord** можно сделать указанную запись текущей записью в открытой таблице, форме или наборе результатов запроса.

## <a name="setting"></a>Setting

Действие **GoToRecord** имеет следующие аргументы.

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
<td><p><strong>Object Type</strong></p></td>
<td><p>Тип объекта, который содержит запись, которую необходимо сделать текущей. Щелкните <strong></strong> <strong>"Таблица",</strong> <strong>"Запрос",</strong>"Форма", <strong></strong> <strong></strong>"Представление сервера", <strong></strong>"Хранимая процедура" или <strong>"Функция"</strong> в поле "Тип объекта" в разделе "Аргументы действий" области построитель макроса. <strong></strong> Оставьте этот аргумент пустым, чтобы выбрать активный объект.</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя объекта, который содержит запись, которую вы хотите сделать текущей записью. В <strong>поле "Имя объекта"</strong> показаны все объекты в текущей базе данных типа, выбранного <strong>аргументом "Тип объекта".</strong> Если оставить аргумент <strong>Object Type</strong> пустым, также оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Запись, которая делает текущую запись. Нажмите <strong>кнопку</strong>"Предыдущая", <strong>"Далее", "Первая",</strong>"Последняя", <strong>"Перейти к"</strong>или <strong>"Новая"</strong> в поле <strong>"Запись".</strong> <strong></strong> <strong></strong> Значение по умолчанию — <strong>Next</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>Или выражение, которое оценивается в качестве этого. Перед выражением должен быть знак "равно" ( <strong>=</strong> ). Этот аргумент указывает запись, которая будет делать текущую запись. Аргумент <strong>Offset</strong> можно использовать двумя способами:</p>
<ul>
<li><p>Если аргумент <strong>Record</strong> имеет <strong></strong>следующий или предыдущий Microsoft Office Access 2007 перемещает число записей вперед или назад, указанное в <strong></strong> <strong>аргументе Offset.</strong></p></li>
<li><p>Если аргумент <strong>Record</strong> — <strong>Go To,</strong>Access перемещается к записи с числом, равным <strong>аргументу Offset.</strong> Номер записи отображается в поле номера записи в нижней части окна.</p>
<p><strong>ПРИМЕЧАНИЕ.</strong>Если вы используете <strong>первый,</strong> <strong>последний</strong>или новый параметр для аргумента <strong>Record,</strong> Access игнорирует аргумент <strong>Offset.</strong> <strong></strong> Если ввести слишком большой аргумент <strong>Offset,</strong> Access отобразит сообщение об ошибке. Нельзя ввести отрицательные числа для аргумента <strong>Offset.</strong></p></li>
<li><p>Если аргумент <strong>Record</strong> имеет <strong></strong>следующий или предыдущий Microsoft Office Access 2007 перемещает число записей вперед или назад, указанное в <strong></strong> <strong>аргументе Offset.</strong></p></li>
<li><p>Если аргумент <strong>Record</strong> — <strong>Go To,</strong>Access перемещается к записи с числом, равным <strong>аргументу Offset.</strong> Номер записи отображается в поле номера записи в нижней части окна.</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Если фокус находится в определенном контрольном уровне в записи, это действие оставляет его в том же контроле для новой записи.

Вы можете использовать **новый** параметр для аргумента **Record,** чтобы перейти к пустой записи в конце формы или таблицы, чтобы ввести новые данные.

Это действие аналогично нажатию  стрелки под кнопкой "Найти" на вкладке **"Главная"** и нажатию кнопки **"Перейти".** Подкоманда "Первая", "Последняя", "Далее", "Предыдущая" и "Новая запись" команды **"Перейти** к" имеют то же влияние на выбранный объект, что и параметры **First,** **Last,** **Next** , **Previous** и    **New** для аргумента **Record.** Вы также можете перейти к записям с помощью кнопок навигации в нижней части окна.

С помощью действия **GoToRecord** можно сделать запись в скрытой форме текущей записью, если указана скрытая форма в аргументах **Object Type** и **Object Name.**

Чтобы запустить действие **GoToRecord** в модуле Visual Basic для приложений (VBA), используйте метод **GoToRecord** объекта **DoCmd.**

