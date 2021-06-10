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
# <a name="ado-error-reference"></a><span data-ttu-id="97439-102">Справочник по ошибкам ADO</span><span class="sxs-lookup"><span data-stu-id="97439-102">ADO error reference</span></span>

<span data-ttu-id="97439-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97439-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97439-104">**Константа ErrorValueEnum** описывает значения ошибок ADO.</span><span class="sxs-lookup"><span data-stu-id="97439-104">The **ErrorValueEnum** constant describes the ADO error values.</span></span> <span data-ttu-id="97439-105">Полный список указанных констант, включая значения, см. в приложении [B: ADO Errors.](appendix-b-ado-errors.md)</span><span class="sxs-lookup"><span data-stu-id="97439-105">For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md).</span></span> <span data-ttu-id="97439-106">В этом разделе рассматриваются некоторые из наиболее интересных ошибок и объясняются некоторые конкретные ситуации, которые могут привести к их повышению, или решения для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="97439-106">This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem.</span></span> <span data-ttu-id="97439-107">Перечислены **как константа ErrorValueEnum,** так и короткий положительный десятичной номер.</span><span class="sxs-lookup"><span data-stu-id="97439-107">Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97439-108">Номер</span><span class="sxs-lookup"><span data-stu-id="97439-108">Number</span></span></p></th>
<th><p><span data-ttu-id="97439-109">Константа ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="97439-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="97439-110">Описание/Возможные причины</span><span class="sxs-lookup"><span data-stu-id="97439-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97439-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="97439-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-112"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="97439-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-113">Поставщик не выполнил запрашиваемую операцию.</span><span class="sxs-lookup"><span data-stu-id="97439-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="97439-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-115"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="97439-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-116">Аргументы имеют неправильный тип, находятся вне допустимого диапазона или находятся в конфликте друг с другом.</span><span class="sxs-lookup"><span data-stu-id="97439-116">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span> <span data-ttu-id="97439-117">Эта ошибка часто вызвана опечаткой в SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="97439-117">This error is often caused by a typographical error in an SQL SELECT statement.</span></span> <span data-ttu-id="97439-118">Например, ошибочное имя поля или имя таблицы может создать эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="97439-118">For example, a misspelled field name or table name can generate this error.</span></span> <span data-ttu-id="97439-119">Эта ошибка также может возникать, когда поле или таблица, названная в заявлении SELECT, не существует в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="97439-119">This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="97439-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-121"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="97439-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-122">Файл не может быть открыт.</span><span class="sxs-lookup"><span data-stu-id="97439-122">File could not be opened.</span></span> <span data-ttu-id="97439-123">Было задано имя файла с ошибками, или файл был перемещен, переименован или удален.</span><span class="sxs-lookup"><span data-stu-id="97439-123">A misspelled file name was specified, or a file has been moved, renamed, or deleted.</span></span> <span data-ttu-id="97439-124">В сети диск может быть временно недоступен, а сетевой трафик может препятствовать подключению.</span><span class="sxs-lookup"><span data-stu-id="97439-124">Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="97439-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-126"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="97439-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-127">Файл нельзя было прочитать.</span><span class="sxs-lookup"><span data-stu-id="97439-127">File could not be read.</span></span> <span data-ttu-id="97439-128">Имя файла указывается неправильно, файл мог быть перемещен или удален, или файл мог быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="97439-128">The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="97439-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-130"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="97439-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-131">Написать файл не удалось.</span><span class="sxs-lookup"><span data-stu-id="97439-131">Write to file failed.</span></span> <span data-ttu-id="97439-132">Возможно, вы закрыли файл, а затем попытались написать в него, или файл может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="97439-132">You might have closed a file and then tried to write to it, or the file might be corrupted.</span></span> <span data-ttu-id="97439-133">Если файл расположен на сетевом диске, временные условия сети могут помешать записи на сетевой диск.</span><span class="sxs-lookup"><span data-stu-id="97439-133">If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="97439-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-135"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="97439-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-136">Либо <strong>BOF,</strong> <strong>либо EOF</strong> — true, либо текущая запись удалена.</span><span class="sxs-lookup"><span data-stu-id="97439-136">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="97439-137">Запрашиваемая операция требует текущей записи.</span><span class="sxs-lookup"><span data-stu-id="97439-137">Requested operation requires a current record.</span></span> <span data-ttu-id="97439-138">Была предпринята попытка обновить записи с помощью <strong>Find</strong> или <strong>Seek</strong> для перемещения указателя записи в нужную запись.</span><span class="sxs-lookup"><span data-stu-id="97439-138">An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record.</span></span> <span data-ttu-id="97439-139">Если запись не найдена, <strong>EOF</strong> будет true.</span><span class="sxs-lookup"><span data-stu-id="97439-139">If the record is not found, <strong>EOF</strong> will be True.</span></span> <span data-ttu-id="97439-140">Эта ошибка также может возникнуть после неудачного <strong>addNew</strong> или <strong>Delete,</strong> так как при сбойе этих методов нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="97439-140">This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="97439-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-142"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="97439-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-143">В этом контексте операция запрещена.</span><span class="sxs-lookup"><span data-stu-id="97439-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="97439-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-145"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="97439-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-146">Поставщик, поставляемый, отличается от используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="97439-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="97439-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-148"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="97439-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-149"><strong>Объект подключения</strong> не может быть явно закрыт во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="97439-149"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span> <span data-ttu-id="97439-150">Объект <strong>Recordset</strong> или <strong>Connection,</strong> который в настоящее время участвует в транзакции, не может быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="97439-150">A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed.</span></span> <span data-ttu-id="97439-151">Перед закрытием объекта позвоните в <strong>RollbackTrans</strong> или <strong>CommitTrans.</strong></span><span class="sxs-lookup"><span data-stu-id="97439-151">Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="97439-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-153"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="97439-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-154">Объект или поставщик не способны выполнять запрашиваемую операцию.</span><span class="sxs-lookup"><span data-stu-id="97439-154">The object or provider is not capable of performing the requested operation.</span></span> <span data-ttu-id="97439-155">Некоторые операции зависят от конкретной версии поставщика.</span><span class="sxs-lookup"><span data-stu-id="97439-155">Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="97439-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-157"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="97439-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-158">Элемент не может быть найден в коллекции, соответствующей запрашиваемой имени или ordinal.</span><span class="sxs-lookup"><span data-stu-id="97439-158">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span> <span data-ttu-id="97439-159">Задано неправильное поле или имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="97439-159">An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="97439-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-161"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="97439-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-162">Объект уже находится в коллекции.</span><span class="sxs-lookup"><span data-stu-id="97439-162">Object is already in collection.</span></span> <span data-ttu-id="97439-163">Не удается примять.</span><span class="sxs-lookup"><span data-stu-id="97439-163">Cannot append.</span></span> <span data-ttu-id="97439-164">Объект нельзя дважды добавлять в ту же коллекцию.</span><span class="sxs-lookup"><span data-stu-id="97439-164">An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="97439-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-166"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="97439-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-167">Объект больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="97439-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="97439-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-169"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="97439-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-170">Приложение использует значение неправильного типа для текущей операции.</span><span class="sxs-lookup"><span data-stu-id="97439-170">Application uses a value of the wrong type for the current operation.</span></span> <span data-ttu-id="97439-171">Возможно, вы поставили строку для операции, которая ожидает поток, например.</span><span class="sxs-lookup"><span data-stu-id="97439-171">You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="97439-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-173"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="97439-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-174">Операция не допускается при закрытии объекта.</span><span class="sxs-lookup"><span data-stu-id="97439-174">Operation is not allowed when the object is closed.</span></span> <span data-ttu-id="97439-175">Подключение <strong>или</strong> <strong>набор записей</strong> закрыт.</span><span class="sxs-lookup"><span data-stu-id="97439-175">The <strong>Connection</strong> or <strong>Recordset</strong> has been closed.</span></span> <span data-ttu-id="97439-176">Например, некоторые другие процедуры могли закрыть глобальный объект.</span><span class="sxs-lookup"><span data-stu-id="97439-176">For example, some other routine might have closed a global object.</span></span> <span data-ttu-id="97439-177">Эту ошибку можно предотвратить, проверив <strong>свойство state</strong> перед попыткой операции.</span><span class="sxs-lookup"><span data-stu-id="97439-177">You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="97439-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-179"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="97439-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-180">Операция не допускается, когда объект открыт.</span><span class="sxs-lookup"><span data-stu-id="97439-180">Operation is not allowed when the object is open.</span></span> <span data-ttu-id="97439-181">Открытый объект не может быть открыт.</span><span class="sxs-lookup"><span data-stu-id="97439-181">An object that is open cannot be opened.</span></span> <span data-ttu-id="97439-182">Поля нельзя примыкать к открытому <strong>набору записей.</strong></span><span class="sxs-lookup"><span data-stu-id="97439-182">Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="97439-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-184"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="97439-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-185">Поставщик не может быть найден.</span><span class="sxs-lookup"><span data-stu-id="97439-185">Provider cannot be found.</span></span> <span data-ttu-id="97439-186">Он может быть неправильно установлен.</span><span class="sxs-lookup"><span data-stu-id="97439-186">It may not be properly installed.</span></span> <span data-ttu-id="97439-187">Имя поставщика может быть неправильно указано, указанный поставщик может не быть установлен на компьютере, на котором выполняется код, или установка может быть повреждена.</span><span class="sxs-lookup"><span data-stu-id="97439-187">The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="97439-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-189"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="97439-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-190">Свойство <strong>ActiveConnection</strong> объекта <strong>Recordset,</strong> который имеет объект <strong>Command</strong> в качестве источника, не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="97439-190">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed.</span></span> <span data-ttu-id="97439-191">Приложение пыталось назначить новый объект <strong>Подключения</strong> к <strong>набору Recordset,</strong> который имеет <strong>объект Command</strong> в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="97439-191">The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="97439-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-193"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="97439-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-194"><strong>Объект параметра</strong> неправильно определен.</span><span class="sxs-lookup"><span data-stu-id="97439-194"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="97439-195">Несогласованные или неполные сведения были предоставлены.</span><span class="sxs-lookup"><span data-stu-id="97439-195">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="97439-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-197"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="97439-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-198">Подключение не может использоваться для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="97439-198">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="97439-199">В этом контексте она закрыта или недействительна.</span><span class="sxs-lookup"><span data-stu-id="97439-199">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="97439-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-201"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="97439-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-202">Операция не может выполняться во время обработки события.</span><span class="sxs-lookup"><span data-stu-id="97439-202">Operation cannot be performed while processing event.</span></span> <span data-ttu-id="97439-203">Операция не может выполняться в обработнике событий, из-за этого событие снова загорелось.</span><span class="sxs-lookup"><span data-stu-id="97439-203">An operation cannot be performed within an event handler that causes the event to fire again.</span></span> <span data-ttu-id="97439-204">Например, методы навигации не должны быть вызваны из обработника событий <strong>WillMove.</strong></span><span class="sxs-lookup"><span data-stu-id="97439-204">For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="97439-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-206"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="97439-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-207">Операция не может выполняться при асинхронном выполнении.</span><span class="sxs-lookup"><span data-stu-id="97439-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="97439-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-209"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="97439-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-210">Операция была отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="97439-210">Operation has been canceled by the user.</span></span> <span data-ttu-id="97439-211">Приложение вызвало метод <strong>CancelUpdate</strong> или <strong>CancelBatch,</strong> и текущая операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="97439-211">The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="97439-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-213"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="97439-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-214">Операция не может выполняться при асинхронном подключении.</span><span class="sxs-lookup"><span data-stu-id="97439-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="97439-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-216"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="97439-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-217">Координация транзакции недействительна или не запущена.</span><span class="sxs-lookup"><span data-stu-id="97439-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="97439-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-219"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="97439-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-220">Операция не может выполняться при неоформлённой работе.</span><span class="sxs-lookup"><span data-stu-id="97439-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="97439-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-222"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="97439-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-223">Параметры безопасности на этом компьютере запрещают доступ к источнику данных на другом домене.</span><span class="sxs-lookup"><span data-stu-id="97439-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="97439-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-225"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="97439-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-226">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="97439-226">For internal use only.</span></span> <span data-ttu-id="97439-227">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="97439-227">Don't use.</span></span> <span data-ttu-id="97439-228">(Запись была включена для полноты.</span><span class="sxs-lookup"><span data-stu-id="97439-228">(Entry was included for the sake of completeness.</span></span> <span data-ttu-id="97439-229">Эта ошибка не должна отображаться в коде.)</span><span class="sxs-lookup"><span data-stu-id="97439-229">This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="97439-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-231"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="97439-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-232">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="97439-232">For internal use only.</span></span> <span data-ttu-id="97439-233">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="97439-233">Don't use.</span></span> <span data-ttu-id="97439-234">(Запись включена для полноты.</span><span class="sxs-lookup"><span data-stu-id="97439-234">(Entry included for the sake of completeness.</span></span> <span data-ttu-id="97439-235">Эта ошибка не должна отображаться в коде.)</span><span class="sxs-lookup"><span data-stu-id="97439-235">This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="97439-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-237"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="97439-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-238">Значение data противоречит ограничениям целостности поля.</span><span class="sxs-lookup"><span data-stu-id="97439-238">Data value conflicts with the integrity constraints of the field.</span></span> <span data-ttu-id="97439-239">Новое значение для <strong>поля приведет</strong> к дублирующему ключу.</span><span class="sxs-lookup"><span data-stu-id="97439-239">A new value for a <strong>Field</strong> would cause a duplicate key.</span></span> <span data-ttu-id="97439-240">Значение, которое формирует одну сторону связи между двумя записями, может не быть updatable.</span><span class="sxs-lookup"><span data-stu-id="97439-240">A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="97439-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-242"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="97439-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-243">Недостаточное разрешение препятствует записи в поле.</span><span class="sxs-lookup"><span data-stu-id="97439-243">Insufficient permission prevents writing to the field.</span></span> <span data-ttu-id="97439-244">Пользователь, названный в строке подключения, не имеет соответствующих разрешений для записи в <strong>поле</strong>.</span><span class="sxs-lookup"><span data-stu-id="97439-244">The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="97439-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-246"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="97439-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-247">Значение данных слишком большое, чтобы представляться типом данных поля.</span><span class="sxs-lookup"><span data-stu-id="97439-247">Data value is too large to be represented by the field data type.</span></span> <span data-ttu-id="97439-248">Назначено численное значение, слишком большое для назначенного поля.</span><span class="sxs-lookup"><span data-stu-id="97439-248">A numeric value that is too large for the intended field was assigned.</span></span> <span data-ttu-id="97439-249">Например, для короткого integer-поля было назначено длинное значение.</span><span class="sxs-lookup"><span data-stu-id="97439-249">For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="97439-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-251"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="97439-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-252">Значение данных противоречит типу данных или ограничениям поля.</span><span class="sxs-lookup"><span data-stu-id="97439-252">Data value conflicts with the data type or constraints of the field.</span></span> <span data-ttu-id="97439-253">В хранилище данных имеются ограничения проверки, отличающиеся от <strong>значения Field.</strong></span><span class="sxs-lookup"><span data-stu-id="97439-253">The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="97439-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-255"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="97439-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-256">Преобразование не удалось, так как значение данных было подписано, а тип данных поля, используемый поставщиком, не был подписан.</span><span class="sxs-lookup"><span data-stu-id="97439-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="97439-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-258"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="97439-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-259">Значение данных не может быть преобразовано по другим причинам, кроме несоответствия знака или переполнения данных.</span><span class="sxs-lookup"><span data-stu-id="97439-259">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="97439-260">Например, преобразование будет иметь усеченные данные.</span><span class="sxs-lookup"><span data-stu-id="97439-260">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="97439-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-262"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="97439-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-263">Значение данных невозможно установить или получить, так как тип данных поля был неизвестным или у поставщика не было достаточных ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="97439-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="97439-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-265"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="97439-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-266">Запись не содержит этого поля.</span><span class="sxs-lookup"><span data-stu-id="97439-266">Record does not contain this field.</span></span> <span data-ttu-id="97439-267">Было указано неправильное имя поля или поле, не указанное в коллекции <strong>Fields</strong> текущей записи.</span><span class="sxs-lookup"><span data-stu-id="97439-267">An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="97439-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-269"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="97439-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-270">Url-адрес источника или родитель URL-адреса не существует.</span><span class="sxs-lookup"><span data-stu-id="97439-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="97439-271">В URL-адресе источника или назначения имеется опечатка.</span><span class="sxs-lookup"><span data-stu-id="97439-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="97439-272">Возможно, у https://mysite/photo/myphoto.jpg вас будет время, когда вы должны иметь https://mysite/photos/myphoto.jpg вместо этого.</span><span class="sxs-lookup"><span data-stu-id="97439-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="97439-273">Ошибка в родительском URL-адресе (в данном <em></em> случае фотография, а не <em>фотографии)</em>вызвала ошибку.</span><span class="sxs-lookup"><span data-stu-id="97439-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="97439-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-275"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="97439-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-276">Разрешений недостаточно для доступа к дереву или подтрию.</span><span class="sxs-lookup"><span data-stu-id="97439-276">Permissions are insufficient to access tree or subtree.</span></span> <span data-ttu-id="97439-277">Пользователь, названный в строке подключения, не имеет соответствующих разрешений.</span><span class="sxs-lookup"><span data-stu-id="97439-277">The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="97439-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-279"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="97439-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-280">URL-адрес содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="97439-280">URL contains invalid characters.</span></span> <span data-ttu-id="97439-281">Убедитесь, что URL-адрес введите правильно.</span><span class="sxs-lookup"><span data-stu-id="97439-281">Make sure the URL is typed correctly.</span></span> <span data-ttu-id="97439-282">URL-адрес следует схеме, зарегистрированной текущему поставщику (например, поставщик интернет-публикаций зарегистрирован для http).</span><span class="sxs-lookup"><span data-stu-id="97439-282">The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="97439-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-284"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="97439-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-285">Объект, представленный указанным URL-адресом, блокируется одним или более другими процессами.</span><span class="sxs-lookup"><span data-stu-id="97439-285">Object represented by the specified URL is locked by one or more other processes.</span></span> <span data-ttu-id="97439-286">Подождите, пока процесс завершится, и снова попытайтесь сделать операцию.</span><span class="sxs-lookup"><span data-stu-id="97439-286">Wait until the process has finished and attempt the operation again.</span></span> <span data-ttu-id="97439-287">Объект, к который вы пытаетесь получить доступ, был заблокирован другим пользователем или другим процессом в вашем приложении.</span><span class="sxs-lookup"><span data-stu-id="97439-287">The object you are trying to access has been locked by another user or by another process in your application.</span></span> <span data-ttu-id="97439-288">Скорее всего, это может возникнуть в среде с несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="97439-288">This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="97439-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-290"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="97439-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-291">Операция копирования не может выполняться.</span><span class="sxs-lookup"><span data-stu-id="97439-291">Copy operation cannot be performed.</span></span> <span data-ttu-id="97439-292">Объект, названный URL-адресом назначения, уже существует.</span><span class="sxs-lookup"><span data-stu-id="97439-292">Object named by destination URL already exists.</span></span> <span data-ttu-id="97439-293">Укажите <strong>adCopyOverwrite для</strong> замены объекта.</span><span class="sxs-lookup"><span data-stu-id="97439-293">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span> <span data-ttu-id="97439-294">Если при копировании файлов в каталоге не указывается <strong>adCopyOverwrite,</strong> при попытке скопировать элемент, который уже существует в пункте назначения, копия не удается.</span><span class="sxs-lookup"><span data-stu-id="97439-294">If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="97439-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-296"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="97439-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-297">Сервер не может завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="97439-297">The server cannot complete the operation.</span></span> <span data-ttu-id="97439-298">Возможно, это происходит из-за того, что сервер занят другими операциями или может иметь ограниченные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="97439-298">This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="97439-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-300"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="97439-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-301">Поставщик не может найти устройство хранения, обозначенное URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="97439-301">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="97439-302">Убедитесь, что URL-адрес введите правильно.</span><span class="sxs-lookup"><span data-stu-id="97439-302">Make sure the URL is typed correctly.</span></span> <span data-ttu-id="97439-303">URL-адрес устройства хранения может быть неправильным, но эта ошибка может возникнуть по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="97439-303">The URL of the storage device might be incorrect, but this error can occur for other reasons.</span></span> <span data-ttu-id="97439-304">Устройство может быть отключено, а большой объем сетевого трафика может помешать подключению.</span><span class="sxs-lookup"><span data-stu-id="97439-304">The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="97439-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-306"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="97439-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-307">Операция не может быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="97439-307">Operation cannot be performed.</span></span> <span data-ttu-id="97439-308">Поставщик не может получить достаточно места для хранения.</span><span class="sxs-lookup"><span data-stu-id="97439-308">Provider cannot obtain enough storage space.</span></span> <span data-ttu-id="97439-309">На сервере может не быть достаточно места для оперативной памяти или жесткого диска для временных файлов.</span><span class="sxs-lookup"><span data-stu-id="97439-309">There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="97439-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-311"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="97439-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-312">URL-адрес источника или назначения находится за пределами текущей записи.</span><span class="sxs-lookup"><span data-stu-id="97439-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="97439-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-314"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="97439-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-315">Операция не завершена, и состояние недоступно.</span><span class="sxs-lookup"><span data-stu-id="97439-315">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="97439-316">Поле может быть недоступно или операция не была предпринята.</span><span class="sxs-lookup"><span data-stu-id="97439-316">The field may be unavailable or the operation was not attempted.</span></span> <span data-ttu-id="97439-317">Другой пользователь мог изменить или удалить поле, к нему необходимо получить доступ.</span><span class="sxs-lookup"><span data-stu-id="97439-317">Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="97439-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-319"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="97439-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-320">Запись, названная этим URL-адресом, не существует.</span><span class="sxs-lookup"><span data-stu-id="97439-320">Record named by this URL does not exist.</span></span> <span data-ttu-id="97439-321">При попытке открыть файл с помощью объекта <strong>Запись</strong> имя файла или путь к файлу был опечатка.</span><span class="sxs-lookup"><span data-stu-id="97439-321">While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="97439-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-323"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="97439-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-324">URL-адрес удаляемого объекта находится за пределами текущей записи.</span><span class="sxs-lookup"><span data-stu-id="97439-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="97439-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-326"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="97439-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-327">Операция требует допустимого <strong>ParentCatalog</strong>.</span><span class="sxs-lookup"><span data-stu-id="97439-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="97439-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-329"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="97439-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-330">Подключение было отказано.</span><span class="sxs-lookup"><span data-stu-id="97439-330">Connection was denied.</span></span> <span data-ttu-id="97439-331">Запрашиваемая вами новая связь отличается от используемого подключения.</span><span class="sxs-lookup"><span data-stu-id="97439-331">The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="97439-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-333"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="97439-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-334">Обновление полей не удалось.</span><span class="sxs-lookup"><span data-stu-id="97439-334">Fields update failed.</span></span> <span data-ttu-id="97439-335">Дополнительные сведения изучите свойство <strong>Status</strong> отдельных объектов поля.</span><span class="sxs-lookup"><span data-stu-id="97439-335">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span> <span data-ttu-id="97439-336">Эта ошибка может возникать в двух ситуациях: при изменении значения объекта <strong>Field</strong> в процессе изменения или добавления записи в базу данных; и при изменении свойств самого <strong>объекта Field.</strong></span><span class="sxs-lookup"><span data-stu-id="97439-336">This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself.</span></span> <span data-ttu-id="97439-337">Обновление <strong>Record</strong> или <strong>Recordset</strong> не удалось из-за проблемы с одним из полей текущей записи.</span><span class="sxs-lookup"><span data-stu-id="97439-337">The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record.</span></span> <span data-ttu-id="97439-338">Перенапределяйте коллекцию <strong>Fields</strong> и проверьте свойство <strong>Status</strong> каждого поля, чтобы определить причину проблемы.</span><span class="sxs-lookup"><span data-stu-id="97439-338">Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97439-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="97439-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-340"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="97439-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-341">Поставщик не поддерживает ограничения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="97439-341">Provider does not support sharing restrictions.</span></span> <span data-ttu-id="97439-342">Была предпринята попытка ограничить общий доступ к файлам, и поставщик не поддерживает эту концепцию.</span><span class="sxs-lookup"><span data-stu-id="97439-342">An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97439-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="97439-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-344"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="97439-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="97439-345">Поставщик не поддерживает запрашиваемого вида ограничения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="97439-345">Provider does not support the requested kind of sharing restriction.</span></span> <span data-ttu-id="97439-346">Была предпринята попытка установить определенный тип ограничения общего доступа к файлам, который не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="97439-346">An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider.</span></span> <span data-ttu-id="97439-347">См. документацию поставщика, чтобы определить, какие ограничения для общего доступа к файлам поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="97439-347">See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

