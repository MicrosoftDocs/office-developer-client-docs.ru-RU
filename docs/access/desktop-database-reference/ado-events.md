---
title: События объектов данных ActiveX (ADO)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cc2ef73798dca18e00c42768fde78da2abdb56a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283340"
---
# <a name="ado-events"></a><span data-ttu-id="eabe9-102">События ADO</span><span class="sxs-lookup"><span data-stu-id="eabe9-102">ADO events</span></span>

<span data-ttu-id="eabe9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eabe9-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="eabe9-104">Событие</span><span class="sxs-lookup"><span data-stu-id="eabe9-104">Event</span></span></th>
<th><span data-ttu-id="eabe9-105">Описание</span><span class="sxs-lookup"><span data-stu-id="eabe9-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">События begintranscomplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-107">Вызывается после операции <strong>BeginTrans</strong> .</span><span class="sxs-lookup"><span data-stu-id="eabe9-107">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-109">Вызывается после операции <strong>CommitTrans</strong> .</span><span class="sxs-lookup"><span data-stu-id="eabe9-109">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-110"><a href="connectcomplete-and-disconnect-events-ado.md">События connectcomplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-111">Вызывается после запуска подключения.</span><span class="sxs-lookup"><span data-stu-id="eabe9-111">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-113">Вызывается после завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="eabe9-113">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-114"><a href="endofrecordset-event-ado.md">Событие endofrecordset</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-115">Вызывается при попытке переместиться в строку, находящиеся за концом объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eabe9-115">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-116"><a href="executecomplete-event-ado.md">Событие executecomplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-117">Вызывается после завершения выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="eabe9-117">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-118"><a href="fetchcomplete-event-ado.md">Событие fetchcomplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-119">Вызывается после того, как все записи в длительной асинхронной операции были получены в <strong>набор записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="eabe9-119">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-120"><a href="fetchprogress-event-ado.md">Событие fetchprogress</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-121">Вызывается периодически в ходе длительной асинхронной операции, чтобы сообщить, сколько строк в данный момент было извлечено в <strong>набор записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="eabe9-121">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-123">Вызывается после изменения значения одного или нескольких объектов <strong>field</strong> .</span><span class="sxs-lookup"><span data-stu-id="eabe9-123">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-124"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-124"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-125">Вызывается при возникновении предупреждения в ходе операции <strong>коннектионевент</strong> .</span><span class="sxs-lookup"><span data-stu-id="eabe9-125">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-127">Вызывается после изменения текущей позиции в <strong>наборе записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="eabe9-127">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-129">Вызывается после изменения одной или нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="eabe9-129">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-131">Вызывается после изменения объекта <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="eabe9-131">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-133">Вызывается после операции <strong>RollbackTrans</strong> .</span><span class="sxs-lookup"><span data-stu-id="eabe9-133">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">События willchangefield</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-135">Вызывается до того, как ожидающая операция изменяет значение одного или нескольких объектов <strong>field</strong> в <strong>наборе записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="eabe9-135">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">События willchangerecord</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-137">Вызывается перед одной или несколькими записями (строк) в изменении <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="eabe9-137">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">События willchangerecordset</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-139">Вызывается до того, как ожидающая операция изменит объект <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eabe9-139">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-140"><a href="willconnect-event-ado.md">Событие willconnect</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-140"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-141">Вызывается перед запуском подключения.</span><span class="sxs-lookup"><span data-stu-id="eabe9-141">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eabe9-142"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-142"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-143">Вызывается непосредственно перед выполнением ожидающей команды для этого подключения и предоставляет пользователю возможность просматривать и изменять параметры, ожидающие выполнения.</span><span class="sxs-lookup"><span data-stu-id="eabe9-143">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eabe9-144"><a href="willmove-and-movecomplete-events-ado.md">События WillMove</a></span><span class="sxs-lookup"><span data-stu-id="eabe9-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="eabe9-145">Событие <strong>события WillMove</strong> вызывается до того, <em>как</em> ожидающая операция меняет текущую позицию в <strong>наборе записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="eabe9-145">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
