---
title: RecordStatusEnum (Справочник по базам данных Access на компьютере)
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
# <a name="recordstatusenum"></a><span data-ttu-id="0e608-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="0e608-102">RecordStatusEnum</span></span>

<span data-ttu-id="0e608-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e608-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e608-104">Указывает состояние записи по отношению к пакетным обновлениям и другим массовым операциям.</span><span class="sxs-lookup"><span data-stu-id="0e608-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e608-105">Константа</span><span class="sxs-lookup"><span data-stu-id="0e608-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0e608-106">Значение</span><span class="sxs-lookup"><span data-stu-id="0e608-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0e608-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0e608-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e608-108"><strong>Адрекканцелед</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-109">0x100</span><span class="sxs-lookup"><span data-stu-id="0e608-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="0e608-110">Указывает, что запись не была сохранена, так как операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="0e608-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-111"><strong>Адреккантрелеасе</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-112">0x400</span><span class="sxs-lookup"><span data-stu-id="0e608-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="0e608-113">Указывает, что новая запись не была сохранена, так как существующая запись заблокирована.</span><span class="sxs-lookup"><span data-stu-id="0e608-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-114"><strong>Адрекконкурренцивиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-115">0x800</span><span class="sxs-lookup"><span data-stu-id="0e608-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="0e608-116">Указывает, что запись не была сохранена из-за использования оптимистичного параллелизма.</span><span class="sxs-lookup"><span data-stu-id="0e608-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-117"><strong>Адрекдбделетед</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-118">0x40000</span><span class="sxs-lookup"><span data-stu-id="0e608-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="0e608-119">Указывает, что запись уже была удалена из источника данных.</span><span class="sxs-lookup"><span data-stu-id="0e608-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-120"><strong>Адрекделетед</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-121">0x4</span><span class="sxs-lookup"><span data-stu-id="0e608-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="0e608-122">Указывает, что запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="0e608-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-123"><strong>АдреЦинтегритивиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="0e608-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="0e608-125">Указывает, что запись не была сохранена, так как пользователь нарушил ограничения целостности.</span><span class="sxs-lookup"><span data-stu-id="0e608-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-126"><strong>АдреЦинвалид</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-127">0x10</span><span class="sxs-lookup"><span data-stu-id="0e608-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="0e608-128">Указывает, что запись не была сохранена, так как ее Закладка является недопустимой.</span><span class="sxs-lookup"><span data-stu-id="0e608-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-129"><strong>Адрекмаксчанжесексцеедед</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="0e608-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="0e608-131">Указывает, что запись не была сохранена из-за слишком большого количества ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="0e608-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-132"><strong>Адрекмодифиед</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-133">0x2</span><span class="sxs-lookup"><span data-stu-id="0e608-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="0e608-134">Указывает, что запись была изменена.</span><span class="sxs-lookup"><span data-stu-id="0e608-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-135"><strong>Адрекмултиплечанжес</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-136">0x40</span><span class="sxs-lookup"><span data-stu-id="0e608-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="0e608-137">Указывает, что запись не была сохранена, так как она бы затронула несколько записей.</span><span class="sxs-lookup"><span data-stu-id="0e608-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-138"><strong>Адрекнев</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-139">0x1</span><span class="sxs-lookup"><span data-stu-id="0e608-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="0e608-140">Указывает, что запись является новой.</span><span class="sxs-lookup"><span data-stu-id="0e608-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-141"><strong>Адрекобжектопен</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="0e608-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="0e608-143">Указывает, что запись не была сохранена из-за конфликта с открытым объектом хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e608-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-144"><strong>Адрекок</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-145">нуль</span><span class="sxs-lookup"><span data-stu-id="0e608-145">0</span></span></p></td>
<td><p><span data-ttu-id="0e608-146">Указывает, что запись успешно обновлена.</span><span class="sxs-lookup"><span data-stu-id="0e608-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-147"><strong>Адрекаутофмемори</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-148">0x8000</span><span class="sxs-lookup"><span data-stu-id="0e608-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="0e608-149">Указывает, что запись не была сохранена из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="0e608-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-150"><strong>Адрекпендингчанжес</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-151">0x80</span><span class="sxs-lookup"><span data-stu-id="0e608-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="0e608-152">Указывает, что запись не была сохранена, так как она относится к ожидающей вставке.</span><span class="sxs-lookup"><span data-stu-id="0e608-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-153"><strong>Адрекпермиссиондениед</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-154">0x10000</span><span class="sxs-lookup"><span data-stu-id="0e608-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="0e608-155">Указывает, что запись не была сохранена, так как у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="0e608-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-156"><strong>Адрексчемавиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-157">0x20000</span><span class="sxs-lookup"><span data-stu-id="0e608-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="0e608-158">Указывает, что запись не была сохранена, так как она нарушает структуру основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="0e608-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-159"><strong>Адрекунмодифиед</strong></span><span class="sxs-lookup"><span data-stu-id="0e608-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="0e608-160">0x8</span><span class="sxs-lookup"><span data-stu-id="0e608-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="0e608-161">Указывает, что запись не была изменена.</span><span class="sxs-lookup"><span data-stu-id="0e608-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0e608-162">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0e608-162">ADO/WFC equivalent</span></span>

