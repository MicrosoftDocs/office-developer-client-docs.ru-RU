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
# <a name="ado-event-handler-summary"></a><span data-ttu-id="a87c7-102">ADO Event Handler Summary</span><span class="sxs-lookup"><span data-stu-id="a87c7-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="a87c7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a87c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a87c7-104">Два объекта ADO могут поднимать события: объект [Connection](connection-object-ado.md) и [объект Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="a87c7-104">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="a87c7-105">Семейство **ConnectionEvent** относится к операциям на объекте **Подключение,** а семейство **RecordsetEvent** относится к операциям на **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="a87c7-105">The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

- <span data-ttu-id="a87c7-106">**События подключения.** События выпускаются при начале операции подключения, ее совершении или откате; при [выполнении](command-object-ado.md) команды; когда предупреждение возникает во время операции **события подключения;** или когда **подключение начинается** или заканчивается.</span><span class="sxs-lookup"><span data-stu-id="a87c7-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

- <span data-ttu-id="a87c7-107">**События** наборов записей. События выпускаются вокруг асинхронных операций по извлечению, а также при навигации по строкам объекта  **Recordset,** изменении поля в строке **recordset,** изменении строки в recordset, открываем **recordset** с помощью курсора на стороне сервера, закрываем **recordset** или внося какие-либо изменения в **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="a87c7-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="a87c7-108">В следующих таблицах подводятся итоги событий и их описаний.</span><span class="sxs-lookup"><span data-stu-id="a87c7-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a87c7-109">ConnectionEvent</span><span class="sxs-lookup"><span data-stu-id="a87c7-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="a87c7-110">Description</span><span class="sxs-lookup"><span data-stu-id="a87c7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a87c7-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete,</a>CommitTransComplete, RollbackTransComplete</span><span class="sxs-lookup"><span data-stu-id="a87c7-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="a87c7-112"><strong>Управление транзакцией</strong> — уведомление о том, что текущая транзакция по подключению запущена, совершена или отката.</span><span class="sxs-lookup"><span data-stu-id="a87c7-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a87c7-113"><a href="willconnect-event-ado.md">WillConnect,</a> <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span><span class="sxs-lookup"><span data-stu-id="a87c7-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="a87c7-114"><strong>Управление подключением</strong> — уведомление о том, что текущее подключение будет запущено, запущено или завершено.</span><span class="sxs-lookup"><span data-stu-id="a87c7-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a87c7-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="a87c7-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a87c7-116"><strong>Управление выполнением</strong> команд — уведомление о начале или завершении выполнения текущей команды подключения.</span><span class="sxs-lookup"><span data-stu-id="a87c7-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a87c7-117"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="a87c7-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="a87c7-118"><strong>Informational</strong> — уведомление о том, что есть дополнительные сведения о текущей операции.</span><span class="sxs-lookup"><span data-stu-id="a87c7-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
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
<th><p><span data-ttu-id="a87c7-119">RecordsetEvent</span><span class="sxs-lookup"><span data-stu-id="a87c7-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="a87c7-120">Description</span><span class="sxs-lookup"><span data-stu-id="a87c7-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a87c7-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="a87c7-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a87c7-122"><strong>Состояние ирисовки</strong> — уведомление о ходе операции ирисовки данных или о том, что операция ирисовки завершена.</span><span class="sxs-lookup"><span data-stu-id="a87c7-122"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed.</span></span> <span data-ttu-id="a87c7-123">Эти события доступны только в том случае, если <strong>recordset</strong> был открыт с помощью курсора на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="a87c7-123">These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a87c7-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="a87c7-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a87c7-125"><strong>Управление изменением поля</strong> — уведомление об изменении или изменении значения текущего поля.</span><span class="sxs-lookup"><span data-stu-id="a87c7-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a87c7-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="a87c7-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="a87c7-127"><strong>Управление навигацией</strong> — уведомление о том, что текущая позиция строки в <strong>наборе записей</strong> будет изменена, изменена или достигла конца <strong>recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a87c7-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a87c7-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="a87c7-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a87c7-129"><strong>Управление изменением строк</strong> — уведомление о том, что что-то в текущем ряду <strong>наборов записей</strong> будет изменено или изменено.</span><span class="sxs-lookup"><span data-stu-id="a87c7-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a87c7-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="a87c7-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a87c7-131"><strong>Управление изменениями в наборе</strong> записей — уведомление о том, что что-то в текущем <strong>наборе записей</strong> изменится или изменилось.</span><span class="sxs-lookup"><span data-stu-id="a87c7-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

