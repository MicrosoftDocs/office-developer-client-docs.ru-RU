---
title: EventReasonEnum (Ссылка на настольные базы данных)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4948cd9a5f1436e4e1afc61bef87b63675e115ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293331"
---
# <a name="eventreasonenum"></a><span data-ttu-id="b7228-102">EventReasonEnum</span><span class="sxs-lookup"><span data-stu-id="b7228-102">EventReasonEnum</span></span>

<span data-ttu-id="b7228-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7228-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7228-104">Указывает причину, по которой произошло событие.</span><span class="sxs-lookup"><span data-stu-id="b7228-104">Specifies the reason that caused an event to occur.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7228-105">Константа</span><span class="sxs-lookup"><span data-stu-id="b7228-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b7228-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b7228-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b7228-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b7228-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7228-108"><strong>adRsnAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-108"><strong>adRsnAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-109">1</span><span class="sxs-lookup"><span data-stu-id="b7228-109">1</span></span></p></td>
<td><p><span data-ttu-id="b7228-110">Операция добавила новую запись.</span><span class="sxs-lookup"><span data-stu-id="b7228-110">An operation added a new record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-111"><strong>adRsnClose</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-111"><strong>adRsnClose</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-112">9 </span><span class="sxs-lookup"><span data-stu-id="b7228-112">9</span></span></p></td>
<td><p><span data-ttu-id="b7228-113">Операция закрыла <strong>Набор записей.</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-113">An operation closed the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-114"><strong>adRsnDelete</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-114"><strong>adRsnDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-115">2</span><span class="sxs-lookup"><span data-stu-id="b7228-115">2</span></span></p></td>
<td><p><span data-ttu-id="b7228-116">Операция удалила запись.</span><span class="sxs-lookup"><span data-stu-id="b7228-116">An operation deleted a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-117"><strong>adRsnFirstChange</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-117"><strong>adRsnFirstChange</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-118">11</span><span class="sxs-lookup"><span data-stu-id="b7228-118">11</span></span></p></td>
<td><p><span data-ttu-id="b7228-119">Операция сделала первое изменение записи.</span><span class="sxs-lookup"><span data-stu-id="b7228-119">An operation made the first change to a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-120"><strong>adRsnMove</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-120"><strong>adRsnMove</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-121">10 </span><span class="sxs-lookup"><span data-stu-id="b7228-121">10</span></span></p></td>
<td><p><span data-ttu-id="b7228-122">Операция переместила указатель записи в <strong>recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-122">An operation moved the record pointer within the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-123"><strong>adRsnMoveFirst</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-123"><strong>adRsnMoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-124">12 </span><span class="sxs-lookup"><span data-stu-id="b7228-124">12</span></span></p></td>
<td><p><span data-ttu-id="b7228-125">Операция переместила указатель записи на первую запись <strong>в Наборе записей.</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-125">An operation moved the record pointer to the first record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-126"><strong>adRsnMoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-126"><strong>adRsnMoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-127">15</span><span class="sxs-lookup"><span data-stu-id="b7228-127">15</span></span></p></td>
<td><p><span data-ttu-id="b7228-128">Операция переместила указатель записи на последнюю запись <strong>в Наборе записей.</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-128">An operation moved the record pointer to the last record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-129"><strong>adRsnMoveNext</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-129"><strong>adRsnMoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-130">13</span><span class="sxs-lookup"><span data-stu-id="b7228-130">13</span></span></p></td>
<td><p><span data-ttu-id="b7228-131">Операция переместила указатель записи на следующую запись <strong>в Наборе записей.</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-131">An operation moved the record pointer to the next record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-132"><strong>adRsnMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-132"><strong>adRsnMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-133">14 </span><span class="sxs-lookup"><span data-stu-id="b7228-133">14</span></span></p></td>
<td><p><span data-ttu-id="b7228-134">Операция переместила указатель записи к предыдущей записи в <strong>Наборе записей.</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-134">An operation moved the record pointer to the previous record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-135"><strong>adRsnRequery</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-135"><strong>adRsnRequery</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-136">7 </span><span class="sxs-lookup"><span data-stu-id="b7228-136">7</span></span></p></td>
<td><p><span data-ttu-id="b7228-137">Операция повторного <a href="recordset-object-ado.md">recordset</a>.</span><span class="sxs-lookup"><span data-stu-id="b7228-137">An operation requeried the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-138"><strong>adRsnResynch</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-138"><strong>adRsnResynch</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-139">8 </span><span class="sxs-lookup"><span data-stu-id="b7228-139">8</span></span></p></td>
<td><p><span data-ttu-id="b7228-140">Операция ресинхронизировала <strong>набор recordset</strong> с базой данных.</span><span class="sxs-lookup"><span data-stu-id="b7228-140">An operation resynchronized the <strong>Recordset</strong> with the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-141"><strong>adRsnUndoAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-141"><strong>adRsnUndoAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-142">5 </span><span class="sxs-lookup"><span data-stu-id="b7228-142">5</span></span></p></td>
<td><p><span data-ttu-id="b7228-143">Операция отменила добавление новой записи.</span><span class="sxs-lookup"><span data-stu-id="b7228-143">An operation reversed the addition of a new record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-144"><strong>adRsnUndoDelete</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-144"><strong>adRsnUndoDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-145">6 </span><span class="sxs-lookup"><span data-stu-id="b7228-145">6</span></span></p></td>
<td><p><span data-ttu-id="b7228-146">Операция отменила удаление записи.</span><span class="sxs-lookup"><span data-stu-id="b7228-146">An operation reversed the deletion of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-147"><strong>adRsnUndoUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-147"><strong>adRsnUndoUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-148">4 </span><span class="sxs-lookup"><span data-stu-id="b7228-148">4</span></span></p></td>
<td><p><span data-ttu-id="b7228-149">Операция отменила обновление записи.</span><span class="sxs-lookup"><span data-stu-id="b7228-149">An operation reversed the update of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-150"><strong>adRsnUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="b7228-150"><strong>adRsnUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="b7228-151">3</span><span class="sxs-lookup"><span data-stu-id="b7228-151">3</span></span></p></td>
<td><p><span data-ttu-id="b7228-152">Операция обновила существующую запись.</span><span class="sxs-lookup"><span data-stu-id="b7228-152">An operation updated an existing record.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b7228-153">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="b7228-153">ADO/WFC equivalent</span></span>

