---
title: Сводка по обработчикам событий ADO
TOCTitle: ADO event handler summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c37c1257ad3f3cb046f7faf82ffcb93f067b1ff5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283375"
---
# <a name="ado-event-handler-summary"></a>ADO Event Handler Summary


**Область применения**: Access 2013, Office 2013

Два объекта ADO могут вызывать события: объект [Connection](connection-object-ado.md) и объект [Recordset](recordset-object-ado.md) . Семейство **коннектионевент** относится к операциям объекта **Connection** , а семейство **рекордсетевент** относится к операциям объекта **Recordset** .

- **События подключения**: события, выдаваемые при начале транзакции подключения, фиксируются или откатываются; При выполнении [команды](command-object-ado.md) ; При возникновении предупреждения во время операции **подключения** ; или время начала или окончания **подключения** .

- **События Recordset**: события создаются в асинхронных операциях выборки, а также при навигации по строкам объекта **Recordset** , изменении поля в строке объекта Recordset, изменении строки **** в **наборе записей**и открытии ** Объект Recordset** с помощью курсора на стороне сервера, закройте **набор записей**или внесите изменения в **набор записей**.

В приведенных ниже таблицах приводится сводка по событиям и их описаниям.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Коннектионевент</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">События begintranscomplete</a>, CommitTransComplete, RollbackTransComplete</p></td>
<td><p><strong>Управление транзакциями</strong> — уведомление о том, что текущая транзакция подключения была запущена, зафиксирована или отменена.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">Событие willconnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">события connectcomplete, Disconnect</a></p></td>
<td><p><strong>Управление подключением</strong> — уведомление о том, что текущее подключение будет запущено, начато или завершено.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">событие executecomplete</a></p></td>
<td><p><strong>Управление выполнением команд</strong> — уведомление о том, что выполнение текущей команды для подключения будет начато или завершено.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>Информационное</strong> сообщение — уведомление о том, что существует дополнительная информация о текущей операции.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Рекордсетевент</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">Событие fetchprogress</a>, <a href="fetchcomplete-event-ado.md">событие fetchcomplete</a></p></td>
<td><p><strong>Состояние извлечения</strong> — уведомление о ходе выполнения операции извлечения данных или завершении операции извлечения. Эти события доступны только в том случае, если <strong>набор записей</strong> был открыт с помощью курсора на стороне клиента.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">События willchangefield, FieldChangeComplete</a></p></td>
<td><p><strong>Управление изменениями полей</strong> — уведомление о том, что значение текущего поля изменится или изменилось.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">События WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">событие endofrecordset</a></p></td>
<td><p><strong>Управление навигацией</strong> — уведомление о том, что текущая позиция строки в <strong>наборе записей</strong> будет изменена, изменена или достигнут конец <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">События willchangerecord, RecordChangeComplete</a></p></td>
<td><p><strong>Управление изменениями строк</strong> — уведомление о том, что значение в текущей строке <strong>набора записей</strong> изменится или изменилось.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">События willchangerecordset, RecordsetChangeComplete</a></p></td>
<td><p><strong>Управление изменениями в наборе записей</strong> — уведомление о том, что объект в текущем <strong>наборе записей</strong> изменится или изменился.</p></td>
</tr>
</tbody>
</table>

