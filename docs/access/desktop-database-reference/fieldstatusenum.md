---
title: Фиелдстатусенум (Справочник по базам данных Access на компьютере)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ccf98f2a740e2a077d6e2451102bfc72bcd1b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292519"
---
# <a name="fieldstatusenum"></a><span data-ttu-id="5908a-102">FieldStatusEnum</span><span class="sxs-lookup"><span data-stu-id="5908a-102">FieldStatusEnum</span></span>

<span data-ttu-id="5908a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5908a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5908a-104">Задает состояние объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="5908a-104">Specifies the status of a **Field** object.</span></span>

<span data-ttu-id="5908a-105">Значения \*\*адфиелдпендинг\* \*\* указывают операцию, вызвавшую Задание состояния, и могут быть объединены с другими значениями состояния.</span><span class="sxs-lookup"><span data-stu-id="5908a-105">The **adFieldPending\*** values indicate the operation that caused the status to be set, and may be combined with other status values.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5908a-106">Константа</span><span class="sxs-lookup"><span data-stu-id="5908a-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="5908a-107">Значение</span><span class="sxs-lookup"><span data-stu-id="5908a-107">Value</span></span></p></th>
<th><p><span data-ttu-id="5908a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5908a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5908a-109"><strong>адфиелдалреадексистс</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-109"><strong>adFieldAlreadyExists</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-110">26</span><span class="sxs-lookup"><span data-stu-id="5908a-110">26</span></span></p></td>
<td><p><span data-ttu-id="5908a-111">Указывает, что указанное поле уже существует.</span><span class="sxs-lookup"><span data-stu-id="5908a-111">Indicates that the specified field already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-112"><strong>адфиелдбадстатус</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-112"><strong>adFieldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-113">12 </span><span class="sxs-lookup"><span data-stu-id="5908a-113">12</span></span></p></td>
<td><p><span data-ttu-id="5908a-114">Указывает, что от ADO до поставщика OLE DB было передано недопустимое значение Status.</span><span class="sxs-lookup"><span data-stu-id="5908a-114">Indicates that an invalid status value was sent from ADO to the OLE DB provider.</span></span> <span data-ttu-id="5908a-115">Возможные причины: поставщик OLE DB 1,0 или 1,1 или неправильное сочетание <a href="value-property-ado.md">значения</a> и <a href="status-property-ado-field.md">состояния</a>.</span><span class="sxs-lookup"><span data-stu-id="5908a-115">Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <a href="value-property-ado.md">Value</a> and <a href="status-property-ado-field.md">Status</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-116"><strong>адфиелдканноткомплете</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-116"><strong>adFieldCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-117">двадцать</span><span class="sxs-lookup"><span data-stu-id="5908a-117">20</span></span></p></td>
<td><p><span data-ttu-id="5908a-118">Указывает, что сервер с URL-адресом, указанным в параметре <a href="source-property-ado-record.md">Source</a> , не смог выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="5908a-118">Indicates that the server of the URL specified by <a href="source-property-ado-record.md">Source</a> could not complete the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-119"><strong>адфиелдканнотделетесаурце</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-119"><strong>adFieldCannotDeleteSource</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-120">23</span><span class="sxs-lookup"><span data-stu-id="5908a-120">23</span></span></p></td>
<td><p><span data-ttu-id="5908a-121">Указывает, что во время операции перемещения дерево или поддерево были перемещены в новое расположение, но источник не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="5908a-121">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-122"><strong>адфиелдкантконвертвалуе</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-122"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-123">2</span><span class="sxs-lookup"><span data-stu-id="5908a-123">2</span></span></p></td>
<td><p><span data-ttu-id="5908a-124">Указывает, что поле невозможно извлечь или сохранить без потери данных.</span><span class="sxs-lookup"><span data-stu-id="5908a-124">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-125"><strong>адфиелдканткреате</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-125"><strong>adFieldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-126">7 </span><span class="sxs-lookup"><span data-stu-id="5908a-126">7</span></span></p></td>
<td><p><span data-ttu-id="5908a-127">Указывает, что не удалось добавить поле, так как поставщик превысил ограничение (например, число полей разрешено).</span><span class="sxs-lookup"><span data-stu-id="5908a-127">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-128"><strong>адфиелддатаоверфлов</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-128"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-129">6 </span><span class="sxs-lookup"><span data-stu-id="5908a-129">6</span></span></p></td>
<td><p><span data-ttu-id="5908a-130">Указывает, что данные, возвращенные поставщиком, переполняет тип данных поля.</span><span class="sxs-lookup"><span data-stu-id="5908a-130">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-131"><strong>адфиелддефаулт</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-131"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-132">13</span><span class="sxs-lookup"><span data-stu-id="5908a-132">13</span></span></p></td>
<td><p><span data-ttu-id="5908a-133">Указывает, что при задании данных использовалось значение поля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5908a-133">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-134"><strong>адфиелддоеснотексист</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-134"><strong>adFieldDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-135">16 </span><span class="sxs-lookup"><span data-stu-id="5908a-135">16</span></span></p></td>
<td><p><span data-ttu-id="5908a-136">Указывает, что указанное поле не существует.</span><span class="sxs-lookup"><span data-stu-id="5908a-136">Indicates that the field specified does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-137"><strong>адфиелдигноре</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-137"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-138">15 </span><span class="sxs-lookup"><span data-stu-id="5908a-138">15</span></span></p></td>
<td><p><span data-ttu-id="5908a-139">Указывает, что это поле было пропущено при задании значений данных в источнике.</span><span class="sxs-lookup"><span data-stu-id="5908a-139">Indicates that this field was skipped when setting data values in the source.</span></span> <span data-ttu-id="5908a-140">Поставщик не задает значение.</span><span class="sxs-lookup"><span data-stu-id="5908a-140">The provider set no value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-141"><strong>адфиелдинтегритивиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-141"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-142">10 </span><span class="sxs-lookup"><span data-stu-id="5908a-142">10</span></span></p></td>
<td><p><span data-ttu-id="5908a-143">Указывает, что поле невозможно изменить, так как это вычисляемая или производная сущность.</span><span class="sxs-lookup"><span data-stu-id="5908a-143">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-144"><strong>адфиелдинвалидурл</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-144"><strong>adFieldInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-145">17 </span><span class="sxs-lookup"><span data-stu-id="5908a-145">17</span></span></p></td>
<td><p><span data-ttu-id="5908a-146">Указывает, что URL-адрес источника данных содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="5908a-146">Indicates that the data source URL contains invalid characters.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-147"><strong>адфиелдиснулл</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-147"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-148">4</span><span class="sxs-lookup"><span data-stu-id="5908a-148">3</span></span></p></td>
<td><p><span data-ttu-id="5908a-149">Указывает, что поставщик возвратил значение VARIANT типа VT_NULL, а поле не пустое.</span><span class="sxs-lookup"><span data-stu-id="5908a-149">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-150"><strong>адфиелдок</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-150"><strong>adFieldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-151">нуль</span><span class="sxs-lookup"><span data-stu-id="5908a-151">0</span></span></p></td>
<td><p><span data-ttu-id="5908a-152">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5908a-152">Default.</span></span> <span data-ttu-id="5908a-153">Указывает, что поле было успешно добавлено или удалено.</span><span class="sxs-lookup"><span data-stu-id="5908a-153">Indicates that the field was successfully added or deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-154"><strong>адфиелдаутофспаце</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-154"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-155">22</span><span class="sxs-lookup"><span data-stu-id="5908a-155">22</span></span></p></td>
<td><p><span data-ttu-id="5908a-156">Указывает, что поставщик не может получить достаточно места для выполнения операции перемещения или копирования.</span><span class="sxs-lookup"><span data-stu-id="5908a-156">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-157"><strong>адфиелдпендингчанже</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-157"><strong>adFieldPendingChange</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-158">0x40000</span><span class="sxs-lookup"><span data-stu-id="5908a-158">0x40000</span></span></p></td>
<td><p><span data-ttu-id="5908a-159">Указывает, что поле было удалено, а затем повторно Добавлено, возможно, с другим типом данных, или что значение поля, для которого ранее было изменено состояние Адфиелдок.</span><span class="sxs-lookup"><span data-stu-id="5908a-159">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field that previously had a status of adFieldOK has changed.</span></span> <span data-ttu-id="5908a-160">Последняя форма поля изменит коллекцию <a href="fields-collection-ado.md">Fields</a> после вызова метода <a href="update-method-ado.md">Update</a> .</span><span class="sxs-lookup"><span data-stu-id="5908a-160">The final form of the field will modify the <a href="fields-collection-ado.md">Fields</a> collection after the <a href="update-method-ado.md">Update</a> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-161"><strong>адфиелдпендингделете</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-161"><strong>adFieldPendingDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-162">0x20000</span><span class="sxs-lookup"><span data-stu-id="5908a-162">0x20000</span></span></p></td>
<td><p><span data-ttu-id="5908a-163">Указывает, что операция <strong>удаления</strong> привела к заданию состояния.</span><span class="sxs-lookup"><span data-stu-id="5908a-163">Indicates that the <strong>Delete</strong> operation caused the status to be set.</span></span> <span data-ttu-id="5908a-164">Поле помечено для удаления из коллекции <strong>Fields</strong> после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="5908a-164">The field has been marked for deletion from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-165"><strong>адфиелдпендингинсерт</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-165"><strong>adFieldPendingInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-166">0x10000</span><span class="sxs-lookup"><span data-stu-id="5908a-166">0x10000</span></span></p></td>
<td><p><span data-ttu-id="5908a-167">Указывает, что операция <strong>append</strong> привела к заданию состояния.</span><span class="sxs-lookup"><span data-stu-id="5908a-167">Indicates that the <strong>Append</strong> operation caused the status to be set.</span></span> <span data-ttu-id="5908a-168"><strong>Поле</strong> помечено для добавления в коллекцию <strong>Fields</strong> после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="5908a-168">The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-169"><strong>адфиелдпендингункновн</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-169"><strong>adFieldPendingUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-170">0x80000</span><span class="sxs-lookup"><span data-stu-id="5908a-170">0x80000</span></span></p></td>
<td><p><span data-ttu-id="5908a-171">Указывает, что поставщик не может определить, какая операция привела к заданию состояния поля.</span><span class="sxs-lookup"><span data-stu-id="5908a-171">Indicates that the provider cannot determine what operation caused field status to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-172"><strong>адфиелдпендингункновнделете</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-172"><strong>adFieldPendingUnknownDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-173">0x100000</span><span class="sxs-lookup"><span data-stu-id="5908a-173">0x100000</span></span></p></td>
<td><p><span data-ttu-id="5908a-174">Указывает, что поставщик не может определить, какая операция привела к заданию состояния поля, и что это поле будет удалено из коллекции <strong>Fields</strong> после вызова метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="5908a-174">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-175"><strong>адфиелдпермиссиондениед</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-175"><strong>adFieldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-176">9 </span><span class="sxs-lookup"><span data-stu-id="5908a-176">9</span></span></p></td>
<td><p><span data-ttu-id="5908a-177">Указывает, что поле невозможно изменить, так как оно определено как доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5908a-177">Indicates that the field cannot be modified because it is defined as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-178"><strong>адфиелдреадонли</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-178"><strong>adFieldReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-179">открыт</span><span class="sxs-lookup"><span data-stu-id="5908a-179">24</span></span></p></td>
<td><p><span data-ttu-id="5908a-180">Указывает, что поле в источнике данных определено как доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5908a-180">Indicates that the field in the data source is defined as read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-181"><strong>адфиелдресаурцеексистс</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-181"><strong>adFieldResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-182">19</span><span class="sxs-lookup"><span data-stu-id="5908a-182">19</span></span></p></td>
<td><p><span data-ttu-id="5908a-183">Указывает, что поставщик не смог выполнить операцию, так как объект уже существует в целевом URL-адресе и не может перезаписать объект.</span><span class="sxs-lookup"><span data-stu-id="5908a-183">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-184"><strong>адфиелдресаурцелоккед</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-184"><strong>adFieldResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-185">18 </span><span class="sxs-lookup"><span data-stu-id="5908a-185">18</span></span></p></td>
<td><p><span data-ttu-id="5908a-186">Указывает, что поставщик не смог выполнить операцию, так как источник данных заблокирован одним или несколькими другими приложениями или процессами.</span><span class="sxs-lookup"><span data-stu-id="5908a-186">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-187"><strong>адфиелдресаурцеаутофскопе</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-187"><strong>adFieldResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-188">25</span><span class="sxs-lookup"><span data-stu-id="5908a-188">25</span></span></p></td>
<td><p><span data-ttu-id="5908a-189">Указывает, что исходный или конечный URL-адрес находится вне области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="5908a-189">Indicates that a source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-190"><strong>адфиелдсчемавиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-190"><strong>adFieldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-191">11 </span><span class="sxs-lookup"><span data-stu-id="5908a-191">11</span></span></p></td>
<td><p><span data-ttu-id="5908a-192">Указывает, что значение противоречит ограничению схемы источника данных для поля.</span><span class="sxs-lookup"><span data-stu-id="5908a-192">Indicates that the value violated the data source schema constraint for the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-193"><strong>адфиелдсигнмисматч</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-193"><strong>adFieldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-194">5 </span><span class="sxs-lookup"><span data-stu-id="5908a-194">5</span></span></p></td>
<td><p><span data-ttu-id="5908a-195">Указывает, что значение данных, возвращаемое поставщиком, было подписано, но тип данных значения поля ADO не подписан.</span><span class="sxs-lookup"><span data-stu-id="5908a-195">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-196"><strong>адфиелдтрункатед</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-196"><strong>adFieldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-197">4 </span><span class="sxs-lookup"><span data-stu-id="5908a-197">4</span></span></p></td>
<td><p><span data-ttu-id="5908a-198">Указывает, что данные переменной длины были усечены при чтении из источника данных.</span><span class="sxs-lookup"><span data-stu-id="5908a-198">Indicates that variable-length data was truncated when reading from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5908a-199"><strong>адфиелдунаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-199"><strong>adFieldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-200">8 </span><span class="sxs-lookup"><span data-stu-id="5908a-200">8</span></span></p></td>
<td><p><span data-ttu-id="5908a-201">Указывает, что поставщик не может определить значение при чтении из источника данных.</span><span class="sxs-lookup"><span data-stu-id="5908a-201">Indicates that the provider could not determine the value when reading from the data source.</span></span> <span data-ttu-id="5908a-202">Например, строка была только что создана, значение столбца по умолчанию было недоступно, а еще не было указано новое значение.</span><span class="sxs-lookup"><span data-stu-id="5908a-202">For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5908a-203"><strong>адфиелдволуменотфаунд</strong></span><span class="sxs-lookup"><span data-stu-id="5908a-203"><strong>adFieldVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="5908a-204">21</span><span class="sxs-lookup"><span data-stu-id="5908a-204">21</span></span></p></td>
<td><p><span data-ttu-id="5908a-205">Указывает, что поставщик не может определить объем хранилища, указанный по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="5908a-205">Indicates that the provider is unable to locate the storage volume indicated by the URL.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="5908a-206">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="5908a-206">ADO/WFC equivalent</span></span>

<span data-ttu-id="5908a-207">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="5908a-207">These constants do not have ADO/WFC equivalents.</span></span>

