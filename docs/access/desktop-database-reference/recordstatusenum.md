---
title: RecordStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88929ced56583316c42f2d5195054e51e98a1d5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481169"
---
# <a name="recordstatusenum"></a><span data-ttu-id="164a3-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="164a3-102">RecordStatusEnum</span></span>


<span data-ttu-id="164a3-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="164a3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="164a3-104">Указывает состояние записи по отношению к пакета обновлений и других массовых операций.</span><span class="sxs-lookup"><span data-stu-id="164a3-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="164a3-105">Константа</span><span class="sxs-lookup"><span data-stu-id="164a3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="164a3-106">Значение</span><span class="sxs-lookup"><span data-stu-id="164a3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="164a3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="164a3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="164a3-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-109">0x100</span><span class="sxs-lookup"><span data-stu-id="164a3-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="164a3-110">Указывает, что запись не была сохранена, так как операция отменена.</span><span class="sxs-lookup"><span data-stu-id="164a3-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-112">0x400</span><span class="sxs-lookup"><span data-stu-id="164a3-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="164a3-113">Указывает, что новую запись не был сохранен, так как существующей записи был заблокирован.</span><span class="sxs-lookup"><span data-stu-id="164a3-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-115">0x800</span><span class="sxs-lookup"><span data-stu-id="164a3-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="164a3-116">Указывает, что запись не была сохранена оптимистичный параллелизм использовался в.</span><span class="sxs-lookup"><span data-stu-id="164a3-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-118">0x40000</span><span class="sxs-lookup"><span data-stu-id="164a3-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="164a3-119">Указывает, что запись уже была удалена из источника данных.</span><span class="sxs-lookup"><span data-stu-id="164a3-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-121">0x4</span><span class="sxs-lookup"><span data-stu-id="164a3-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="164a3-122">Указывает, что запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="164a3-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="164a3-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="164a3-125">Указывает, что запись не была сохранена, так как пользователь нарушает ограничения целостности данных.</span><span class="sxs-lookup"><span data-stu-id="164a3-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-127">0x10</span><span class="sxs-lookup"><span data-stu-id="164a3-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="164a3-128">Указывает, что запись не была сохранена, так как ее закладки является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="164a3-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="164a3-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="164a3-131">Указывает, что запись не была сохранена из-за слишком много ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="164a3-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-133">0x2</span><span class="sxs-lookup"><span data-stu-id="164a3-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="164a3-134">Указывает, что запись была изменена.</span><span class="sxs-lookup"><span data-stu-id="164a3-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-136">0x40</span><span class="sxs-lookup"><span data-stu-id="164a3-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="164a3-137">Указывает, что запись не была сохранена, так как он бы влияет несколько записей.</span><span class="sxs-lookup"><span data-stu-id="164a3-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-139">0x1</span><span class="sxs-lookup"><span data-stu-id="164a3-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="164a3-140">Указывает, что запись является новой.</span><span class="sxs-lookup"><span data-stu-id="164a3-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="164a3-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="164a3-143">Указывает, что запись не была сохранена из-за конфликта с помощью объекта open хранилища.</span><span class="sxs-lookup"><span data-stu-id="164a3-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-145">0</span><span class="sxs-lookup"><span data-stu-id="164a3-145">0</span></span></p></td>
<td><p><span data-ttu-id="164a3-146">Указывает, что запись успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="164a3-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-148">0x8000</span><span class="sxs-lookup"><span data-stu-id="164a3-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="164a3-149">Указывает, что запись не была сохранена, так как компьютер хватает памяти.</span><span class="sxs-lookup"><span data-stu-id="164a3-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-151">0x80</span><span class="sxs-lookup"><span data-stu-id="164a3-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="164a3-152">Указывает, что запись не была сохранена, так как она ссылается на очередь вставки.</span><span class="sxs-lookup"><span data-stu-id="164a3-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-154">0x10000</span><span class="sxs-lookup"><span data-stu-id="164a3-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="164a3-155">Указывает, что запись не была сохранена, так как пользователь не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="164a3-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-157">0x20000</span><span class="sxs-lookup"><span data-stu-id="164a3-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="164a3-158">Указывает, что запись не была сохранена, поскольку оно нарушает структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="164a3-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="164a3-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="164a3-160">0x8</span><span class="sxs-lookup"><span data-stu-id="164a3-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="164a3-161">Указывает, что записи не были изменены.</span><span class="sxs-lookup"><span data-stu-id="164a3-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="164a3-162">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="164a3-162">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="164a3-163">AdoEnums.RecordStatus.</span><span class="sxs-lookup"><span data-stu-id="164a3-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="164a3-164">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="164a3-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="164a3-165">Constant</span><span class="sxs-lookup"><span data-stu-id="164a3-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="164a3-166">AdoEnums.RecordStatus.CANCELED</span><span class="sxs-lookup"><span data-stu-id="164a3-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-167">AdoEnums.RecordStatus.CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="164a3-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="164a3-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-169">AdoEnums.RecordStatus.DBDELETED</span><span class="sxs-lookup"><span data-stu-id="164a3-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-170">AdoEnums.RecordStatus.DELETED</span><span class="sxs-lookup"><span data-stu-id="164a3-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="164a3-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-172">AdoEnums.RecordStatus.INVALID</span><span class="sxs-lookup"><span data-stu-id="164a3-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="164a3-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-174">AdoEnums.RecordStatus.MODIFIED</span><span class="sxs-lookup"><span data-stu-id="164a3-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="164a3-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-176">AdoEnums.RecordStatus.NEW</span><span class="sxs-lookup"><span data-stu-id="164a3-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-177">AdoEnums.RecordStatus.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="164a3-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-178">AdoEnums.RecordStatus.OK</span><span class="sxs-lookup"><span data-stu-id="164a3-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-179">AdoEnums.RecordStatus.OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="164a3-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-180">AdoEnums.RecordStatus.PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="164a3-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="164a3-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="164a3-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="164a3-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="164a3-183">AdoEnums.RecordStatus.UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="164a3-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

