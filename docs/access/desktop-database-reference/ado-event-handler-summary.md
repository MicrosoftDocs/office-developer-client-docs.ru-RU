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
# <a name="ado-event-handler-summary"></a><span data-ttu-id="f8c5d-102">ADO Event Handler Summary</span><span class="sxs-lookup"><span data-stu-id="f8c5d-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="f8c5d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8c5d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8c5d-104">Два объекта ADO могут вызывают события: [объект Connection](connection-object-ado.md) и [объект Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f8c5d-104">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="f8c5d-105">Семейство **ConnectionEvent** относится к операциям объекта **Connection,** а семейство **RecordsetEvent** относится к операциям объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="f8c5d-105">The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

- <span data-ttu-id="f8c5d-106">**События подключения:** события выдаются, когда транзакция подключения начинается, зафиксирована или отката; при [выполнении](command-object-ado.md) команды; при выявии предупреждения во время операции **connection Event;** или когда **подключение начинается** или заканчивается.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

- <span data-ttu-id="f8c5d-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset,** open a **Recordset** with a server-side cursor, close a **Recordset**, or make any changeever in the **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="f8c5d-108">В следующих таблицах описаны события и их описания.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8c5d-109">ConnectionEvent</span><span class="sxs-lookup"><span data-stu-id="f8c5d-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="f8c5d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f8c5d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8c5d-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete,</a>CommitTransComplete, RollbackTransComplete</span><span class="sxs-lookup"><span data-stu-id="f8c5d-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="f8c5d-112"><strong>Управление транзакцией</strong> — уведомление о том, что текущая транзакция для подключения запущена, зафиксирована или отката.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8c5d-113"><a href="willconnect-event-ado.md">WillConnect,</a> <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span><span class="sxs-lookup"><span data-stu-id="f8c5d-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="f8c5d-114"><strong>Управление подключениями</strong> — уведомление о том, что текущее подключение будет запущено, запущено или завершено.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8c5d-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="f8c5d-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f8c5d-116"><strong>Управление выполнением</strong> команд — уведомление о начале или завершении выполнения текущей команды подключения.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8c5d-117"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="f8c5d-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="f8c5d-118"><strong>Информационный</strong> — уведомление о том, что имеются дополнительные сведения о текущей операции.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
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
<th><p><span data-ttu-id="f8c5d-119">RecordsetEvent</span><span class="sxs-lookup"><span data-stu-id="f8c5d-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="f8c5d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f8c5d-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8c5d-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="f8c5d-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f8c5d-122"><strong>Состояние ирисовки</strong> — уведомление о ходе выполнения операции иудиации данных или о том, что операция ирисовки завершена.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-122"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed.</span></span> <span data-ttu-id="f8c5d-123">Эти события доступны, только если <strong>набор записей</strong> был открыт с помощью курсора на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-123">These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8c5d-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f8c5d-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f8c5d-125"><strong>Управление изменениями полей</strong> — уведомление о том, что значение текущего поля изменится или изменилось.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8c5d-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete,</a> <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="f8c5d-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="f8c5d-127"><strong>Управление навигацией</strong> — уведомление о том, что текущая позиция строки в наборе <strong>записей</strong> изменится, изменилась или достигла конца <strong>recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="f8c5d-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8c5d-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f8c5d-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f8c5d-129"><strong>Управление изменениями строк</strong> — уведомление о том, что что-то в текущей строке наборов <strong>записей</strong> изменится или изменилось.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8c5d-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f8c5d-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f8c5d-131"><strong>Управление изменениями в наборе</strong> записей — уведомление о том, что что-то в текущем наборе <strong>записей</strong> изменится или изменилось.</span><span class="sxs-lookup"><span data-stu-id="f8c5d-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

