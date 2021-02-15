---
title: Справочник по ошибкам ADO
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a7f756af1422588d99fcffe1ae1413422131b70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283396"
---
# <a name="ado-error-reference"></a><span data-ttu-id="e6617-102">Справочник по ошибкам ADO</span><span class="sxs-lookup"><span data-stu-id="e6617-102">ADO error reference</span></span>

<span data-ttu-id="e6617-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6617-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6617-104">**Константа ErrorValueEnum** описывает значения ошибок ADO.</span><span class="sxs-lookup"><span data-stu-id="e6617-104">The **ErrorValueEnum** constant describes the ADO error values.</span></span> <span data-ttu-id="e6617-105">Полный список этих перечисляемых констант, включая значения, см. в приложении [Б. Ошибки ADO.](appendix-b-ado-errors.md)</span><span class="sxs-lookup"><span data-stu-id="e6617-105">For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md).</span></span> <span data-ttu-id="e6617-106">В этом разделе рассматриваются некоторые наиболее интересные ошибки и поясняются некоторые конкретные ситуации, которые могут их привести, или решения для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="e6617-106">This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem.</span></span> <span data-ttu-id="e6617-107">В **списке указаны как константа ErrorValueEnum,** так и короткое положительное десятичность.</span><span class="sxs-lookup"><span data-stu-id="e6617-107">Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6617-108">Числовой</span><span class="sxs-lookup"><span data-stu-id="e6617-108">Number</span></span></p></th>
<th><p><span data-ttu-id="e6617-109">Константа ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="e6617-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="e6617-110">Описание/Возможные причины</span><span class="sxs-lookup"><span data-stu-id="e6617-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6617-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-112"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-113">Поставщику не удалось выполнить запрашиваемую операцию.</span><span class="sxs-lookup"><span data-stu-id="e6617-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-115"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-116">Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="e6617-116">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span> <span data-ttu-id="e6617-117">Эта ошибка часто вызвана опечаткой в SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="e6617-117">This error is often caused by a typographical error in an SQL SELECT statement.</span></span> <span data-ttu-id="e6617-118">Например, эта ошибка может быть опечатка имени поля или таблицы.</span><span class="sxs-lookup"><span data-stu-id="e6617-118">For example, a misspelled field name or table name can generate this error.</span></span> <span data-ttu-id="e6617-119">Эта ошибка также может возникать, если поле или таблица, именуемая в заявлении SELECT, не существует в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="e6617-119">This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-121"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-122">Не удалось открыть файл.</span><span class="sxs-lookup"><span data-stu-id="e6617-122">File could not be opened.</span></span> <span data-ttu-id="e6617-123">Было указано имя файла с ошибками или файл был перемещен, переименован или удален.</span><span class="sxs-lookup"><span data-stu-id="e6617-123">A misspelled file name was specified, or a file has been moved, renamed, or deleted.</span></span> <span data-ttu-id="e6617-124">По сети диск может быть временно недоступен или сетевой трафик может препятствовать подключению.</span><span class="sxs-lookup"><span data-stu-id="e6617-124">Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-126"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-127">Не удалось прочитать файл.</span><span class="sxs-lookup"><span data-stu-id="e6617-127">File could not be read.</span></span> <span data-ttu-id="e6617-128">Имя файла указано неправильно, возможно, файл был перемещен или удален либо файл поврежден.</span><span class="sxs-lookup"><span data-stu-id="e6617-128">The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-130"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-131">Сбой записи в файл.</span><span class="sxs-lookup"><span data-stu-id="e6617-131">Write to file failed.</span></span> <span data-ttu-id="e6617-132">Возможно, вы закрыли файл, а затем попытались записать его, или файл может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="e6617-132">You might have closed a file and then tried to write to it, or the file might be corrupted.</span></span> <span data-ttu-id="e6617-133">Если файл находится на сетевом диске, временные сетевые условия могут препятствовать записи на сетевой диск.</span><span class="sxs-lookup"><span data-stu-id="e6617-133">If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-135"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-136">Либо <strong>BOF,</strong> <strong>либо EOF</strong> имеет true, либо текущая запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="e6617-136">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="e6617-137">Для запрашиваемой операции требуется текущая запись.</span><span class="sxs-lookup"><span data-stu-id="e6617-137">Requested operation requires a current record.</span></span> <span data-ttu-id="e6617-138">Была предпринята попытка обновить записи <strong></strong> с помощью поиска или поиска, чтобы переместить указатель записи в нужную запись. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="e6617-138">An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record.</span></span> <span data-ttu-id="e6617-139">Если запись не найдена, <strong>EOF</strong> будет иметь true.</span><span class="sxs-lookup"><span data-stu-id="e6617-139">If the record is not found, <strong>EOF</strong> will be True.</span></span> <span data-ttu-id="e6617-140">Эта ошибка также может возникать после с ошибки <strong>AddNew</strong> или <strong>Delete,</strong> так как при с ошибке этих методов нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e6617-140">This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-142"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-143">В этом контексте операция не разрешена.</span><span class="sxs-lookup"><span data-stu-id="e6617-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-145"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-146">Поставщик отличается от поставщика, который уже используется.</span><span class="sxs-lookup"><span data-stu-id="e6617-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-148"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-149"><strong>Объект подключения</strong> не может быть явно закрыт во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="e6617-149"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span> <span data-ttu-id="e6617-150">Объект <strong>Recordset</strong> или <strong>Connection,</strong> который в настоящее время участвует в транзакции, не может быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="e6617-150">A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed.</span></span> <span data-ttu-id="e6617-151">Вызовите <strong>RollbackTrans или</strong> <strong>CommitTrans</strong> перед закрытием объекта.</span><span class="sxs-lookup"><span data-stu-id="e6617-151">Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-153"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-154">Объект или поставщик не могут выполнить запрашиваемую операцию.</span><span class="sxs-lookup"><span data-stu-id="e6617-154">The object or provider is not capable of performing the requested operation.</span></span> <span data-ttu-id="e6617-155">Некоторые операции зависят от конкретной версии поставщика.</span><span class="sxs-lookup"><span data-stu-id="e6617-155">Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-157"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-158">Не удается найти элемент в коллекции, соответствующей запросятово имени или порядку.</span><span class="sxs-lookup"><span data-stu-id="e6617-158">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span> <span data-ttu-id="e6617-159">Указано неправильное поле или имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="e6617-159">An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-161"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-162">Объект уже находится в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6617-162">Object is already in collection.</span></span> <span data-ttu-id="e6617-163">Не удается приметься.</span><span class="sxs-lookup"><span data-stu-id="e6617-163">Cannot append.</span></span> <span data-ttu-id="e6617-164">Объект нельзя добавить в ту же коллекцию дважды.</span><span class="sxs-lookup"><span data-stu-id="e6617-164">An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-166"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-167">Объект больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="e6617-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-169"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-170">Приложение использует неправильное значение для текущей операции.</span><span class="sxs-lookup"><span data-stu-id="e6617-170">Application uses a value of the wrong type for the current operation.</span></span> <span data-ttu-id="e6617-171">Возможно, вы предоставили строку для операции, которая ожидает потока, например.</span><span class="sxs-lookup"><span data-stu-id="e6617-171">You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-173"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-174">Операция не разрешена при закрытии объекта.</span><span class="sxs-lookup"><span data-stu-id="e6617-174">Operation is not allowed when the object is closed.</span></span> <span data-ttu-id="e6617-175">Подключение <strong>или</strong> <strong>набор записей</strong> закрыты.</span><span class="sxs-lookup"><span data-stu-id="e6617-175">The <strong>Connection</strong> or <strong>Recordset</strong> has been closed.</span></span> <span data-ttu-id="e6617-176">Например, другая процедура могла закрыть глобальный объект.</span><span class="sxs-lookup"><span data-stu-id="e6617-176">For example, some other routine might have closed a global object.</span></span> <span data-ttu-id="e6617-177">Эту ошибку можно предотвратить, проверив свойство <strong>State</strong> перед попыткой операции.</span><span class="sxs-lookup"><span data-stu-id="e6617-177">You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-179"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-180">Операция не разрешена, если объект открыт.</span><span class="sxs-lookup"><span data-stu-id="e6617-180">Operation is not allowed when the object is open.</span></span> <span data-ttu-id="e6617-181">Открытый объект не может быть открыт.</span><span class="sxs-lookup"><span data-stu-id="e6617-181">An object that is open cannot be opened.</span></span> <span data-ttu-id="e6617-182">Поля нельзя примедить к открытому <strong>набору записей.</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-182">Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-184"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-185">Не удается найти поставщика.</span><span class="sxs-lookup"><span data-stu-id="e6617-185">Provider cannot be found.</span></span> <span data-ttu-id="e6617-186">Он может быть неправильно установлен.</span><span class="sxs-lookup"><span data-stu-id="e6617-186">It may not be properly installed.</span></span> <span data-ttu-id="e6617-187">Имя поставщика может быть указано неправильно, указанный поставщик может не быть установлен на компьютере, на котором выполняется код, или установка может быть повреждена.</span><span class="sxs-lookup"><span data-stu-id="e6617-187">The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-189"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-190">Свойство <strong>ActiveConnection</strong> объекта <strong>Recordset,</strong> в качестве источника которого имеется объект <strong>Command,</strong> нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="e6617-190">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed.</span></span> <span data-ttu-id="e6617-191">Приложение попытались назначить новый объект <strong>Connection</strong> <strong>объекту Recordset,</strong> который имеет объект <strong>Command</strong> в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="e6617-191">The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-193"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-194"><strong>Объект Parameter</strong> определен неправильно.</span><span class="sxs-lookup"><span data-stu-id="e6617-194"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="e6617-195">Предоставлены несогласованные или неполные сведения.</span><span class="sxs-lookup"><span data-stu-id="e6617-195">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-197"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-198">Подключение нельзя использовать для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="e6617-198">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="e6617-199">В этом контексте он либо закрыт, либо недействителен.</span><span class="sxs-lookup"><span data-stu-id="e6617-199">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-201"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-202">Операция не может быть выполнена во время обработки события.</span><span class="sxs-lookup"><span data-stu-id="e6617-202">Operation cannot be performed while processing event.</span></span> <span data-ttu-id="e6617-203">Невозможно выполнить операцию в обработнике событий, который вызывает повторную работу события.</span><span class="sxs-lookup"><span data-stu-id="e6617-203">An operation cannot be performed within an event handler that causes the event to fire again.</span></span> <span data-ttu-id="e6617-204">Например, методы навигации не должны быть вызваны из <strong>обработника событий WillMove.</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-204">For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-206"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-207">Операция не может выполняться при асинхронном выполнении.</span><span class="sxs-lookup"><span data-stu-id="e6617-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-209"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-210">Операция была отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="e6617-210">Operation has been canceled by the user.</span></span> <span data-ttu-id="e6617-211">Приложение вызвало метод <strong>CancelUpdate</strong> или <strong>CancelBatch,</strong> а текущая операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="e6617-211">The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-213"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-214">Операция не может выполняться при асинхронном подключении.</span><span class="sxs-lookup"><span data-stu-id="e6617-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-216"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-217">Транзакция координации недействительна или не запущена.</span><span class="sxs-lookup"><span data-stu-id="e6617-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-219"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-220">Не удается выполнить операцию, пока она не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6617-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-222"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-223">Параметры безопасности на этом компьютере запрещают доступ к источнику данных в другом домене.</span><span class="sxs-lookup"><span data-stu-id="e6617-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-225"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-226">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e6617-226">For internal use only.</span></span> <span data-ttu-id="e6617-227">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="e6617-227">Don't use.</span></span> <span data-ttu-id="e6617-228">(Запись была включена для полноты.</span><span class="sxs-lookup"><span data-stu-id="e6617-228">(Entry was included for the sake of completeness.</span></span> <span data-ttu-id="e6617-229">Эта ошибка не должна отображаться в коде.)</span><span class="sxs-lookup"><span data-stu-id="e6617-229">This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-231"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-232">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e6617-232">For internal use only.</span></span> <span data-ttu-id="e6617-233">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="e6617-233">Don't use.</span></span> <span data-ttu-id="e6617-234">(Запись включена для полноты.</span><span class="sxs-lookup"><span data-stu-id="e6617-234">(Entry included for the sake of completeness.</span></span> <span data-ttu-id="e6617-235">Эта ошибка не должна отображаться в коде.)</span><span class="sxs-lookup"><span data-stu-id="e6617-235">This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-237"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-238">Значение данных конфликтет с ограничениями целостности поля.</span><span class="sxs-lookup"><span data-stu-id="e6617-238">Data value conflicts with the integrity constraints of the field.</span></span> <span data-ttu-id="e6617-239">Новое значение поля <strong>приведет</strong> к дублированию ключа.</span><span class="sxs-lookup"><span data-stu-id="e6617-239">A new value for a <strong>Field</strong> would cause a duplicate key.</span></span> <span data-ttu-id="e6617-240">Значение, которое формирует одну сторону связи между двумя записями, может быть не может быть updatable.</span><span class="sxs-lookup"><span data-stu-id="e6617-240">A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-242"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-243">Недостаточное разрешение препятствует записи в поле.</span><span class="sxs-lookup"><span data-stu-id="e6617-243">Insufficient permission prevents writing to the field.</span></span> <span data-ttu-id="e6617-244">У пользователя, имя которого есть в строке подключения, нет необходимых разрешений для записи в <strong>поле.</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-244">The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-246"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-247">Значение данных слишком большое для представления типом данных поля.</span><span class="sxs-lookup"><span data-stu-id="e6617-247">Data value is too large to be represented by the field data type.</span></span> <span data-ttu-id="e6617-248">Назначено числовая величина, слишком большая для назначенного поля.</span><span class="sxs-lookup"><span data-stu-id="e6617-248">A numeric value that is too large for the intended field was assigned.</span></span> <span data-ttu-id="e6617-249">Например, длинное значение было назначено короткому полю.</span><span class="sxs-lookup"><span data-stu-id="e6617-249">For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-251"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-252">Значение данных конфликтет с типом данных или ограничениями поля.</span><span class="sxs-lookup"><span data-stu-id="e6617-252">Data value conflicts with the data type or constraints of the field.</span></span> <span data-ttu-id="e6617-253">Хранилище данных имеет ограничения проверки, отличающиеся от <strong>значения Field.</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-253">The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-255"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-256">Сбой преобразования, так как значение данных было подписано, а тип данных поля, используемый поставщиком, не подписан.</span><span class="sxs-lookup"><span data-stu-id="e6617-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-258"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-259">Значение данных не может быть преобразовано по другим причинам, кроме несоответствия подписей или переполнения данных.</span><span class="sxs-lookup"><span data-stu-id="e6617-259">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="e6617-260">Например, преобразование будет иметь усеченные данные.</span><span class="sxs-lookup"><span data-stu-id="e6617-260">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-262"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-263">Значение данных нельзя установить или извлечь, так как тип данных поля был неизвестным, или у поставщика недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e6617-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-265"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-266">Запись не содержит это поле.</span><span class="sxs-lookup"><span data-stu-id="e6617-266">Record does not contain this field.</span></span> <span data-ttu-id="e6617-267">Было указано неправильное имя поля или поле, не в которое в коллекции <strong>Fields</strong> текущей записи была указана ссылка.</span><span class="sxs-lookup"><span data-stu-id="e6617-267">An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-269"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-270">Исходный URL-адрес или родительский URL-адрес назначения не существуют.</span><span class="sxs-lookup"><span data-stu-id="e6617-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="e6617-271">В URL-адресе источника или назначения имеется опечатка.</span><span class="sxs-lookup"><span data-stu-id="e6617-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="e6617-272">Возможно, у https://mysite/photo/myphoto.jpg вас будет время, когда вы действительно должны https://mysite/photos/myphoto.jpg иметь вместо этого.</span><span class="sxs-lookup"><span data-stu-id="e6617-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="e6617-273">Опечатка в родительском URL-адресе (в данном случае <em>фотография,</em> а не <em>фотографии)</em>вызвала ошибку.</span><span class="sxs-lookup"><span data-stu-id="e6617-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-275"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-276">Недостаточно разрешений для доступа к дереву или подtree.</span><span class="sxs-lookup"><span data-stu-id="e6617-276">Permissions are insufficient to access tree or subtree.</span></span> <span data-ttu-id="e6617-277">Пользователь с именем в строке подключения не имеет соответствующих разрешений.</span><span class="sxs-lookup"><span data-stu-id="e6617-277">The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-279"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-280">URL-адрес содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="e6617-280">URL contains invalid characters.</span></span> <span data-ttu-id="e6617-281">Убедитесь, что URL-адрес введите правильно.</span><span class="sxs-lookup"><span data-stu-id="e6617-281">Make sure the URL is typed correctly.</span></span> <span data-ttu-id="e6617-282">URL-адрес следует схеме, зарегистрированной для текущего поставщика (например, поставщик публикации Интернета зарегистрирован для http).</span><span class="sxs-lookup"><span data-stu-id="e6617-282">The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-284"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-285">Объект, представленный указанным URL-адресом, блокируется одним или более другими процессами.</span><span class="sxs-lookup"><span data-stu-id="e6617-285">Object represented by the specified URL is locked by one or more other processes.</span></span> <span data-ttu-id="e6617-286">Подождите, пока процесс завершится, и снова попытайтесь повторить операцию.</span><span class="sxs-lookup"><span data-stu-id="e6617-286">Wait until the process has finished and attempt the operation again.</span></span> <span data-ttu-id="e6617-287">Объект, к который вы пытаетесь получить доступ, заблокирован другим пользователем или другим процессом в приложении.</span><span class="sxs-lookup"><span data-stu-id="e6617-287">The object you are trying to access has been locked by another user or by another process in your application.</span></span> <span data-ttu-id="e6617-288">Скорее всего, это может возникнуть в среде с несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="e6617-288">This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-290"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-291">Не удается выполнить операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="e6617-291">Copy operation cannot be performed.</span></span> <span data-ttu-id="e6617-292">Объект с именем по url-адресу назначения уже существует.</span><span class="sxs-lookup"><span data-stu-id="e6617-292">Object named by destination URL already exists.</span></span> <span data-ttu-id="e6617-293">Укажите <strong>adCopyOverwrite для</strong> замены объекта.</span><span class="sxs-lookup"><span data-stu-id="e6617-293">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span> <span data-ttu-id="e6617-294">Если при копировании файлов в каталоге не указан <strong>adCopyOverwrite,</strong> то при попытке скопировать элемент, который уже существует в месте назначения, происходит сбой копирования.</span><span class="sxs-lookup"><span data-stu-id="e6617-294">If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-296"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-297">Сервер не может завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="e6617-297">The server cannot complete the operation.</span></span> <span data-ttu-id="e6617-298">Это может быть из-за того, что сервер занят другими операциями или у него может быть мало ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6617-298">This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-300"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-301">Поставщик не может найти устройство хранения, обозначенное URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="e6617-301">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="e6617-302">Убедитесь, что URL-адрес введите правильно.</span><span class="sxs-lookup"><span data-stu-id="e6617-302">Make sure the URL is typed correctly.</span></span> <span data-ttu-id="e6617-303">URL-адрес устройства хранения может быть неправильным, но эта ошибка может возникнуть по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="e6617-303">The URL of the storage device might be incorrect, but this error can occur for other reasons.</span></span> <span data-ttu-id="e6617-304">Устройство может быть отключено или большой объем сетевого трафика может препятствовать подключению.</span><span class="sxs-lookup"><span data-stu-id="e6617-304">The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-306"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-307">Не удается выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="e6617-307">Operation cannot be performed.</span></span> <span data-ttu-id="e6617-308">Поставщик не может получить достаточно места для хранения.</span><span class="sxs-lookup"><span data-stu-id="e6617-308">Provider cannot obtain enough storage space.</span></span> <span data-ttu-id="e6617-309">На сервере может быть недостаточно места на ОЗУ или жестком диске для временных файлов.</span><span class="sxs-lookup"><span data-stu-id="e6617-309">There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-311"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-312">Url-адрес источника или назначения находится за пределами области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e6617-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-314"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-315">Не удалось завершить операцию, и состояние недоступно.</span><span class="sxs-lookup"><span data-stu-id="e6617-315">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="e6617-316">Поле может быть недоступно или операция не была предпринята.</span><span class="sxs-lookup"><span data-stu-id="e6617-316">The field may be unavailable or the operation was not attempted.</span></span> <span data-ttu-id="e6617-317">Другой пользователь мог изменить или удалить поле, к нему вы пытаетесь получить доступ.</span><span class="sxs-lookup"><span data-stu-id="e6617-317">Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-319"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-320">Запись с именем по этому URL-адресу не существует.</span><span class="sxs-lookup"><span data-stu-id="e6617-320">Record named by this URL does not exist.</span></span> <span data-ttu-id="e6617-321">При попытке открыть файл с помощью объекта <strong>Record</strong> имя файла или путь к файлу был опечаток.</span><span class="sxs-lookup"><span data-stu-id="e6617-321">While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-323"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-324">URL-адрес удаляемого объекта находится вне области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e6617-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-326"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-327">Для операции требуется <strong>допустимый parentCatalog.</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-329"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-330">Подключение было отклонено.</span><span class="sxs-lookup"><span data-stu-id="e6617-330">Connection was denied.</span></span> <span data-ttu-id="e6617-331">Запрашиваемая вами новая связь имеет характеристики, отлича которые уже используются.</span><span class="sxs-lookup"><span data-stu-id="e6617-331">The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-333"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-334">Сбой обновления полей.</span><span class="sxs-lookup"><span data-stu-id="e6617-334">Fields update failed.</span></span> <span data-ttu-id="e6617-335">Для получения дополнительных сведений <strong>изучите свойство Status</strong> отдельных объектов полей.</span><span class="sxs-lookup"><span data-stu-id="e6617-335">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span> <span data-ttu-id="e6617-336">Эта ошибка может возникать в двух ситуациях: при изменении значения объекта <strong>Field</strong> в процессе изменения или добавления записи в базу данных; и при изменении свойств самого <strong>объекта Field.</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-336">This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself.</span></span> <span data-ttu-id="e6617-337"><strong>Сбой</strong> обновления record или <strong>Recordset</strong> из-за проблемы с одним из полей в текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e6617-337">The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record.</span></span> <span data-ttu-id="e6617-338">Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span><span class="sxs-lookup"><span data-stu-id="e6617-338">Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6617-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-340"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-341">Поставщик не поддерживает ограничения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e6617-341">Provider does not support sharing restrictions.</span></span> <span data-ttu-id="e6617-342">Предпринята попытка ограничить общий доступ к файлам, и поставщик не поддерживает эту концепцию.</span><span class="sxs-lookup"><span data-stu-id="e6617-342">An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6617-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-344"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="e6617-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="e6617-345">Поставщик не поддерживает запрашиваемого типа ограничения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e6617-345">Provider does not support the requested kind of sharing restriction.</span></span> <span data-ttu-id="e6617-346">Предпринята попытка установить определенный тип ограничения общего доступа к файлам, который не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e6617-346">An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider.</span></span> <span data-ttu-id="e6617-347">Чтобы определить, какие ограничения общего доступа к файлам поддерживаются, см. документацию поставщика.</span><span class="sxs-lookup"><span data-stu-id="e6617-347">See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

