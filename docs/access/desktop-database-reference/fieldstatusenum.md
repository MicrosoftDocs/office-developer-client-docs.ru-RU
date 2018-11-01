---
title: FieldStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 007daa84e15b79d6aa82e4e1e75b1c3d2b0901ce
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867925"
---
# <a name="fieldstatusenum"></a><span data-ttu-id="4f089-102">FieldStatusEnum</span><span class="sxs-lookup"><span data-stu-id="4f089-102">FieldStatusEnum</span></span>

<span data-ttu-id="4f089-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f089-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f089-104">Указывает состояние объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="4f089-104">Specifies the status of a **Field** object.</span></span>

<span data-ttu-id="4f089-105">\*\*AdFieldPending\* \*\* , то это означает операцию, которая вызвала состояние нужно задать и может использоваться в сочетании с другими значения состояния.</span><span class="sxs-lookup"><span data-stu-id="4f089-105">The **adFieldPending\*** values indicate the operation that caused the status to be set, and may be combined with other status values.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f089-106">Константа</span><span class="sxs-lookup"><span data-stu-id="4f089-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="4f089-107">Значение</span><span class="sxs-lookup"><span data-stu-id="4f089-107">Value</span></span></p></th>
<th><p><span data-ttu-id="4f089-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4f089-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f089-109"><strong>adFieldAlreadyExists</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-109"><strong>adFieldAlreadyExists</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-110">26</span><span class="sxs-lookup"><span data-stu-id="4f089-110">26</span></span></p></td>
<td><p><span data-ttu-id="4f089-111">Указывает, что указанного поля уже существует.</span><span class="sxs-lookup"><span data-stu-id="4f089-111">Indicates that the specified field already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-112"><strong>adFieldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-112"><strong>adFieldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-113">12</span><span class="sxs-lookup"><span data-stu-id="4f089-113">12</span></span></p></td>
<td><p><span data-ttu-id="4f089-114">Указывает, что значение недопустимый статус был отправлен ADO для поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4f089-114">Indicates that an invalid status value was sent from ADO to the OLE DB provider.</span></span> <span data-ttu-id="4f089-115">Возможные причины OLE DB 1.0 или 1.1 поставщика или неправильное сочетание <a href="value-property-ado.md">значения</a> и <a href="status-property-ado-field.md">состояние</a>.</span><span class="sxs-lookup"><span data-stu-id="4f089-115">Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <a href="value-property-ado.md">Value</a> and <a href="status-property-ado-field.md">Status</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-116"><strong>adFieldCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-116"><strong>adFieldCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-117">20</span><span class="sxs-lookup"><span data-stu-id="4f089-117">20</span></span></p></td>
<td><p><span data-ttu-id="4f089-118">Указывает, что сервер URL-адрес, указанный с <a href="source-property-ado-record.md">источника</a> не удалось завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="4f089-118">Indicates that the server of the URL specified by <a href="source-property-ado-record.md">Source</a> could not complete the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-119"><strong>adFieldCannotDeleteSource</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-119"><strong>adFieldCannotDeleteSource</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-120">23</span><span class="sxs-lookup"><span data-stu-id="4f089-120">23</span></span></p></td>
<td><p><span data-ttu-id="4f089-121">Указывает, что во время операции перемещения дерево или поддерево был перемещен в новое место, но не удалось удалить источник.</span><span class="sxs-lookup"><span data-stu-id="4f089-121">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-122"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-122"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-123">2</span><span class="sxs-lookup"><span data-stu-id="4f089-123">2</span></span></p></td>
<td><p><span data-ttu-id="4f089-124">Указывает поля извлекается или хранятся без потери данных.</span><span class="sxs-lookup"><span data-stu-id="4f089-124">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-125"><strong>adFieldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-125"><strong>adFieldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-126">7</span><span class="sxs-lookup"><span data-stu-id="4f089-126">7</span></span></p></td>
<td><p><span data-ttu-id="4f089-127">Указывает, что поле не удается добавить так как поставщик превысила ограничение (например, допустимое число полей).</span><span class="sxs-lookup"><span data-stu-id="4f089-127">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-128"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-128"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-129">6</span><span class="sxs-lookup"><span data-stu-id="4f089-129">6</span></span></p></td>
<td><p><span data-ttu-id="4f089-130">Указывает, что данные, возвращаемые от поставщика переполнена тип данных поля.</span><span class="sxs-lookup"><span data-stu-id="4f089-130">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-131"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-131"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-132">13</span><span class="sxs-lookup"><span data-stu-id="4f089-132">13</span></span></p></td>
<td><p><span data-ttu-id="4f089-133">Указывает, что значение по умолчанию для поля было использовано при задании данных.</span><span class="sxs-lookup"><span data-stu-id="4f089-133">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-134"><strong>adFieldDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-134"><strong>adFieldDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-135">16</span><span class="sxs-lookup"><span data-stu-id="4f089-135">16</span></span></p></td>
<td><p><span data-ttu-id="4f089-136">Указывает, что поле не существует.</span><span class="sxs-lookup"><span data-stu-id="4f089-136">Indicates that the field specified does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-137"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-137"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-138">15</span><span class="sxs-lookup"><span data-stu-id="4f089-138">15</span></span></p></td>
<td><p><span data-ttu-id="4f089-139">Указывает, что это поле была пропущена при значения параметра данных в источнике.</span><span class="sxs-lookup"><span data-stu-id="4f089-139">Indicates that this field was skipped when setting data values in the source.</span></span> <span data-ttu-id="4f089-140">Поставщик значение Нет.</span><span class="sxs-lookup"><span data-stu-id="4f089-140">The provider set no value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-141"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-141"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-142">10</span><span class="sxs-lookup"><span data-stu-id="4f089-142">10</span></span></p></td>
<td><p><span data-ttu-id="4f089-143">Указывает, что поле нельзя изменить, так как они вычисляемые или производные сущности.</span><span class="sxs-lookup"><span data-stu-id="4f089-143">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-144"><strong>adFieldInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-144"><strong>adFieldInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-145">17</span><span class="sxs-lookup"><span data-stu-id="4f089-145">17</span></span></p></td>
<td><p><span data-ttu-id="4f089-146">Указывает, что URL-адрес источника данных содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="4f089-146">Indicates that the data source URL contains invalid characters.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-147"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-147"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-148">3</span><span class="sxs-lookup"><span data-stu-id="4f089-148">3</span></span></p></td>
<td><p><span data-ttu-id="4f089-149">Указывает, что поставщик возвращаемое значение типа VARIANT типа VT_NULL и поле не является пустым.</span><span class="sxs-lookup"><span data-stu-id="4f089-149">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-150"><strong>adFieldOK</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-150"><strong>adFieldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-151">0</span><span class="sxs-lookup"><span data-stu-id="4f089-151">0</span></span></p></td>
<td><p><span data-ttu-id="4f089-152">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4f089-152">Default.</span></span> <span data-ttu-id="4f089-153">Указывает, что поле было успешно добавлено или удалено.</span><span class="sxs-lookup"><span data-stu-id="4f089-153">Indicates that the field was successfully added or deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-154"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-154"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-155">22</span><span class="sxs-lookup"><span data-stu-id="4f089-155">22</span></span></p></td>
<td><p><span data-ttu-id="4f089-156">Указывает, что поставщик не удается получить достаточно дискового пространства для выполнения перемещения или копирования операции.</span><span class="sxs-lookup"><span data-stu-id="4f089-156">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-157"><strong>adFieldPendingChange</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-157"><strong>adFieldPendingChange</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-158">0x40000</span><span class="sxs-lookup"><span data-stu-id="4f089-158">0x40000</span></span></p></td>
<td><p><span data-ttu-id="4f089-159">Указывает, что поле удаленного и затем повторно добавлена, возможно, с другой тип данных, либо, что значение поля, который ранее нахождения в состоянии adFieldOK был изменен.</span><span class="sxs-lookup"><span data-stu-id="4f089-159">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field that previously had a status of adFieldOK has changed.</span></span> <span data-ttu-id="4f089-160">После вызова метода <a href="update-method-ado.md">Update</a> окончательной форме поле будет изменять коллекции <a href="fields-collection-ado.md">полей</a> .</span><span class="sxs-lookup"><span data-stu-id="4f089-160">The final form of the field will modify the <a href="fields-collection-ado.md">Fields</a> collection after the <a href="update-method-ado.md">Update</a> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-161"><strong>adFieldPendingDelete</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-161"><strong>adFieldPendingDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-162">0x20000</span><span class="sxs-lookup"><span data-stu-id="4f089-162">0x20000</span></span></p></td>
<td><p><span data-ttu-id="4f089-163">Указывает, что операция <strong>удаления</strong> привело состояние должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="4f089-163">Indicates that the <strong>Delete</strong> operation caused the status to be set.</span></span> <span data-ttu-id="4f089-164">Поле был помечен для удаления из коллекции <strong>полей</strong> после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="4f089-164">The field has been marked for deletion from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-165"><strong>adFieldPendingInsert</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-165"><strong>adFieldPendingInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-166">0x10000</span><span class="sxs-lookup"><span data-stu-id="4f089-166">0x10000</span></span></p></td>
<td><p><span data-ttu-id="4f089-167">Указывает, что операции <strong>добавления</strong> привело состояние должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="4f089-167">Indicates that the <strong>Append</strong> operation caused the status to be set.</span></span> <span data-ttu-id="4f089-168">В <strong>поле</strong> был помечен для добавления в коллекцию <strong>полей</strong> после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="4f089-168">The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-169"><strong>adFieldPendingUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-169"><strong>adFieldPendingUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-170">0x80000</span><span class="sxs-lookup"><span data-stu-id="4f089-170">0x80000</span></span></p></td>
<td><p><span data-ttu-id="4f089-171">Указывает, что поставщик может определить, какие вызвало поле Состояние операции должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="4f089-171">Indicates that the provider cannot determine what operation caused field status to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-172"><strong>adFieldPendingUnknownDelete</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-172"><strong>adFieldPendingUnknownDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-173">0x100000</span><span class="sxs-lookup"><span data-stu-id="4f089-173">0x100000</span></span></p></td>
<td><p><span data-ttu-id="4f089-174">Указывает, что поставщик не может определить, какие операции, возникающие состояние поля должно быть задано и что поля будут удалены из коллекции <strong>полей</strong> , после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="4f089-174">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-175"><strong>adFieldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-175"><strong>adFieldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-176">9</span><span class="sxs-lookup"><span data-stu-id="4f089-176">9</span></span></p></td>
<td><p><span data-ttu-id="4f089-177">Указывает, что поле нельзя изменить, так как оно определяется только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4f089-177">Indicates that the field cannot be modified because it is defined as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-178"><strong>adFieldReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-178"><strong>adFieldReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-179">24</span><span class="sxs-lookup"><span data-stu-id="4f089-179">24</span></span></p></td>
<td><p><span data-ttu-id="4f089-180">Указывает, что поля в источнике данных только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4f089-180">Indicates that the field in the data source is defined as read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-181"><strong>adFieldResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-181"><strong>adFieldResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-182">19</span><span class="sxs-lookup"><span data-stu-id="4f089-182">19</span></span></p></td>
<td><p><span data-ttu-id="4f089-183">Указывает, что поставщик не удалось выполнить операцию, поскольку объект уже существует в URL-адрес конечного и не удается перезаписать объекта.</span><span class="sxs-lookup"><span data-stu-id="4f089-183">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-184"><strong>adFieldResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-184"><strong>adFieldResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-185">18</span><span class="sxs-lookup"><span data-stu-id="4f089-185">18</span></span></p></td>
<td><p><span data-ttu-id="4f089-186">Указывает, что поставщик не удалось выполнить операцию, так как источник данных заблокирован один или несколько других приложений или процессом.</span><span class="sxs-lookup"><span data-stu-id="4f089-186">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-187"><strong>adFieldResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-187"><strong>adFieldResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-188">25</span><span class="sxs-lookup"><span data-stu-id="4f089-188">25</span></span></p></td>
<td><p><span data-ttu-id="4f089-189">Указывает, что URL-адрес источника и назначения выходят за рамки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="4f089-189">Indicates that a source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-190"><strong>adFieldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-190"><strong>adFieldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-191">11</span><span class="sxs-lookup"><span data-stu-id="4f089-191">11</span></span></p></td>
<td><p><span data-ttu-id="4f089-192">Указывает, что значение нарушает ограничения схемы источника данных для поля.</span><span class="sxs-lookup"><span data-stu-id="4f089-192">Indicates that the value violated the data source schema constraint for the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-193"><strong>adFieldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-193"><strong>adFieldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-194">5</span><span class="sxs-lookup"><span data-stu-id="4f089-194">5</span></span></p></td>
<td><p><span data-ttu-id="4f089-195">Указывает, что подписанных данных значение, возвращаемое поставщиком, но тип данных значения поля ADO не был подписан.</span><span class="sxs-lookup"><span data-stu-id="4f089-195">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-196"><strong>adFieldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-196"><strong>adFieldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-197">4</span><span class="sxs-lookup"><span data-stu-id="4f089-197">4</span></span></p></td>
<td><p><span data-ttu-id="4f089-198">Указывает, что данные переменной длины усечено при чтении из источника данных.</span><span class="sxs-lookup"><span data-stu-id="4f089-198">Indicates that variable-length data was truncated when reading from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f089-199"><strong>adFieldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-199"><strong>adFieldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-200">8</span><span class="sxs-lookup"><span data-stu-id="4f089-200">8</span></span></p></td>
<td><p><span data-ttu-id="4f089-201">Указывает, что поставщик не удается определить значение при чтении из источника данных.</span><span class="sxs-lookup"><span data-stu-id="4f089-201">Indicates that the provider could not determine the value when reading from the data source.</span></span> <span data-ttu-id="4f089-202">Например строку только что был создан, значение по умолчанию для столбца были недоступны и новое значение было еще не был указан.</span><span class="sxs-lookup"><span data-stu-id="4f089-202">For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f089-203"><strong>adFieldVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="4f089-203"><strong>adFieldVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="4f089-204">21</span><span class="sxs-lookup"><span data-stu-id="4f089-204">21</span></span></p></td>
<td><p><span data-ttu-id="4f089-205">Указывает, что поставщик не удается найти тома хранилища, указанный в параметре URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4f089-205">Indicates that the provider is unable to locate the storage volume indicated by the URL.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4f089-206">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="4f089-206">ADO/WFC equivalent</span></span>

<span data-ttu-id="4f089-207">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="4f089-207">These constants do not have ADO/WFC equivalents.</span></span>

