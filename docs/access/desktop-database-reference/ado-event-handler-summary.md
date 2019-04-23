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
# <a name="ado-event-handler-summary"></a><span data-ttu-id="f7528-102">ADO Event Handler Summary</span><span class="sxs-lookup"><span data-stu-id="f7528-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="f7528-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7528-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7528-104">Два объекта ADO могут вызывать события: объект [Connection](connection-object-ado.md) и объект [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f7528-104">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="f7528-105">Семейство **коннектионевент** относится к операциям объекта **Connection** , а семейство **рекордсетевент** относится к операциям объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f7528-105">The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

- <span data-ttu-id="f7528-106">**События подключения**: события, выдаваемые при начале транзакции подключения, фиксируются или откатываются; При выполнении [команды](command-object-ado.md) ; При возникновении предупреждения во время операции **подключения** ; или время начала или окончания **подключения** .</span><span class="sxs-lookup"><span data-stu-id="f7528-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

- <span data-ttu-id="f7528-107">**События Recordset**: события создаются в асинхронных операциях выборки, а также при навигации по строкам объекта **Recordset** , изменении поля в строке объекта Recordset, изменении строки \*\*\*\* в **наборе записей**и открытии \*\* Объект Recordset\*\* с помощью курсора на стороне сервера, закройте **набор записей**или внесите изменения в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="f7528-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="f7528-108">В приведенных ниже таблицах приводится сводка по событиям и их описаниям.</span><span class="sxs-lookup"><span data-stu-id="f7528-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7528-109">Коннектионевент</span><span class="sxs-lookup"><span data-stu-id="f7528-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="f7528-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f7528-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7528-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">События begintranscomplete</a>, CommitTransComplete, RollbackTransComplete</span><span class="sxs-lookup"><span data-stu-id="f7528-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="f7528-112"><strong>Управление транзакциями</strong> — уведомление о том, что текущая транзакция подключения была запущена, зафиксирована или отменена.</span><span class="sxs-lookup"><span data-stu-id="f7528-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-113"><a href="willconnect-event-ado.md">Событие willconnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">события connectcomplete, Disconnect</a></span><span class="sxs-lookup"><span data-stu-id="f7528-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="f7528-114"><strong>Управление подключением</strong> — уведомление о том, что текущее подключение будет запущено, начато или завершено.</span><span class="sxs-lookup"><span data-stu-id="f7528-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7528-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">событие executecomplete</a></span><span class="sxs-lookup"><span data-stu-id="f7528-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f7528-116"><strong>Управление выполнением команд</strong> — уведомление о том, что выполнение текущей команды для подключения будет начато или завершено.</span><span class="sxs-lookup"><span data-stu-id="f7528-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-117"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="f7528-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="f7528-118"><strong>Информационное</strong> сообщение — уведомление о том, что существует дополнительная информация о текущей операции.</span><span class="sxs-lookup"><span data-stu-id="f7528-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
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
<th><p><span data-ttu-id="f7528-119">Рекордсетевент</span><span class="sxs-lookup"><span data-stu-id="f7528-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="f7528-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f7528-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7528-121"><a href="fetchprogress-event-ado.md">Событие fetchprogress</a>, <a href="fetchcomplete-event-ado.md">событие fetchcomplete</a></span><span class="sxs-lookup"><span data-stu-id="f7528-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f7528-122"><strong>Состояние извлечения</strong> — уведомление о ходе выполнения операции извлечения данных или завершении операции извлечения.</span><span class="sxs-lookup"><span data-stu-id="f7528-122"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed.</span></span> <span data-ttu-id="f7528-123">Эти события доступны только в том случае, если <strong>набор записей</strong> был открыт с помощью курсора на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="f7528-123">These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">События willchangefield, FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f7528-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f7528-125"><strong>Управление изменениями полей</strong> — уведомление о том, что значение текущего поля изменится или изменилось.</span><span class="sxs-lookup"><span data-stu-id="f7528-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7528-126"><a href="willmove-and-movecomplete-events-ado.md">События WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">событие endofrecordset</a></span><span class="sxs-lookup"><span data-stu-id="f7528-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="f7528-127"><strong>Управление навигацией</strong> — уведомление о том, что текущая позиция строки в <strong>наборе записей</strong> будет изменена, изменена или достигнут конец <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="f7528-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">События willchangerecord, RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f7528-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f7528-129"><strong>Управление изменениями строк</strong> — уведомление о том, что значение в текущей строке <strong>набора записей</strong> изменится или изменилось.</span><span class="sxs-lookup"><span data-stu-id="f7528-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7528-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">События willchangerecordset, RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f7528-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f7528-131"><strong>Управление изменениями в наборе записей</strong> — уведомление о том, что объект в текущем <strong>наборе записей</strong> изменится или изменился.</span><span class="sxs-lookup"><span data-stu-id="f7528-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