<span data-ttu-id="b7228-154">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b7228-154">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7228-155">Константа</span><span class="sxs-lookup"><span data-stu-id="b7228-155">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7228-156">AdoEnums.EventReason.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="b7228-156">AdoEnums.EventReason.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-157">AdoEnums.EventReason.CLOSE</span><span class="sxs-lookup"><span data-stu-id="b7228-157">AdoEnums.EventReason.CLOSE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-158">AdoEnums.EventReason.DELETE</span><span class="sxs-lookup"><span data-stu-id="b7228-158">AdoEnums.EventReason.DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-159">AdoEnums.EventReason.FIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="b7228-159">AdoEnums.EventReason.FIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-160">AdoEnums.EventReason.MOVE</span><span class="sxs-lookup"><span data-stu-id="b7228-160">AdoEnums.EventReason.MOVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-161">AdoEnums.EventReason.MOVEFIRST</span><span class="sxs-lookup"><span data-stu-id="b7228-161">AdoEnums.EventReason.MOVEFIRST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-162">AdoEnums.EventReason.MOVELAST</span><span class="sxs-lookup"><span data-stu-id="b7228-162">AdoEnums.EventReason.MOVELAST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-163">AdoEnums.EventReason.MOVENEXT</span><span class="sxs-lookup"><span data-stu-id="b7228-163">AdoEnums.EventReason.MOVENEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-164">AdoEnums.EventReason.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="b7228-164">AdoEnums.EventReason.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-165">AdoEnums.EventReason.REQUERY</span><span class="sxs-lookup"><span data-stu-id="b7228-165">AdoEnums.EventReason.REQUERY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-166">AdoEnums.EventReason.RESYNCH</span><span class="sxs-lookup"><span data-stu-id="b7228-166">AdoEnums.EventReason.RESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-167">AdoEnums.EventReason.UNDOADDNEW</span><span class="sxs-lookup"><span data-stu-id="b7228-167">AdoEnums.EventReason.UNDOADDNEW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-168">AdoEnums.EventReason.UNDODELETE</span><span class="sxs-lookup"><span data-stu-id="b7228-168">AdoEnums.EventReason.UNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7228-169">AdoEnums.EventReason.UNDOUPDATE</span><span class="sxs-lookup"><span data-stu-id="b7228-169">AdoEnums.EventReason.UNDOUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7228-170">AdoEnums.EventReason.UPDATE</span><span class="sxs-lookup"><span data-stu-id="b7228-170">AdoEnums.EventReason.UPDATE</span></span></p></td>
</tr>
</tbody>
</table>

