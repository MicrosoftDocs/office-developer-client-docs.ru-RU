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

Вы можете использовать **действие GoToRecord,** чтобы фиксировать текущую запись в наборе результатов открытой таблицы, формы или запроса.

## <a name="setting"></a>Параметр

Действие **GoToRecord имеет** следующие аргументы.

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
<td><p>Тип объекта, который содержит запись, которую необходимо сделать текущим. Щелкните таблицу, <strong></strong> <strong>запрос,</strong> <strong>форму,</strong>представление <strong></strong> <strong>сервера,</strong>сохраненную процедуру <strong></strong> <strong>или</strong>функцию в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> Оставьте этот аргумент пустым, чтобы выбрать активный объект.</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя объекта, который содержит запись, которую необходимо сделать текущей записью. Поле <strong>Имя объекта</strong> отображает все объекты текущей базы данных типа, выбранного <strong>аргументом Object Type.</strong> Если оставить аргумент <strong>Object Type</strong> пустым, оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Запись, чтобы сделать текущую запись. Нажмите <strong>кнопку</strong>Предыдущий , <strong>Далее</strong>, <strong>Первый</strong>, <strong>Последний</strong>, <strong>Перейти к</strong>, или <strong>Новый</strong> в <strong>поле Запись.</strong> По умолчанию <strong>далее</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>Integer или выражение, которое оценивается для integer. Выражению должно предшествовать равный знак ( <strong>=</strong> ). Этот аргумент указывает запись, чтобы сделать текущую запись. Аргумент Offset можно <strong>использовать</strong> двумя способами:</p>
<ul>
<li><p>Когда аргумент <strong>Записи</strong> <strong>следующий</strong> или предыдущий, <strong></strong>Microsoft Office Access 2007 перемещает количество записей вперед или назад, указанное в <strong>аргументе Смещение.</strong></p></li>
<li><p>Когда аргумент <strong>Записи</strong> <strong>перейдите к</strong>записи, доступ перемещается к записи с номером, равным <strong>аргументу Смещение.</strong> Номер записи отображается в поле записи в нижней части окна.</p>
<p><strong>ПРИМЕЧАНИЕ.</strong>Если вы используете <strong>первый,</strong> <strong>последний</strong>или новый параметр для аргумента <strong>Запись,</strong> Access игнорирует аргумент <strong>Смещение.</strong> <strong></strong> Если вы вводите слишком большой аргумент <strong>Смещения,</strong> Access отображает сообщение об ошибке. Для аргумента Смещение нельзя вводить отрицательные <strong>номера.</strong></p></li>
<li><p>Когда аргумент <strong>Записи</strong> <strong>следующий</strong> или предыдущий, <strong></strong>Microsoft Office Access 2007 перемещает количество записей вперед или назад, указанное в <strong>аргументе Смещение.</strong></p></li>
<li><p>Когда аргумент <strong>Записи</strong> <strong>перейдите к</strong>записи, доступ перемещается к записи с номером, равным <strong>аргументу Смещение.</strong> Номер записи отображается в поле записи в нижней части окна.</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если фокус находится в определенном контроле в записи, это действие оставляет его в том же контроле для новой записи.

Вы можете использовать параметр **New** для аргумента **Запись** для перемещения на пустую запись в конце формы или таблицы, чтобы можно было ввести новые данные.

Это действие аналогично нажатию стрелки ниже кнопки **Найти** на вкладке **Главная,** а затем нажать **кнопку Перейти к**. **Первые,** последние, **последующие,**  предыдущие и новые подкомитеты записи команды **Go To** имеют такое же влияние на  выбранный объект, как **первый,** **последний,** **следующий,** предыдущий и новые параметры для аргумента **Запись.**  Вы также можете перейти к записям с помощью кнопок навигации в нижней части окна.

Вы можете использовать **действие GoToRecord** для записи в скрытой форме текущей записи,  если указать скрытую форму в аргументах **Типа** объекта и имени объектов.

Чтобы выполнить **действие GoToRecord** в модуле Visual Basic для приложений (VBA), используйте метод **GoToRecord** объекта **DoCmd.**

