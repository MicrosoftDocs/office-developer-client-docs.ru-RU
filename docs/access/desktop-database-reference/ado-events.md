---
title: Объекты данных ActiveX (ADO) события
TOCTitle: ADO Events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5938ed58e3b0074f69a4380fd4a0ac0be857084b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482825"
---
# <a name="ado-events"></a><span data-ttu-id="87b51-102">ADO Events</span><span class="sxs-lookup"><span data-stu-id="87b51-102">ADO Events</span></span>


<span data-ttu-id="87b51-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="87b51-103">**Applies to**: Access 2013 | Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87b51-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-105">Вызывается после <strong>BeginTrans</strong> операции.</span><span class="sxs-lookup"><span data-stu-id="87b51-105">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-107">Вызывается после <strong>CommitTrans</strong> операции.</span><span class="sxs-lookup"><span data-stu-id="87b51-107">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-109">Вызывается после запуска подключения.</span><span class="sxs-lookup"><span data-stu-id="87b51-109">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-110"><a href="connectcomplete-and-disconnect-events-ado.md">Отключение</a></span><span class="sxs-lookup"><span data-stu-id="87b51-110"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-111">Вызывается после завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="87b51-111">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="87b51-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-113">Вызывается, когда при попытке перейдите к строке за пределами <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b51-113">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-115">Вызывается после завершения выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="87b51-115">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-117">Вызывается после извлечения всех записей в объемных асинхронной операции в <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b51-117">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="87b51-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-119">Вызывается периодически во время длительных асинхронной операции для отчета, сколько строк в настоящее время извлечения в <strong>набор записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b51-119">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-121">Вызывается после изменения значения одного или нескольких объектов <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b51-121">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-122"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="87b51-122"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-123">Вызывается при каждом появлении предупреждения в процессе выполнения операции <strong>ConnectionEvent</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b51-123">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-125">Вызывается после текущей позиции в изменения <strong>записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b51-125">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-127">Вызывается после изменения одной или нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="87b51-127">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-129">Вызывается после изменения <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b51-129">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="87b51-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-131">Вызывается после операции <strong>RollbackTrans</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b51-131">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="87b51-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-133">Вызывается перед ожидающие операции изменяется значение один или несколько объектов <strong>поля</strong> в <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b51-133">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="87b51-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-135">Вызывается до изменения одного или нескольких записей (строк) в <strong>набор записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b51-135">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="87b51-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-137">Вызывается перед операцию ожидающие изменения <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b51-137">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-138"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="87b51-138"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-139">Вызывается до начала подключения.</span><span class="sxs-lookup"><span data-stu-id="87b51-139">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b51-140"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="87b51-140"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-141">Вызывается непосредственно перед ожидающие команда выполняет для этого подключения и дает пользователю возможность проверки и изменения параметров ожидающих выполнения.</span><span class="sxs-lookup"><span data-stu-id="87b51-141">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b51-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="87b51-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="87b51-143">Событие <strong>WillMove</strong> вызывается <em>перед</em> ожидающие операции изменяет текущую позицию в наборе <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b51-143">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

