---
title: FieldStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e5c7ecb345c993b2582ce6971044d325afca857a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482997"
---
# <a name="fieldstatusenum"></a><span data-ttu-id="72e69-102">FieldStatusEnum</span><span class="sxs-lookup"><span data-stu-id="72e69-102">FieldStatusEnum</span></span>


<span data-ttu-id="72e69-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="72e69-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72e69-104">Указывает состояние объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="72e69-104">Specifies the status of a **Field** object.</span></span>

<span data-ttu-id="72e69-105">\*\*AdFieldPending\* \*\* , то это означает операцию, которая вызвала состояние нужно задать и может использоваться в сочетании с другими значения состояния.</span><span class="sxs-lookup"><span data-stu-id="72e69-105">The **adFieldPending\*** values indicate the operation that caused the status to be set, and may be combined with other status values.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72e69-106">Константа</span><span class="sxs-lookup"><span data-stu-id="72e69-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="72e69-107">Значение</span><span class="sxs-lookup"><span data-stu-id="72e69-107">Value</span></span></p></th>
<th><p><span data-ttu-id="72e69-108">Описание</span><span class="sxs-lookup"><span data-stu-id="72e69-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72e69-109"><strong>adFieldAlreadyExists</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-109"><strong>adFieldAlreadyExists</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-110">26</span><span class="sxs-lookup"><span data-stu-id="72e69-110">26</span></span></p></td>
<td><p><span data-ttu-id="72e69-111">Указывает, что указанного поля уже существует.</span><span class="sxs-lookup"><span data-stu-id="72e69-111">Indicates that the specified field already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-112"><strong>adFieldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-112"><strong>adFieldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-113">12</span><span class="sxs-lookup"><span data-stu-id="72e69-113">12</span></span></p></td>
<td><p><span data-ttu-id="72e69-114">Указывает, что значение недопустимый статус был отправлен ADO для поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="72e69-114">Indicates that an invalid status value was sent from ADO to the OLE DB provider.</span></span> <span data-ttu-id="72e69-115">Возможные причины OLE DB 1.0 или 1.1 поставщика или неправильное сочетание <a href="value-property-ado.md">значения</a> и <a href="status-property-ado-field.md">состояние</a>.</span><span class="sxs-lookup"><span data-stu-id="72e69-115">Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <a href="value-property-ado.md">Value</a> and <a href="status-property-ado-field.md">Status</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-116"><strong>adFieldCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-116"><strong>adFieldCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-117">20</span><span class="sxs-lookup"><span data-stu-id="72e69-117">20</span></span></p></td>
<td><p><span data-ttu-id="72e69-118">Указывает, что сервер URL-адрес, указанный с <a href="source-property-ado-record.md">источника</a> не удалось завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="72e69-118">Indicates that the server of the URL specified by <a href="source-property-ado-record.md">Source</a> could not complete the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-119"><strong>adFieldCannotDeleteSource</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-119"><strong>adFieldCannotDeleteSource</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-120">23</span><span class="sxs-lookup"><span data-stu-id="72e69-120">23</span></span></p></td>
<td><p><span data-ttu-id="72e69-121">Указывает, что во время операции перемещения дерево или поддерево был перемещен в новое место, но не удалось удалить источник.</span><span class="sxs-lookup"><span data-stu-id="72e69-121">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-122"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-122"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-123">2</span><span class="sxs-lookup"><span data-stu-id="72e69-123">2</span></span></p></td>
<td><p><span data-ttu-id="72e69-124">Указывает поля извлекается или хранятся без потери данных.</span><span class="sxs-lookup"><span data-stu-id="72e69-124">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-125"><strong>adFieldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-125"><strong>adFieldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-126">7</span><span class="sxs-lookup"><span data-stu-id="72e69-126">7</span></span></p></td>
<td><p><span data-ttu-id="72e69-127">Указывает, что поле не удается добавить так как поставщик превысила ограничение (например, допустимое число полей).</span><span class="sxs-lookup"><span data-stu-id="72e69-127">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-128"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-128"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-129">6</span><span class="sxs-lookup"><span data-stu-id="72e69-129">6</span></span></p></td>
<td><p><span data-ttu-id="72e69-130">Указывает, что данные, возвращаемые от поставщика переполнена тип данных поля.</span><span class="sxs-lookup"><span data-stu-id="72e69-130">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-131"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-131"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-132">13</span><span class="sxs-lookup"><span data-stu-id="72e69-132">13</span></span></p></td>
<td><p><span data-ttu-id="72e69-133">Указывает, что значение по умолчанию для поля было использовано при задании данных.</span><span class="sxs-lookup"><span data-stu-id="72e69-133">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-134"><strong>adFieldDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-134"><strong>adFieldDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-135">16</span><span class="sxs-lookup"><span data-stu-id="72e69-135">16</span></span></p></td>
<td><p><span data-ttu-id="72e69-136">Указывает, что поле не существует.</span><span class="sxs-lookup"><span data-stu-id="72e69-136">Indicates that the field specified does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-137"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-137"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-138">15</span><span class="sxs-lookup"><span data-stu-id="72e69-138">15</span></span></p></td>
<td><p><span data-ttu-id="72e69-139">Указывает, что это поле была пропущена при значения параметра данных в источнике.</span><span class="sxs-lookup"><span data-stu-id="72e69-139">Indicates that this field was skipped when setting data values in the source.</span></span> <span data-ttu-id="72e69-140">Поставщик значение Нет.</span><span class="sxs-lookup"><span data-stu-id="72e69-140">The provider set no value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-141"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-141"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-142">10</span><span class="sxs-lookup"><span data-stu-id="72e69-142">10</span></span></p></td>
<td><p><span data-ttu-id="72e69-143">Указывает, что поле нельзя изменить, так как они вычисляемые или производные сущности.</span><span class="sxs-lookup"><span data-stu-id="72e69-143">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-144"><strong>adFieldInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-144"><strong>adFieldInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-145">17</span><span class="sxs-lookup"><span data-stu-id="72e69-145">17</span></span></p></td>
<td><p><span data-ttu-id="72e69-146">Указывает, что URL-адрес источника данных содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="72e69-146">Indicates that the data source URL contains invalid characters.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-147"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-147"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-148">3</span><span class="sxs-lookup"><span data-stu-id="72e69-148">3</span></span></p></td>
<td><p><span data-ttu-id="72e69-149">Указывает, что поставщик возвращаемое значение типа VARIANT типа VT_NULL и поле не является пустым.</span><span class="sxs-lookup"><span data-stu-id="72e69-149">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-150"><strong>adFieldOK</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-150"><strong>adFieldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-151">0</span><span class="sxs-lookup"><span data-stu-id="72e69-151">0</span></span></p></td>
<td><p><span data-ttu-id="72e69-152">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="72e69-152">Default.</span></span> <span data-ttu-id="72e69-153">Указывает, что поле было успешно добавлено или удалено.</span><span class="sxs-lookup"><span data-stu-id="72e69-153">Indicates that the field was successfully added or deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-154"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-154"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-155">22</span><span class="sxs-lookup"><span data-stu-id="72e69-155">22</span></span></p></td>
<td><p><span data-ttu-id="72e69-156">Указывает, что поставщик не удается получить достаточно дискового пространства для выполнения перемещения или копирования операции.</span><span class="sxs-lookup"><span data-stu-id="72e69-156">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-157"><strong>adFieldPendingChange</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-157"><strong>adFieldPendingChange</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-158">0x40000</span><span class="sxs-lookup"><span data-stu-id="72e69-158">0x40000</span></span></p></td>
<td><p><span data-ttu-id="72e69-159">Указывает, что поле удаленного и затем повторно добавлена, возможно, с другой тип данных, либо, что значение поля, который ранее нахождения в состоянии adFieldOK был изменен.</span><span class="sxs-lookup"><span data-stu-id="72e69-159">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field that previously had a status of adFieldOK has changed.</span></span> <span data-ttu-id="72e69-160">После вызова метода <a href="update-method-ado.md">Update</a> окончательной форме поле будет изменять коллекции <a href="fields-collection-ado.md">полей</a> .</span><span class="sxs-lookup"><span data-stu-id="72e69-160">The final form of the field will modify the <a href="fields-collection-ado.md">Fields</a> collection after the <a href="update-method-ado.md">Update</a> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-161"><strong>adFieldPendingDelete</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-161"><strong>adFieldPendingDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-162">0x20000</span><span class="sxs-lookup"><span data-stu-id="72e69-162">0x20000</span></span></p></td>
<td><p><span data-ttu-id="72e69-163">Указывает, что операция <strong>удаления</strong> привело состояние должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="72e69-163">Indicates that the <strong>Delete</strong> operation caused the status to be set.</span></span> <span data-ttu-id="72e69-164">Поле был помечен для удаления из коллекции <strong>полей</strong> после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="72e69-164">The field has been marked for deletion from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-165"><strong>adFieldPendingInsert</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-165"><strong>adFieldPendingInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-166">0x10000</span><span class="sxs-lookup"><span data-stu-id="72e69-166">0x10000</span></span></p></td>
<td><p><span data-ttu-id="72e69-167">Указывает, что операции <strong>добавления</strong> привело состояние должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="72e69-167">Indicates that the <strong>Append</strong> operation caused the status to be set.</span></span> <span data-ttu-id="72e69-168">В <strong>поле</strong> был помечен для добавления в коллекцию <strong>полей</strong> после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="72e69-168">The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-169"><strong>adFieldPendingUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-169"><strong>adFieldPendingUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-170">0x80000</span><span class="sxs-lookup"><span data-stu-id="72e69-170">0x80000</span></span></p></td>
<td><p><span data-ttu-id="72e69-171">Указывает, что поставщик может определить, какие вызвало поле Состояние операции должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="72e69-171">Indicates that the provider cannot determine what operation caused field status to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-172"><strong>adFieldPendingUnknownDelete</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-172"><strong>adFieldPendingUnknownDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-173">0x100000</span><span class="sxs-lookup"><span data-stu-id="72e69-173">0x100000</span></span></p></td>
<td><p><span data-ttu-id="72e69-174">Указывает, что поставщик не может определить, какие операции, возникающие состояние поля должно быть задано и что поля будут удалены из коллекции <strong>полей</strong> , после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="72e69-174">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-175"><strong>adFieldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-175"><strong>adFieldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-176">9</span><span class="sxs-lookup"><span data-stu-id="72e69-176">9</span></span></p></td>
<td><p><span data-ttu-id="72e69-177">Указывает, что поле нельзя изменить, так как оно определяется только для чтения.</span><span class="sxs-lookup"><span data-stu-id="72e69-177">Indicates that the field cannot be modified because it is defined as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-178"><strong>adFieldReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-178"><strong>adFieldReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-179">24</span><span class="sxs-lookup"><span data-stu-id="72e69-179">24</span></span></p></td>
<td><p><span data-ttu-id="72e69-180">Указывает, что поля в источнике данных только для чтения.</span><span class="sxs-lookup"><span data-stu-id="72e69-180">Indicates that the field in the data source is defined as read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-181"><strong>adFieldResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-181"><strong>adFieldResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-182">19</span><span class="sxs-lookup"><span data-stu-id="72e69-182">19</span></span></p></td>
<td><p><span data-ttu-id="72e69-183">Указывает, что поставщик не удалось выполнить операцию, поскольку объект уже существует в URL-адрес конечного и не удается перезаписать объекта.</span><span class="sxs-lookup"><span data-stu-id="72e69-183">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-184"><strong>adFieldResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-184"><strong>adFieldResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-185">18</span><span class="sxs-lookup"><span data-stu-id="72e69-185">18</span></span></p></td>
<td><p><span data-ttu-id="72e69-186">Указывает, что поставщик не удалось выполнить операцию, так как источник данных заблокирован один или несколько других приложений или процессом.</span><span class="sxs-lookup"><span data-stu-id="72e69-186">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-187"><strong>adFieldResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-187"><strong>adFieldResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-188">25</span><span class="sxs-lookup"><span data-stu-id="72e69-188">25</span></span></p></td>
<td><p><span data-ttu-id="72e69-189">Указывает, что URL-адрес источника и назначения выходят за рамки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="72e69-189">Indicates that a source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-190"><strong>adFieldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-190"><strong>adFieldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-191">11</span><span class="sxs-lookup"><span data-stu-id="72e69-191">11</span></span></p></td>
<td><p><span data-ttu-id="72e69-192">Указывает, что значение нарушает ограничения схемы источника данных для поля.</span><span class="sxs-lookup"><span data-stu-id="72e69-192">Indicates that the value violated the data source schema constraint for the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-193"><strong>adFieldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-193"><strong>adFieldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-194">5</span><span class="sxs-lookup"><span data-stu-id="72e69-194">5</span></span></p></td>
<td><p><span data-ttu-id="72e69-195">Указывает, что подписанных данных значение, возвращаемое поставщиком, но тип данных значения поля ADO не был подписан.</span><span class="sxs-lookup"><span data-stu-id="72e69-195">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-196"><strong>adFieldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-196"><strong>adFieldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-197">4</span><span class="sxs-lookup"><span data-stu-id="72e69-197">4</span></span></p></td>
<td><p><span data-ttu-id="72e69-198">Указывает, что данные переменной длины усечено при чтении из источника данных.</span><span class="sxs-lookup"><span data-stu-id="72e69-198">Indicates that variable-length data was truncated when reading from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e69-199"><strong>adFieldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-199"><strong>adFieldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-200">8</span><span class="sxs-lookup"><span data-stu-id="72e69-200">8</span></span></p></td>
<td><p><span data-ttu-id="72e69-201">Указывает, что поставщик не удается определить значение при чтении из источника данных.</span><span class="sxs-lookup"><span data-stu-id="72e69-201">Indicates that the provider could not determine the value when reading from the data source.</span></span> <span data-ttu-id="72e69-202">Например строку только что был создан, значение по умолчанию для столбца были недоступны и новое значение было еще не был указан.</span><span class="sxs-lookup"><span data-stu-id="72e69-202">For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e69-203"><strong>adFieldVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="72e69-203"><strong>adFieldVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="72e69-204">21</span><span class="sxs-lookup"><span data-stu-id="72e69-204">21</span></span></p></td>
<td><p><span data-ttu-id="72e69-205">Указывает, что поставщик не удается найти тома хранилища, указанный в параметре URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="72e69-205">Indicates that the provider is unable to locate the storage volume indicated by the URL.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72e69-206">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="72e69-206">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="72e69-207">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="72e69-207">These constants do not have ADO/WFC equivalents.</span></span>

