---
title: ADO Event Handler Summary
TOCTitle: ADO Event Handler Summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9042bdbf3271f5aed65f44d8c7f76f1dcbee1d9c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481413"
---
# <a name="ado-event-handler-summary"></a>ADO Event Handler Summary


**Применимо к**: Access 2013 | Office 2013

Два объекта ADO могут вызывать события: объект [подключения](connection-object-ado.md) и объекта [набора записей](recordset-object-ado.md) . Семейство **ConnectionEvent** относится к операции на объект **подключения** , а семейства **RecordsetEvent** относится к операции в объекте **набора записей** .

  - **Подключение событий**: события выдается, когда начинается транзакций для подключения, прилагает все усилия или откат; При выполнении [команды](command-object-ado.md) ; При появлении предупреждения во время операции **Подключения событий** ; или при запуске или завершает **подключение** .

  - **Набор записей событий**: события выдается вокруг операции асинхронной выборки, а также при переходе по строкам объекта **набора записей** , изменение поля в строке из **набора записей**, измените строку в **набор записей**, откройте ** Набор записей** с курсором на сервере, закройте **записей**или внести какие-либо изменения никакой в **набора записей**.

В следующей таблице перечислены события и их описание.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ConnectionEvent</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</p></td>
<td><p><strong>Управление транзакциями</strong> , уведомления о запуске текущей операции на подключение, фиксации или отката.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, отключите</a></p></td>
<td><p><strong>Управление подключениями</strong> — уведомление, в котором будет запущен процесс текущее подключение, запущена или его завершения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p><strong>Управление командами выполнения</strong> — уведомление, выполнение текущей команды на подключение будет запущен процесс или его завершения.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>Информационное</strong> — уведомления о наличии Дополнительные сведения о текущей операции.</p></td>
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
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p><strong>Состояние извлечения</strong> — уведомления о ходе выполнения операции по извлечению данных или завершения операции извлечения. Эти события доступны только в том случае, если <strong>набор записей</strong> был открыт с помощью клиентского курсора.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField FieldChangeComplete</a></p></td>
<td><p><strong>Управление измените поле</strong> — уведомление, значение текущего поля изменится или была изменена.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p><strong>Управления навигации</strong> — уведомление, изменится текущей позиции строки в <strong>набор записей</strong> , были изменены или достигнут конец <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord RecordChangeComplete</a></p></td>
<td><p><strong>Управление измените строку</strong> — уведомление, что-нибудь в текущей строки <strong>набора записей</strong> изменится или была изменена.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset RecordsetChangeComplete</a></p></td>
<td><p><strong>Управление изменение записей</strong> — уведомление, что-нибудь в текущего <strong>набора записей</strong> изменится или была изменена.</p></td>
</tr>
</tbody>
</table>