<span data-ttu-id="0e608-163">Адоенумс. Рекордстатус.</span><span class="sxs-lookup"><span data-stu-id="0e608-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="0e608-164">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="0e608-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e608-165">Константа</span><span class="sxs-lookup"><span data-stu-id="0e608-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e608-166">Адоенумс. Рекордстатус. CANCELed</span><span class="sxs-lookup"><span data-stu-id="0e608-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-167">Адоенумс. Рекордстатус. КАНТРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="0e608-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-168">Адоенумс. Рекордстатус. КОНКУРРЕНЦИВИОЛАТИОН</span><span class="sxs-lookup"><span data-stu-id="0e608-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-169">Адоенумс. Рекордстатус. ДБДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="0e608-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-170">Адоенумс. Рекордстатус. DELETEd</span><span class="sxs-lookup"><span data-stu-id="0e608-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-171">Адоенумс. Рекордстатус. ИНТЕГРИТИВИОЛАТИОН</span><span class="sxs-lookup"><span data-stu-id="0e608-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-172">Адоенумс. Рекордстатус. INVALID</span><span class="sxs-lookup"><span data-stu-id="0e608-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-173">Адоенумс. Рекордстатус. МАКСЧАНЖЕСЕКСЦЕЕДЕД</span><span class="sxs-lookup"><span data-stu-id="0e608-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-174">Адоенумс. Рекордстатус. MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0e608-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-175">Адоенумс. Рекордстатус. МУЛТИПЛЕЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="0e608-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-176">Адоенумс. Рекордстатус. NEW</span><span class="sxs-lookup"><span data-stu-id="0e608-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-177">Адоенумс. Рекордстатус. ОБЖЕКТОПЕН</span><span class="sxs-lookup"><span data-stu-id="0e608-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-178">Адоенумс. Рекордстатус. ОК</span><span class="sxs-lookup"><span data-stu-id="0e608-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-179">Адоенумс. Рекордстатус. АУТОФМЕМОРИ</span><span class="sxs-lookup"><span data-stu-id="0e608-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-180">Адоенумс. Рекордстатус. ПЕНДИНГЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="0e608-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-181">Адоенумс. Рекордстатус. ПЕРМИССИОНДЕНИЕД</span><span class="sxs-lookup"><span data-stu-id="0e608-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e608-182">Адоенумс. Рекордстатус. СЧЕМАВИОЛАТИОН</span><span class="sxs-lookup"><span data-stu-id="0e608-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e608-183">Адоенумс. Рекордстатус. unMODIFIED</span><span class="sxs-lookup"><span data-stu-id="0e608-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

