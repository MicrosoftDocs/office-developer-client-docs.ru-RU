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

Вы можете использовать макрокоманду **GoToRecord (GoToRecord** ), чтобы сделать указанную запись текущей записью в открытой таблице, форме или наборе результатов запроса.

## <a name="setting"></a>Параметр

Макрокоманда **GoToRecord** имеет следующие аргументы.

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
<td><p>Тип объекта, который содержит запись, которую необходимо сделать текущей. Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>серверное представление</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong> в поле <strong>тип объекта</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов. Чтобы выбрать активный объект, оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя объекта, содержащего запись, которую необходимо сделать текущей. В поле <strong>имя объекта</strong> отображаются все объекты текущей базы данных с типом, выбранным аргументом <strong>тип объекта</strong> . Если оставить аргумент " <strong>тип объекта</strong> " пустым, оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Запись для создания текущей записи. В поле <strong>запись</strong> выберите <strong>предыдущий</strong>, <strong>следующий</strong>, <strong>первый</strong>, <strong>последний</strong> <strong>, или</strong> <strong>Новый</strong> . Значение по умолчанию — <strong>Next (далее</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>Целое число или выражение, которое вычисляется как целое число. Перед выражением должен стоять знак равенства (<strong>=</strong>). Этот аргумент указывает запись для создания текущей записи. Аргумент <strong>СМЕЩ</strong> можно использовать двумя способами:</p>
<ul>
<li><p>Если аргумент <strong>Record</strong> находится в <strong>следующей</strong> или <strong>предыдущей</strong>версии, Microsoft Office Access 2007 перемещает число записей, указанных в аргументе <strong>СМЕЩ</strong> , вперед или назад.</p></li>
<li><p>Когда используется аргумент <strong>Record</strong> , Access перемещается <strong>к записи</strong>с номером, равным значению аргумента <strong>offset</strong> . Номер записи отображается в поле номера записи в нижней части окна.</p>
<p><strong>Note</strong>: Если вы используете <strong>первый</strong>, <strong>последний</strong>или <strong>Новый</strong> параметр в аргументе <strong>Record</strong> , Access игнорирует аргумент <strong>СМЕЩ</strong> . Если ввести слишком большой аргумент <strong>смещения</strong> , Access выведет сообщение об ошибке. Вы не можете вводить отрицательные числа для аргумента <strong>СМЕЩ</strong> .</p></li>
<li><p>Если аргумент <strong>Record</strong> находится в <strong>следующей</strong> или <strong>предыдущей</strong>версии, Microsoft Office Access 2007 перемещает число записей, указанных в аргументе <strong>СМЕЩ</strong> , вперед или назад.</p></li>
<li><p>Когда используется аргумент <strong>Record</strong> , Access перемещается <strong>к записи</strong>с номером, равным значению аргумента <strong>offset</strong> . Номер записи отображается в поле номера записи в нижней части окна.</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если фокус находится в определенном элементе управления в записи, это действие оставляет его в том же элементе управления для новой записи.

Вы можете использовать параметр **New** для аргумента **Record** , чтобы переместиться на пустую запись в конце формы или таблицы, чтобы можно было вводить новые данные.

Это действие аналогично щелчку стрелки под кнопкой **найти** на вкладке **Главная** и нажатием кнопки **Перейти**. В качестве **первого**, **последнего**, **следующего**, **предыдущего**и **нового** параметров для аргумента **Record** в выбранном объекте влияют **первый**, **последний**, **следующий**, **предыдущий**и новый подкоманды **записи** **Go** . Кроме того, можно перейти к записям с помощью кнопок навигации в нижней части окна.

Вы можете использовать макрокоманду **GoToRecord (GoToRecord** ), чтобы сделать запись в скрытой форме текущей записью, если указать скрытую форму в аргументах **тип объекта** и **имя объекта** .

Чтобы выполнить макрокоманду **GoToRecord** в модуле Visual Basic для приложений (VBA), используйте метод **GoToRecord** объекта **DoCmd** .

