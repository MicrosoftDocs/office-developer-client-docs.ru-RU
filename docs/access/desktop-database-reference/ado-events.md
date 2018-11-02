---
title: События ActiveX Data Objects (ADO)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3cc8ac02e2410a2f7bfe1038851e16f50c1ea2ee
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910945"
---
# <a name="ado-events"></a><span data-ttu-id="b1206-102">События ADO</span><span class="sxs-lookup"><span data-stu-id="b1206-102">ADO events</span></span>

<span data-ttu-id="b1206-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1206-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="b1206-104">Событие</span><span class="sxs-lookup"><span data-stu-id="b1206-104">Event</span></span></th>
<th><span data-ttu-id="b1206-105">Описание</span><span class="sxs-lookup"><span data-stu-id="b1206-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-107">Вызывается после <strong>BeginTrans</strong> операции.</span><span class="sxs-lookup"><span data-stu-id="b1206-107">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-109">Вызывается после <strong>CommitTrans</strong> операции.</span><span class="sxs-lookup"><span data-stu-id="b1206-109">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-111">Вызывается после запуска подключения.</span><span class="sxs-lookup"><span data-stu-id="b1206-111">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-112"><a href="connectcomplete-and-disconnect-events-ado.md">Отключение</a></span><span class="sxs-lookup"><span data-stu-id="b1206-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-113">Вызывается после завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="b1206-113">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="b1206-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-115">Вызывается, когда при попытке перейдите к строке за пределами <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1206-115">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-117">Вызывается после завершения выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="b1206-117">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-119">Вызывается после извлечения всех записей в объемных асинхронной операции в <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1206-119">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="b1206-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-121">Вызывается периодически во время длительных асинхронной операции для отчета, сколько строк в настоящее время извлечения в <strong>набор записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1206-121">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-123">Вызывается после изменения значения одного или нескольких объектов <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="b1206-123">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-124"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="b1206-124"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-125">Вызывается при каждом появлении предупреждения в процессе выполнения операции <strong>ConnectionEvent</strong> .</span><span class="sxs-lookup"><span data-stu-id="b1206-125">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-127">Вызывается после текущей позиции в изменения <strong>записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="b1206-127">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-129">Вызывается после изменения одной или нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="b1206-129">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-131">Вызывается после изменения <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="b1206-131">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="b1206-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-133">Вызывается после операции <strong>RollbackTrans</strong> .</span><span class="sxs-lookup"><span data-stu-id="b1206-133">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="b1206-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-135">Вызывается перед ожидающие операции изменяется значение один или несколько объектов <strong>поля</strong> в <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1206-135">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="b1206-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-137">Вызывается до изменения одного или нескольких записей (строк) в <strong>набор записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="b1206-137">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="b1206-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-139">Вызывается перед операцию ожидающие изменения <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1206-139">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-140"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="b1206-140"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-141">Вызывается до начала подключения.</span><span class="sxs-lookup"><span data-stu-id="b1206-141">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1206-142"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="b1206-142"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-143">Вызывается непосредственно перед ожидающие команда выполняет для этого подключения и дает пользователю возможность проверки и изменения параметров ожидающих выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1206-143">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1206-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="b1206-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="b1206-145">Событие <strong>WillMove</strong> вызывается <em>перед</em> ожидающие операции изменяет текущую позицию в наборе <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1206-145">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>