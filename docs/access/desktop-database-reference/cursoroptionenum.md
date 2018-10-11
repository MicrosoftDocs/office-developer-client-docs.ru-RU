---
title: CursorOptionEnum (Справочник по для настольных баз данных Access)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6d6f66e3bdee06611faafef5d32a2a486fc2028
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480691"
---
# <a name="cursoroptionenum"></a><span data-ttu-id="7c870-102">CursorOptionEnum</span><span class="sxs-lookup"><span data-stu-id="7c870-102">CursorOptionEnum</span></span>


<span data-ttu-id="7c870-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c870-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7c870-104">Указывает, какие функции [поддерживает](supports-method-ado.md) метод, следует проверить наличие.</span><span class="sxs-lookup"><span data-stu-id="7c870-104">Specifies what functionality the [Supports](supports-method-ado.md) method should test for.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c870-105">Константа</span><span class="sxs-lookup"><span data-stu-id="7c870-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7c870-106">Значение</span><span class="sxs-lookup"><span data-stu-id="7c870-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7c870-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7c870-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c870-108"><strong>adAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-108"><strong>adAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-109">0x1000400</span><span class="sxs-lookup"><span data-stu-id="7c870-109">0x1000400</span></span></p></td>
<td><p><span data-ttu-id="7c870-110">Поддерживает метод <a href="addnew-method-ado.md">AddNew</a> для добавления новых записей.</span><span class="sxs-lookup"><span data-stu-id="7c870-110">Supports the <a href="addnew-method-ado.md">AddNew</a> method to add new records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-111"><strong>adApproxPosition</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-111"><strong>adApproxPosition</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-112">0x4000</span><span class="sxs-lookup"><span data-stu-id="7c870-112">0x4000</span></span></p></td>
<td><p><span data-ttu-id="7c870-113">Поддерживает свойства <a href="absoluteposition-property-ado.md">AbsolutePosition</a> и <a href="absolutepage-property-ado.md">AbsolutePage</a> .</span><span class="sxs-lookup"><span data-stu-id="7c870-113">Supports the <a href="absoluteposition-property-ado.md">AbsolutePosition</a> and <a href="absolutepage-property-ado.md">AbsolutePage</a> properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-114"><strong>adBookmark</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-114"><strong>adBookmark</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="7c870-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="7c870-116">Поддерживает свойства <a href="bookmark-property-ado.md">закладку</a> для получения доступа к определенным записей.</span><span class="sxs-lookup"><span data-stu-id="7c870-116">Supports the <a href="bookmark-property-ado.md">Bookmark</a> property to gain access to specific records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-117"><strong>adDelete</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-117"><strong>adDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-118">0x1000800</span><span class="sxs-lookup"><span data-stu-id="7c870-118">0x1000800</span></span></p></td>
<td><p><span data-ttu-id="7c870-119">Поддерживает метод <a href="delete-method-ado-recordset.md">Delete</a> для удаления записей.</span><span class="sxs-lookup"><span data-stu-id="7c870-119">Supports the <a href="delete-method-ado-recordset.md">Delete</a> method to delete records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-120"><strong>adFind</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-120"><strong>adFind</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-121">0x80000</span><span class="sxs-lookup"><span data-stu-id="7c870-121">0x80000</span></span></p></td>
<td><p><span data-ttu-id="7c870-122">Поддерживает метод <a href="find-method-ado.md">поиска</a> для поиска строки в <a href="recordset-object-ado.md">набора записей</a>.</span><span class="sxs-lookup"><span data-stu-id="7c870-122">Supports the <a href="find-method-ado.md">Find</a> method to locate a row in a <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-123"><strong>adHoldRecords</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-123"><strong>adHoldRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-124">0x100</span><span class="sxs-lookup"><span data-stu-id="7c870-124">0x100</span></span></p></td>
<td><p><span data-ttu-id="7c870-125">Извлекает несколько записей или изменяет следующей позиции без фиксации все ожидающие изменения.</span><span class="sxs-lookup"><span data-stu-id="7c870-125">Retrieves more records or changes the next position without committing all pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-126"><strong>adIndex</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-126"><strong>adIndex</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-127">0x100000</span><span class="sxs-lookup"><span data-stu-id="7c870-127">0x100000</span></span></p></td>
<td><p><span data-ttu-id="7c870-128">Поддерживает свойства <a href="index-property-ado.md">Index</a> одно имя индекса.</span><span class="sxs-lookup"><span data-stu-id="7c870-128">Supports the <a href="index-property-ado.md">Index</a> property to name an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-129"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-129"><strong>adMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-130">0x200</span><span class="sxs-lookup"><span data-stu-id="7c870-130">0x200</span></span></p></td>
<td><p><span data-ttu-id="7c870-131">Поддерживает <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> и <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> методы и методы <a href="move-method-ado.md">перемещения</a> или <a href="getrows-method-ado.md">Получение строк</a> для перемещения положения текущей записи обратной без необходимости установки закладки.</span><span class="sxs-lookup"><span data-stu-id="7c870-131">Supports the <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> and <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> methods, and <a href="move-method-ado.md">Move</a> or <a href="getrows-method-ado.md">GetRows</a> methods to move the current record position backward without requiring bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-132"><strong>adNotify</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-132"><strong>adNotify</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-133">0x40000</span><span class="sxs-lookup"><span data-stu-id="7c870-133">0x40000</span></span></p></td>
<td><p><span data-ttu-id="7c870-134">Указывает, что базовый поставщик данных поддерживает уведомления (что определяет, поддерживается ли события <strong>набора записей</strong> ).</span><span class="sxs-lookup"><span data-stu-id="7c870-134">Indicates that the underlying data provider supports notifications (which determines whether <strong>Recordset</strong> events are supported).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-135"><strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-135"><strong>adResync</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-136">0x20000</span><span class="sxs-lookup"><span data-stu-id="7c870-136">0x20000</span></span></p></td>
<td><p><span data-ttu-id="7c870-137">Поддерживает метод <a href="resync-method-ado.md">выполнить повторную синхронизацию</a> для обновления курсора с данными, который будет отображаться в основной базе данных.</span><span class="sxs-lookup"><span data-stu-id="7c870-137">Supports the <a href="resync-method-ado.md">Resync</a> method to update the cursor with the data that is visible in the underlying database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-138"><strong>adSeek</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-138"><strong>adSeek</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-139">0x200000</span><span class="sxs-lookup"><span data-stu-id="7c870-139">0x200000</span></span></p></td>
<td><p><span data-ttu-id="7c870-140">Поддерживает метод <a href="seek-method-ado.md">поиска</a> для поиска строки в <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c870-140">Supports the <a href="seek-method-ado.md">Seek</a> method to locate a row in a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-141"><strong>adUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-141"><strong>adUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-142">0x1008000</span><span class="sxs-lookup"><span data-stu-id="7c870-142">0x1008000</span></span></p></td>
<td><p><span data-ttu-id="7c870-143">Поддерживает метод <a href="update-method-ado.md">Update</a> для изменения существующих данных.</span><span class="sxs-lookup"><span data-stu-id="7c870-143">Supports the <a href="update-method-ado.md">Update</a> method to modify existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-144"><strong>adUpdateBatch</strong></span><span class="sxs-lookup"><span data-stu-id="7c870-144"><strong>adUpdateBatch</strong></span></span></p></td>
<td><p><span data-ttu-id="7c870-145">0x10000</span><span class="sxs-lookup"><span data-stu-id="7c870-145">0x10000</span></span></p></td>
<td><p><span data-ttu-id="7c870-146">Поддерживает пакетного обновления (методы<a href="updatebatch-method-ado.md">UpdateBatch</a> и <a href="cancelbatch-method-ado.md">CancelBatch</a> ) для передачи группы об изменениях в поставщик.</span><span class="sxs-lookup"><span data-stu-id="7c870-146">Supports batch updating (<a href="updatebatch-method-ado.md">UpdateBatch</a> and <a href="cancelbatch-method-ado.md">CancelBatch</a> methods) to transmit groups of changes to the provider.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7c870-147">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="7c870-147">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="7c870-148">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7c870-148">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c870-149">Constant</span><span class="sxs-lookup"><span data-stu-id="7c870-149">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c870-150">AdoEnums.CursorOption.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="7c870-150">AdoEnums.CursorOption.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-151">AdoEnums.CursorOption.APPROXPOSITION</span><span class="sxs-lookup"><span data-stu-id="7c870-151">AdoEnums.CursorOption.APPROXPOSITION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-152">AdoEnums.CursorOption.BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="7c870-152">AdoEnums.CursorOption.BOOKMARK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-153">AdoEnums.CursorOption.DELETE</span><span class="sxs-lookup"><span data-stu-id="7c870-153">AdoEnums.CursorOption.DELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-154">AdoEnums.CursorOption.FIND</span><span class="sxs-lookup"><span data-stu-id="7c870-154">AdoEnums.CursorOption.FIND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-155">AdoEnums.CursorOption.HOLDRECORDS</span><span class="sxs-lookup"><span data-stu-id="7c870-155">AdoEnums.CursorOption.HOLDRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-156">AdoEnums.CursorOption.INDEX</span><span class="sxs-lookup"><span data-stu-id="7c870-156">AdoEnums.CursorOption.INDEX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-157">AdoEnums.CursorOption.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="7c870-157">AdoEnums.CursorOption.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-158">AdoEnums.CursorOption.NOTIFY</span><span class="sxs-lookup"><span data-stu-id="7c870-158">AdoEnums.CursorOption.NOTIFY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-159">AdoEnums.CursorOption.RESYNC</span><span class="sxs-lookup"><span data-stu-id="7c870-159">AdoEnums.CursorOption.RESYNC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-160">AdoEnums.CursorOption.SEEK</span><span class="sxs-lookup"><span data-stu-id="7c870-160">AdoEnums.CursorOption.SEEK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c870-161">AdoEnums.CursorOption.UPDATE</span><span class="sxs-lookup"><span data-stu-id="7c870-161">AdoEnums.CursorOption.UPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c870-162">AdoEnums.CursorOption.UPDATEBATCH</span><span class="sxs-lookup"><span data-stu-id="7c870-162">AdoEnums.CursorOption.UPDATEBATCH</span></span></p></td>
</tr>
</tbody>
</table>

