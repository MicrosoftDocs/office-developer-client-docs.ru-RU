---
title: Сводка по обработчикам событий ADO
TOCTitle: ADO Event Handler Summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e47cf076c213707857285757d936d58bd153e7c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880602"
---
# <a name="ado-event-handler-summary"></a><span data-ttu-id="915ec-102">Сводка по обработчикам событий ADO</span><span class="sxs-lookup"><span data-stu-id="915ec-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="915ec-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="915ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="915ec-104">Два объекта ADO могут вызывать события: объект [подключения](connection-object-ado.md) и объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="915ec-104">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="915ec-105">Семейство **ConnectionEvent** относится к операции на объект **подключения** , а семейства **RecordsetEvent** относится к операции в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="915ec-105">The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

  - <span data-ttu-id="915ec-106">**Подключение событий**: события выдается, когда начинается транзакций для подключения, прилагает все усилия или откат; При выполнении [команды](command-object-ado.md) ; При появлении предупреждения во время операции **Подключения событий** ; или при запуске или завершает **подключение** .</span><span class="sxs-lookup"><span data-stu-id="915ec-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

  - <span data-ttu-id="915ec-107">**Набор записей событий**: события выдается вокруг операции асинхронной выборки, а также при переходе по строкам объекта **набора записей** , изменение поля в строке из **набора записей**, измените строку в **набор записей**, откройте \*\* Набор записей\*\* с курсором на сервере, закройте **записей**или внести какие-либо изменения никакой в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="915ec-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="915ec-108">В следующей таблице перечислены события и их описание.</span><span class="sxs-lookup"><span data-stu-id="915ec-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="915ec-109">ConnectionEvent</span><span class="sxs-lookup"><span data-stu-id="915ec-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="915ec-110">Описание</span><span class="sxs-lookup"><span data-stu-id="915ec-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="915ec-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span><span class="sxs-lookup"><span data-stu-id="915ec-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="915ec-112"><strong>Управление транзакциями</strong> , уведомления о запуске текущей операции на подключение, фиксации или отката.</span><span class="sxs-lookup"><span data-stu-id="915ec-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="915ec-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, отключите</a></span><span class="sxs-lookup"><span data-stu-id="915ec-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="915ec-114"><strong>Управление подключениями</strong> — уведомление, в котором будет запущен процесс текущее подключение, запущена или его завершения.</span><span class="sxs-lookup"><span data-stu-id="915ec-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="915ec-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="915ec-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="915ec-116"><strong>Управление командами выполнения</strong> — уведомление, выполнение текущей команды на подключение будет запущен процесс или его завершения.</span><span class="sxs-lookup"><span data-stu-id="915ec-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="915ec-117"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="915ec-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="915ec-118"><strong>Информационное</strong> — уведомления о наличии Дополнительные сведения о текущей операции.</span><span class="sxs-lookup"><span data-stu-id="915ec-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
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
<th><p><span data-ttu-id="915ec-119">RecordsetEvent</span><span class="sxs-lookup"><span data-stu-id="915ec-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="915ec-120">Описание</span><span class="sxs-lookup"><span data-stu-id="915ec-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="915ec-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="915ec-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="915ec-122"><strong>Состояние извлечения</strong> — уведомления о ходе выполнения операции по извлечению данных или завершения операции извлечения.</span><span class="sxs-lookup"><span data-stu-id="915ec-122"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed.</span></span> <span data-ttu-id="915ec-123">Эти события доступны только в том случае, если <strong>набор записей</strong> был открыт с помощью клиентского курсора.</span><span class="sxs-lookup"><span data-stu-id="915ec-123">These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="915ec-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="915ec-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="915ec-125"><strong>Управление измените поле</strong> — уведомление, значение текущего поля изменится или была изменена.</span><span class="sxs-lookup"><span data-stu-id="915ec-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="915ec-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="915ec-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="915ec-127"><strong>Управления навигации</strong> — уведомление, изменится текущей позиции строки в <strong>набор записей</strong> , были изменены или достигнут конец <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="915ec-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="915ec-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="915ec-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="915ec-129"><strong>Управление измените строку</strong> — уведомление, что-нибудь в текущей строки <strong>набора записей</strong> изменится или была изменена.</span><span class="sxs-lookup"><span data-stu-id="915ec-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="915ec-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="915ec-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="915ec-131"><strong>Управление изменение записей</strong> — уведомление, что-нибудь в текущего <strong>набора записей</strong> изменится или была изменена.</span><span class="sxs-lookup"><span data-stu-id="915ec-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

