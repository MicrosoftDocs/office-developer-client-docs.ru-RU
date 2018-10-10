---
title: ADO Error Reference
TOCTitle: ADO Error Reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53dfb03616b0610ed580f4e576f4c48ef3be8525
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482710"
---
# <a name="ado-error-reference"></a><span data-ttu-id="3c477-102">ADO Error Reference</span><span class="sxs-lookup"><span data-stu-id="3c477-102">ADO Error Reference</span></span>


<span data-ttu-id="3c477-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c477-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3c477-104">Константа **ErrorValueEnum** описаны значения ошибка ADO.</span><span class="sxs-lookup"><span data-stu-id="3c477-104">The **ErrorValueEnum** constant describes the ADO error values.</span></span> <span data-ttu-id="3c477-105">Полный список эти перечисленные константы, включая значения отображаются [Ошибки ADO B: приложение](appendix-b-ado-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3c477-105">For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md).</span></span> <span data-ttu-id="3c477-106">В этом разделе будет проверить некоторые из наиболее интересных ошибок и описываются некоторые конкретных ситуаций, которые могут вызывать их или с помощью решений для решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="3c477-106">This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem.</span></span> <span data-ttu-id="3c477-107">Перечисленные константы **ErrorValueEnum** и короткий положительное десятичное число.</span><span class="sxs-lookup"><span data-stu-id="3c477-107">Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c477-108">Number</span><span class="sxs-lookup"><span data-stu-id="3c477-108">Number</span></span></p></th>
<th><p><span data-ttu-id="3c477-109">Константа ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="3c477-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="3c477-110">Описание/возможные причины</span><span class="sxs-lookup"><span data-stu-id="3c477-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c477-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-112"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-113">Не удалось выполнить запрошенную операцию поставщика.</span><span class="sxs-lookup"><span data-stu-id="3c477-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-115"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-116">Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="3c477-116">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span> <span data-ttu-id="3c477-117">Ошибка ввода в инструкции SQL SELECT зачастую причиной этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="3c477-117">This error is often caused by a typographical error in an SQL SELECT statement.</span></span> <span data-ttu-id="3c477-118">Например ошибочным поля имя или имя таблицы можно создать эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="3c477-118">For example, a misspelled field name or table name can generate this error.</span></span> <span data-ttu-id="3c477-119">Эта ошибка может возникнуть при поля или таблице с именем в операторе SELECT не существует в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="3c477-119">This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-121"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-122">Не удается открыть файл.</span><span class="sxs-lookup"><span data-stu-id="3c477-122">File could not be opened.</span></span> <span data-ttu-id="3c477-123">Было указано имя файла с ошибками, или файл были перемещены, переименованы или удалении.</span><span class="sxs-lookup"><span data-stu-id="3c477-123">A misspelled file name was specified, or a file has been moved, renamed, or deleted.</span></span> <span data-ttu-id="3c477-124">В сети диске временно недоступен или сетевой трафик, препятствующих подключения.</span><span class="sxs-lookup"><span data-stu-id="3c477-124">Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-126"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-127">Не удалось прочитать файл.</span><span class="sxs-lookup"><span data-stu-id="3c477-127">File could not be read.</span></span> <span data-ttu-id="3c477-128">Неправильно указано имя файла, возможно, файл был перемещен или удален или файл может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="3c477-128">The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-130"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-131">Запись в файл не удалось.</span><span class="sxs-lookup"><span data-stu-id="3c477-131">Write to file failed.</span></span> <span data-ttu-id="3c477-132">Закрытием файла и затем попытка записи в него, или файл поврежден.</span><span class="sxs-lookup"><span data-stu-id="3c477-132">You might have closed a file and then tried to write to it, or the file might be corrupted.</span></span> <span data-ttu-id="3c477-133">Если файл расположен на сетевого диска, временное состояние сети могут запретить запись сетевого диска.</span><span class="sxs-lookup"><span data-stu-id="3c477-133">If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-135"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-136"><strong>BOF</strong> или <strong>EOF</strong> имеет значение True или текущей запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="3c477-136">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="3c477-137">Запрошенная операция требует текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3c477-137">Requested operation requires a current record.</span></span> <span data-ttu-id="3c477-138">Предпринята попытка обновить записей с помощью <strong>Поиск</strong> или <strong>Seek</strong> поместите указатель записи к нужной записи.</span><span class="sxs-lookup"><span data-stu-id="3c477-138">An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record.</span></span> <span data-ttu-id="3c477-139">Если запись не найден, <strong>EOF</strong> будет иметь значение True.</span><span class="sxs-lookup"><span data-stu-id="3c477-139">If the record is not found, <strong>EOF</strong> will be True.</span></span> <span data-ttu-id="3c477-140">Эта ошибка могут также создаваться после неудачной <strong>AddNew</strong> или <strong>Удалить</strong> , так как отсутствует текущий запись при сбое эти методы.</span><span class="sxs-lookup"><span data-stu-id="3c477-140">This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-142"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-143">Операция не допускается в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="3c477-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-145"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-146">Заданный поставщик отличается от одной уже для использования.</span><span class="sxs-lookup"><span data-stu-id="3c477-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-148"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-149">Объект <strong>подключения</strong> не может быть закрыт явным образом в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3c477-149"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span> <span data-ttu-id="3c477-150">Объект <strong>подключения</strong> или <strong>набора записей</strong> , в настоящее время участвует в транзакции не может быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="3c477-150">A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed.</span></span> <span data-ttu-id="3c477-151">Вызовите <strong>RollbackTrans</strong> или <strong>CommitTrans</strong> перед закрытием объект.</span><span class="sxs-lookup"><span data-stu-id="3c477-151">Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-153"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-154">Объект или поставщик не может выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="3c477-154">The object or provider is not capable of performing the requested operation.</span></span> <span data-ttu-id="3c477-155">Некоторые операции зависят от версии определенного поставщика.</span><span class="sxs-lookup"><span data-stu-id="3c477-155">Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-157"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-158">Не удается найти элемента в коллекции, соответствующий запрошенные имя или порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="3c477-158">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span> <span data-ttu-id="3c477-159">Указано неправильное имя поля или таблицы.</span><span class="sxs-lookup"><span data-stu-id="3c477-159">An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-161"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-162">Объект уже присутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3c477-162">Object is already in collection.</span></span> <span data-ttu-id="3c477-163">Не удается добавить.</span><span class="sxs-lookup"><span data-stu-id="3c477-163">Cannot append.</span></span> <span data-ttu-id="3c477-164">Объект нельзя добавить в два раза одного семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="3c477-164">An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-166"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-167">Объект больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3c477-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-169"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-170">Приложение использует значение недопустимого типа для текущей операции.</span><span class="sxs-lookup"><span data-stu-id="3c477-170">Application uses a value of the wrong type for the current operation.</span></span> <span data-ttu-id="3c477-171">Возможно, предоставленные строку операции, требующей потока, например.</span><span class="sxs-lookup"><span data-stu-id="3c477-171">You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-173"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-174">Операция не допускается при закрытии объекта.</span><span class="sxs-lookup"><span data-stu-id="3c477-174">Operation is not allowed when the object is closed.</span></span> <span data-ttu-id="3c477-175"><strong>Подключение</strong> или <strong>набора записей</strong> был закрыт.</span><span class="sxs-lookup"><span data-stu-id="3c477-175">The <strong>Connection</strong> or <strong>Recordset</strong> has been closed.</span></span> <span data-ttu-id="3c477-176">Например некоторые другие подпрограммы закрытием глобальный объект.</span><span class="sxs-lookup"><span data-stu-id="3c477-176">For example, some other routine might have closed a global object.</span></span> <span data-ttu-id="3c477-177">Эта ошибка может запретить, обращаясь к свойству <strong>состояние</strong> перед выполнением операции.</span><span class="sxs-lookup"><span data-stu-id="3c477-177">You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-179"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-180">Операция не разрешена, когда объект открыт.</span><span class="sxs-lookup"><span data-stu-id="3c477-180">Operation is not allowed when the object is open.</span></span> <span data-ttu-id="3c477-181">Не удается открыть объект, который открыт.</span><span class="sxs-lookup"><span data-stu-id="3c477-181">An object that is open cannot be opened.</span></span> <span data-ttu-id="3c477-182">Не удается добавить поля open <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c477-182">Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-184"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-185">Не удается найти поставщика.</span><span class="sxs-lookup"><span data-stu-id="3c477-185">Provider cannot be found.</span></span> <span data-ttu-id="3c477-186">Она может быть установлено неправильно.</span><span class="sxs-lookup"><span data-stu-id="3c477-186">It may not be properly installed.</span></span> <span data-ttu-id="3c477-187">Имя поставщика может быть неправильно указано, указанного поставщика не может быть установлен на компьютере, где выполнение кода или установки может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="3c477-187">The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-189"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-190">Свойства <strong>ActiveConnection</strong> объекта <strong>набора записей</strong> , который содержит объект <strong>команды</strong> в качестве источника, нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="3c477-190">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed.</span></span> <span data-ttu-id="3c477-191">Приложения, попытка назначить новый объект <strong>подключения</strong> <strong>набора записей</strong> , который содержит объект <strong>команды</strong> в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="3c477-191">The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-193"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-194">Объект <strong>параметра</strong> определен неправильно.</span><span class="sxs-lookup"><span data-stu-id="3c477-194"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="3c477-195">Несогласованные или неполные сведения отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="3c477-195">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-197"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-198">Подключение не может использоваться для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="3c477-198">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="3c477-199">Он является закрытой или недопустимый в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="3c477-199">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-201"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-202">Невозможно выполнить операцию во время обработки событий.</span><span class="sxs-lookup"><span data-stu-id="3c477-202">Operation cannot be performed while processing event.</span></span> <span data-ttu-id="3c477-203">Операция не могут выполняться в обработчик событий, который вызывает событие еще раз.</span><span class="sxs-lookup"><span data-stu-id="3c477-203">An operation cannot be performed within an event handler that causes the event to fire again.</span></span> <span data-ttu-id="3c477-204">Например методы перемещения не должен вызываться из обработчика событий <strong>WillMove</strong> .</span><span class="sxs-lookup"><span data-stu-id="3c477-204">For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-206"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-207">Невозможно выполнить операцию во время выполнения асинхронно.</span><span class="sxs-lookup"><span data-stu-id="3c477-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-209"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-210">Операция отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="3c477-210">Operation has been canceled by the user.</span></span> <span data-ttu-id="3c477-211">Приложение называется <strong>CancelUpdate</strong> или метод <strong>CancelBatch</strong> и текущей операции было прервано.</span><span class="sxs-lookup"><span data-stu-id="3c477-211">The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-213"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-214">Не удается выполнить операцию при подключении асинхронно.</span><span class="sxs-lookup"><span data-stu-id="3c477-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-216"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-217">Координирование транзакций является недопустимым или не запущен.</span><span class="sxs-lookup"><span data-stu-id="3c477-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-219"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-220">Невозможно выполнить операцию во время не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c477-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-222"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-223">Параметры безопасности на данном компьютере запрещают доступ к источнику данных в другом домене.</span><span class="sxs-lookup"><span data-stu-id="3c477-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-225"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-226">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="3c477-226">For internal use only.</span></span> <span data-ttu-id="3c477-227">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="3c477-227">Don't use.</span></span> <span data-ttu-id="3c477-228">(Запись был включен для полноты.</span><span class="sxs-lookup"><span data-stu-id="3c477-228">(Entry was included for the sake of completeness.</span></span> <span data-ttu-id="3c477-229">Эта ошибка не должно быть в вашем коде.)</span><span class="sxs-lookup"><span data-stu-id="3c477-229">This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-231"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-232">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="3c477-232">For internal use only.</span></span> <span data-ttu-id="3c477-233">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="3c477-233">Don't use.</span></span> <span data-ttu-id="3c477-234">(Запись в включены для полноты.</span><span class="sxs-lookup"><span data-stu-id="3c477-234">(Entry included for the sake of completeness.</span></span> <span data-ttu-id="3c477-235">Эта ошибка не должно быть в вашем коде.)</span><span class="sxs-lookup"><span data-stu-id="3c477-235">This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-237"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-238">Данные значения конфликтует с ограничения целостности поля.</span><span class="sxs-lookup"><span data-stu-id="3c477-238">Data value conflicts with the integrity constraints of the field.</span></span> <span data-ttu-id="3c477-239">Новое значение для <strong>поля</strong> вызовет повторяющийся ключ.</span><span class="sxs-lookup"><span data-stu-id="3c477-239">A new value for a <strong>Field</strong> would cause a duplicate key.</span></span> <span data-ttu-id="3c477-240">Значение, которое forms одностороннего отношения между двумя записями может оказаться обновляемым.</span><span class="sxs-lookup"><span data-stu-id="3c477-240">A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-242"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-243">Имеющихся разрешений недостаточно не позволяет записи в поле.</span><span class="sxs-lookup"><span data-stu-id="3c477-243">Insufficient permission prevents writing to the field.</span></span> <span data-ttu-id="3c477-244">Пользователя, указанного в строке подключения не имеет разрешения, необходимые для записи в <strong>поле</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c477-244">The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-246"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-247">Значение данных слишком велик для представления по типу данных поля.</span><span class="sxs-lookup"><span data-stu-id="3c477-247">Data value is too large to be represented by the field data type.</span></span> <span data-ttu-id="3c477-248">Числовое значение, которое слишком велико для требуемого поля была назначена.</span><span class="sxs-lookup"><span data-stu-id="3c477-248">A numeric value that is too large for the intended field was assigned.</span></span> <span data-ttu-id="3c477-249">Например поле короткое целое число присвоено значение "длинное целое".</span><span class="sxs-lookup"><span data-stu-id="3c477-249">For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-251"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-252">Данные значения конфликтует с типом данных или ограничения поля.</span><span class="sxs-lookup"><span data-stu-id="3c477-252">Data value conflicts with the data type or constraints of the field.</span></span> <span data-ttu-id="3c477-253">Хранилище данных имеет ограничения проверок, которые отличаются в зависимости от значения <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="3c477-253">The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-255"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-256">Сбой преобразования, так как значение данных имеет знак, а тип данных поля, используемый поставщиком без знака.</span><span class="sxs-lookup"><span data-stu-id="3c477-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-258"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-259">Невозможно преобразовать значение данных по причине, отличной от несоответствия знака или данных переполнения.</span><span class="sxs-lookup"><span data-stu-id="3c477-259">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="3c477-260">Например, для преобразования будет усечено данных.</span><span class="sxs-lookup"><span data-stu-id="3c477-260">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-262"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-263">Значение данных не может быть задана или получена так, как тип данных поля неизвестно или должен недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="3c477-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-265"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-266">Запись не содержит это поле.</span><span class="sxs-lookup"><span data-stu-id="3c477-266">Record does not contain this field.</span></span> <span data-ttu-id="3c477-267">Указан неправильный поля имя или ссылка на поле не в коллекции <strong>полей</strong> текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3c477-267">An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-269"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-270">Исходный URL-адрес или родительский URL-адрес конечного не существует.</span><span class="sxs-lookup"><span data-stu-id="3c477-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="3c477-271">Нет опечатки в URL-адрес источника или назначения.</span><span class="sxs-lookup"><span data-stu-id="3c477-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="3c477-272">Может быть https://mysite/photo/myphoto.jpg при фактически должен иметь https://mysite/photos/myphoto.jpg вместо этого.</span><span class="sxs-lookup"><span data-stu-id="3c477-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="3c477-273">Ошибка ввода в URL-адрес родительского (в данном случае <em>фотографий</em> вместо <em>фотографии</em>) вызвала ошибку.</span><span class="sxs-lookup"><span data-stu-id="3c477-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-275"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-276">Недостаточно разрешений для доступа к дерево или поддерево.</span><span class="sxs-lookup"><span data-stu-id="3c477-276">Permissions are insufficient to access tree or subtree.</span></span> <span data-ttu-id="3c477-277">Пользователя, указанного в строке подключения не имеет соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="3c477-277">The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-279"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-280">URL-адрес содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="3c477-280">URL contains invalid characters.</span></span> <span data-ttu-id="3c477-281">Убедитесь в том, что URL-адрес введен правильно.</span><span class="sxs-lookup"><span data-stu-id="3c477-281">Make sure the URL is typed correctly.</span></span> <span data-ttu-id="3c477-282">URL-адрес, исходя из схемы, зарегистрированных для текущего поставщика (например, Internet публикации регистрируется поставщик для http).</span><span class="sxs-lookup"><span data-stu-id="3c477-282">The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-284"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-285">Объект, представленный указанным URL-адрес заблокирован один или несколько других процессов.</span><span class="sxs-lookup"><span data-stu-id="3c477-285">Object represented by the specified URL is locked by one or more other processes.</span></span> <span data-ttu-id="3c477-286">Дождитесь завершения процесса и повторите попытку выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="3c477-286">Wait until the process has finished and attempt the operation again.</span></span> <span data-ttu-id="3c477-287">Объект, который вы пытаетесь получить доступ был заблокирован другим пользователем или другим процессом в приложении.</span><span class="sxs-lookup"><span data-stu-id="3c477-287">The object you are trying to access has been locked by another user or by another process in your application.</span></span> <span data-ttu-id="3c477-288">Это наиболее могут возникнуть в многопользовательской среде.</span><span class="sxs-lookup"><span data-stu-id="3c477-288">This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-290"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-291">Невозможно выполнить операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="3c477-291">Copy operation cannot be performed.</span></span> <span data-ttu-id="3c477-292">Объект с именем, URL-адрес назначения уже существует.</span><span class="sxs-lookup"><span data-stu-id="3c477-292">Object named by destination URL already exists.</span></span> <span data-ttu-id="3c477-293">Укажите <strong>adCopyOverwrite</strong> объект.</span><span class="sxs-lookup"><span data-stu-id="3c477-293">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span> <span data-ttu-id="3c477-294">Если <strong>adCopyOverwrite</strong> не указан, при копировании файлов в каталоге, копии происходит сбой при попытке скопировать элемент, который уже существует в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="3c477-294">If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-296"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-297">Сервер не может завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="3c477-297">The server cannot complete the operation.</span></span> <span data-ttu-id="3c477-298">Возможно, сервер занят с других операций или не хватает ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c477-298">This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-300"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-301">Поставщик может найти запоминающее устройство, указанный в параметре URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="3c477-301">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="3c477-302">Убедитесь в том, что URL-адрес введен правильно.</span><span class="sxs-lookup"><span data-stu-id="3c477-302">Make sure the URL is typed correctly.</span></span> <span data-ttu-id="3c477-303">URL-адрес устройства хранения может быть неправильная, но эта ошибка может возникнуть по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="3c477-303">The URL of the storage device might be incorrect, but this error can occur for other reasons.</span></span> <span data-ttu-id="3c477-304">Устройство может работать в автономном режиме или большой объем сетевого трафика может запретить подключение от использовались.</span><span class="sxs-lookup"><span data-stu-id="3c477-304">The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-306"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-307">Невозможно выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="3c477-307">Operation cannot be performed.</span></span> <span data-ttu-id="3c477-308">Поставщик не удается получить достаточно дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="3c477-308">Provider cannot obtain enough storage space.</span></span> <span data-ttu-id="3c477-309">Не возможно достаточного количества оперативной памяти или места на жестком диске для временных файлов на сервере.</span><span class="sxs-lookup"><span data-stu-id="3c477-309">There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-311"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-312">URL-адрес источника и назначения выходит за рамки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3c477-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-314"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-315">Не удалось завершить операцию и состояние недоступна.</span><span class="sxs-lookup"><span data-stu-id="3c477-315">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="3c477-316">Поле может быть недоступна или не попытка выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="3c477-316">The field may be unavailable or the operation was not attempted.</span></span> <span data-ttu-id="3c477-317">Может измененного или удаленного поле, которое вы пытаетесь получить доступ к другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="3c477-317">Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-319"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-320">Запись с именем, этот URL-адрес не существует.</span><span class="sxs-lookup"><span data-stu-id="3c477-320">Record named by this URL does not exist.</span></span> <span data-ttu-id="3c477-321">При открытии файла с помощью объекта <strong>записи</strong> был неправильно имя файла и путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="3c477-321">While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-323"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-324">URL-адрес объекта, к удалению выходит за рамки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3c477-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-326"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-327">Операции требуется допустимый <strong>ParentCatalog</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c477-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-329"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-330">Подключение было запрещено.</span><span class="sxs-lookup"><span data-stu-id="3c477-330">Connection was denied.</span></span> <span data-ttu-id="3c477-331">Новое подключение запрошенный имеет разные характеристики, чем в уже используется.</span><span class="sxs-lookup"><span data-stu-id="3c477-331">The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-333"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-334">Не удалось обновить поля.</span><span class="sxs-lookup"><span data-stu-id="3c477-334">Fields update failed.</span></span> <span data-ttu-id="3c477-335">Для получения дополнительных сведений проверьте свойство <strong>Status</strong> объектов отдельного поля.</span><span class="sxs-lookup"><span data-stu-id="3c477-335">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span> <span data-ttu-id="3c477-336">Эта ошибка может возникнуть в двух случаях: при изменении значения объекта <strong>поля</strong> , изменение или Добавление записи в базу данных; и при изменении свойств сам объект <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="3c477-336">This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself.</span></span> <span data-ttu-id="3c477-337">Не удалось обновить <strong>записи</strong> или <strong>записей</strong> из-за проблем с одного из полей в текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3c477-337">The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record.</span></span> <span data-ttu-id="3c477-338">Перечисление коллекции <strong>полей</strong> и проверьте <strong>состояние</strong> свойство каждое поле, чтобы определить причину проблемы.</span><span class="sxs-lookup"><span data-stu-id="3c477-338">Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c477-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-340"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-341">Поставщик не поддерживает ограничения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="3c477-341">Provider does not support sharing restrictions.</span></span> <span data-ttu-id="3c477-342">Предпринята попытка для ограничения доступа к файлам и ваш поставщик поддерживает концепцию.</span><span class="sxs-lookup"><span data-stu-id="3c477-342">An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c477-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-344"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="3c477-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="3c477-345">Поставщик не поддерживает запрошенный тип общего доступа к ограничение.</span><span class="sxs-lookup"><span data-stu-id="3c477-345">Provider does not support the requested kind of sharing restriction.</span></span> <span data-ttu-id="3c477-346">Предпринята попытка установить определенный тип доступа к файлам ограничение, которое не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3c477-346">An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider.</span></span> <span data-ttu-id="3c477-347">В документации поставщика для определения поддерживаются ограничения доступа к файлам.</span><span class="sxs-lookup"><span data-stu-id="3c477-347">See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

