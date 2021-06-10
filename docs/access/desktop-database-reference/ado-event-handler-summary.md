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

Два объекта ADO могут поднимать события: объект [Connection](connection-object-ado.md) и [объект Recordset.](recordset-object-ado.md) Семейство **ConnectionEvent** относится к операциям на объекте **Подключение,** а семейство **RecordsetEvent** относится к операциям на **объекте Recordset.**

- **События подключения.** События выпускаются при начале операции подключения, ее совершении или откате; при [выполнении](command-object-ado.md) команды; когда предупреждение возникает во время операции **события подключения;** или когда **подключение начинается** или заканчивается.

- **События** наборов записей. События выпускаются вокруг асинхронных операций по извлечению, а также при навигации по строкам объекта  **Recordset,** изменении поля в строке **recordset,** изменении строки в recordset, открываем **recordset** с помощью курсора на стороне сервера, закрываем **recordset** или внося какие-либо изменения в **Recordset.**

В следующих таблицах подводятся итоги событий и их описаний.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ConnectionEvent</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete,</a>CommitTransComplete, RollbackTransComplete</p></td>
<td><p><strong>Управление транзакцией</strong> — уведомление о том, что текущая транзакция по подключению запущена, совершена или отката.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect,</a> <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></p></td>
<td><p><strong>Управление подключением</strong> — уведомление о том, что текущее подключение будет запущено, запущено или завершено.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p><strong>Управление выполнением</strong> команд — уведомление о начале или завершении выполнения текущей команды подключения.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>Informational</strong> — уведомление о том, что есть дополнительные сведения о текущей операции.</p></td>
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
<th><p>RecordsetEvent</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p><strong>Состояние ирисовки</strong> — уведомление о ходе операции ирисовки данных или о том, что операция ирисовки завершена. Эти события доступны только в том случае, если <strong>recordset</strong> был открыт с помощью курсора на стороне клиента.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></p></td>
<td><p><strong>Управление изменением поля</strong> — уведомление об изменении или изменении значения текущего поля.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p><strong>Управление навигацией</strong> — уведомление о том, что текущая позиция строки в <strong>наборе записей</strong> будет изменена, изменена или достигла конца <strong>recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></p></td>
<td><p><strong>Управление изменением строк</strong> — уведомление о том, что что-то в текущем ряду <strong>наборов записей</strong> будет изменено или изменено.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></p></td>
<td><p><strong>Управление изменениями в наборе</strong> записей — уведомление о том, что что-то в текущем <strong>наборе записей</strong> изменится или изменилось.</p></td>
</tr>
</tbody>
</table>

