---
title: RecordStatusEnum (Ссылка на настольные базы данных)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a83de7730224c5ecd5080c795d38cf2e9a3305a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309382"
---
# <a name="recordstatusenum"></a><span data-ttu-id="1e4ce-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="1e4ce-102">RecordStatusEnum</span></span>

<span data-ttu-id="1e4ce-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e4ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e4ce-104">Указывает состояние записи в отношении пакетных обновлений и других массовых операций.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e4ce-105">Константа</span><span class="sxs-lookup"><span data-stu-id="1e4ce-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1e4ce-106">Значение</span><span class="sxs-lookup"><span data-stu-id="1e4ce-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1e4ce-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1e4ce-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-109">0x100</span><span class="sxs-lookup"><span data-stu-id="1e4ce-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-110">Указывает, что запись не была сохранена из-за отмены операции.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-112">0x400</span><span class="sxs-lookup"><span data-stu-id="1e4ce-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-113">Указывает, что новая запись не была сохранена, так как существующая запись была заблокирована.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-115">0x800</span><span class="sxs-lookup"><span data-stu-id="1e4ce-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-116">Указывает, что запись не была сохранена из-за использования оптимистичных concurrency.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-118">0x40000</span><span class="sxs-lookup"><span data-stu-id="1e4ce-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-119">Указывает, что запись уже удалена из источника данных.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-121">0x4</span><span class="sxs-lookup"><span data-stu-id="1e4ce-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-122">Указывает, что запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="1e4ce-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-125">Указывает, что запись не была сохранена, так как пользователь нарушил ограничения целостности.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-127">0x10</span><span class="sxs-lookup"><span data-stu-id="1e4ce-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-128">Указывает, что запись не была сохранена, так как ее закладки недействительны.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="1e4ce-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-131">Указывает, что запись не была сохранена, так как было слишком много ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-133">0x2</span><span class="sxs-lookup"><span data-stu-id="1e4ce-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-134">Указывает, что запись была изменена.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-136">0x40</span><span class="sxs-lookup"><span data-stu-id="1e4ce-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-137">Указывает, что запись не была сохранена, так как она затронула бы несколько записей.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-139">0x1</span><span class="sxs-lookup"><span data-stu-id="1e4ce-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-140">Указывает, что запись является новой.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="1e4ce-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-143">Указывает, что запись не была сохранена из-за конфликта с открытым объектом хранения.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-145">0</span><span class="sxs-lookup"><span data-stu-id="1e4ce-145">0</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-146">Указывает, что запись была успешно обновлена.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-148">0x8000</span><span class="sxs-lookup"><span data-stu-id="1e4ce-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-149">Указывает, что запись не была сохранена из-за того, что на компьютере не было памяти.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-151">0x80</span><span class="sxs-lookup"><span data-stu-id="1e4ce-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-152">Указывает, что запись не была сохранена, так как она относится к ожидаемой вставке.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-154">0x10000</span><span class="sxs-lookup"><span data-stu-id="1e4ce-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-155">Указывает, что запись не была сохранена, так как у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-157">0x20000</span><span class="sxs-lookup"><span data-stu-id="1e4ce-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-158">Указывает, что запись не была сохранена, так как нарушает структуру баз данных.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="1e4ce-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="1e4ce-160">0x8</span><span class="sxs-lookup"><span data-stu-id="1e4ce-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="1e4ce-161">Указывает, что запись не была изменена.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1e4ce-162">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1e4ce-162">ADO/WFC equivalent</span></span>

<span data-ttu-id="1e4ce-163">AdoEnums.RecordStatus.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="1e4ce-164">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e4ce-165">Константа</span><span class="sxs-lookup"><span data-stu-id="1e4ce-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-166">AdoEnums.RecordStatus.CANCELED</span><span class="sxs-lookup"><span data-stu-id="1e4ce-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-167">AdoEnums.RecordStatus.CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="1e4ce-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="1e4ce-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-169">AdoEnums.RecordStatus.DBDELETED</span><span class="sxs-lookup"><span data-stu-id="1e4ce-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-170">AdoEnums.RecordStatus.DELETED</span><span class="sxs-lookup"><span data-stu-id="1e4ce-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="1e4ce-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-172">AdoEnums.RecordStatus.INVALID</span><span class="sxs-lookup"><span data-stu-id="1e4ce-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-173">AdoEnums.RecordStatus.MAXCHANGESEXCEED</span><span class="sxs-lookup"><span data-stu-id="1e4ce-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-174">AdoEnums.RecordStatus.MODIFIED</span><span class="sxs-lookup"><span data-stu-id="1e4ce-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="1e4ce-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-176">AdoEnums.RecordStatus.NEW</span><span class="sxs-lookup"><span data-stu-id="1e4ce-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-177">AdoEnums.RecordStatus.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="1e4ce-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-178">AdoEnums.RecordStatus.OK</span><span class="sxs-lookup"><span data-stu-id="1e4ce-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-179">AdoEnums.RecordStatus.OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="1e4ce-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-180">AdoEnums.RecordStatus.PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="1e4ce-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="1e4ce-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e4ce-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="1e4ce-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e4ce-183">AdoEnums.RecordStatus.UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="1e4ce-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

