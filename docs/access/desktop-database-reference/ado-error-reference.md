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
# <a name="ado-error-reference"></a><span data-ttu-id="5898e-102">Справочник по ошибкам ADO</span><span class="sxs-lookup"><span data-stu-id="5898e-102">ADO error reference</span></span>

<span data-ttu-id="5898e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5898e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5898e-104">Константа **еррорвалуинум** описывает значения ошибок ADO.</span><span class="sxs-lookup"><span data-stu-id="5898e-104">The **ErrorValueEnum** constant describes the ADO error values.</span></span> <span data-ttu-id="5898e-105">Полный список этих перечислимых констант, в том числе значений, приведен в разделе [приложение б: ошибки ADO](appendix-b-ado-errors.md).</span><span class="sxs-lookup"><span data-stu-id="5898e-105">For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md).</span></span> <span data-ttu-id="5898e-106">В этом разделе рассматриваются некоторые интересные ошибки и описываются некоторые конкретные ситуации, которые могут порождать их, а также решения для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="5898e-106">This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem.</span></span> <span data-ttu-id="5898e-107">В списке указаны константа **еррорвалуинум** и короткое положительное десятичное число.</span><span class="sxs-lookup"><span data-stu-id="5898e-107">Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5898e-108">Номер</span><span class="sxs-lookup"><span data-stu-id="5898e-108">Number</span></span></p></th>
<th><p><span data-ttu-id="5898e-109">Константа Еррорвалуинум</span><span class="sxs-lookup"><span data-stu-id="5898e-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="5898e-110">Описание/возможные причины</span><span class="sxs-lookup"><span data-stu-id="5898e-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5898e-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-112"><strong>Адеррпровидерфаилед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-113">Поставщику не удалось выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="5898e-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-115"><strong>Адерринвалидаргумент</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-116">Аргументы имеют неверный тип, выходят за пределы допустимого диапазона или конфликтуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="5898e-116">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span> <span data-ttu-id="5898e-117">Эта ошибка часто возникает из-за опечатки в операторе SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="5898e-117">This error is often caused by a typographical error in an SQL SELECT statement.</span></span> <span data-ttu-id="5898e-118">Например, эта ошибка может возникать, если имя поля или имя таблицы с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5898e-118">For example, a misspelled field name or table name can generate this error.</span></span> <span data-ttu-id="5898e-119">Эта ошибка также может возникать, если поле или таблица, указанные в операторе SELECT, не существуют в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="5898e-119">This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-121"><strong>Адерропенингфиле</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-122">Не удалось открыть файл.</span><span class="sxs-lookup"><span data-stu-id="5898e-122">File could not be opened.</span></span> <span data-ttu-id="5898e-123">Указано неправильное имя файла, или файл был перемещен, переименован или удален.</span><span class="sxs-lookup"><span data-stu-id="5898e-123">A misspelled file name was specified, or a file has been moved, renamed, or deleted.</span></span> <span data-ttu-id="5898e-124">По сети диск может быть временно недоступен или сетевой трафик может препятствовать подключению.</span><span class="sxs-lookup"><span data-stu-id="5898e-124">Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-126"><strong>Адеррреадфиле</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-127">Не удалось прочитать файл.</span><span class="sxs-lookup"><span data-stu-id="5898e-127">File could not be read.</span></span> <span data-ttu-id="5898e-128">Имя файла указано неправильно, файл мог быть перемещен или удален, либо файл поврежден.</span><span class="sxs-lookup"><span data-stu-id="5898e-128">The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-130"><strong>Адеррвритефиле</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-131">Ошибка записи в файл.</span><span class="sxs-lookup"><span data-stu-id="5898e-131">Write to file failed.</span></span> <span data-ttu-id="5898e-132">Возможно, вы закрыли файл, а затем попытались выполнить запись в него, или файл поврежден.</span><span class="sxs-lookup"><span data-stu-id="5898e-132">You might have closed a file and then tried to write to it, or the file might be corrupted.</span></span> <span data-ttu-id="5898e-133">Если файл находится на сетевом диске, временные условия сети могут препятствовать записи на сетевой диск.</span><span class="sxs-lookup"><span data-stu-id="5898e-133">If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-135"><strong>Адеррнокуррентрекорд</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-136">Либо <strong>BOF</strong> , либо <strong>EOF</strong> имеет значение true, или текущая запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="5898e-136">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="5898e-137">Для выполнения запрошенной операции требуется текущая запись.</span><span class="sxs-lookup"><span data-stu-id="5898e-137">Requested operation requires a current record.</span></span> <span data-ttu-id="5898e-138">Предпринята попытка обновить записи с помощью команды <strong>Find</strong> или <strong>Seek</strong> , чтобы переместить указатель записи в нужную запись.</span><span class="sxs-lookup"><span data-stu-id="5898e-138">An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record.</span></span> <span data-ttu-id="5898e-139">Если запись не найдена, то <strong>EOF</strong> будет иметь значение true.</span><span class="sxs-lookup"><span data-stu-id="5898e-139">If the record is not found, <strong>EOF</strong> will be True.</span></span> <span data-ttu-id="5898e-140">Эта ошибка также может возникать после сбоя <strong>AddNew</strong> или <strong>Delete</strong> из-за отсутствия текущей записи при сбое этих методов.</span><span class="sxs-lookup"><span data-stu-id="5898e-140">This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-142"><strong>Адерриллегалоператион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-143">Операция не разрешена в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="5898e-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-145"><strong>Адерркантчанжепровидер</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-146">Указанный поставщик отличается от того, который уже используется.</span><span class="sxs-lookup"><span data-stu-id="5898e-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-148"><strong>Адерринтрансактион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-149">Объект <strong>Connection</strong> не может быть закрыт явным образом во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="5898e-149"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span> <span data-ttu-id="5898e-150">Объект <strong>Recordset</strong> или объект <strong>подключения</strong> , который в настоящее время участвует в транзакции, не может быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="5898e-150">A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed.</span></span> <span data-ttu-id="5898e-151">ВыЗовите <strong>RollbackTrans</strong> или <strong>CommitTrans</strong> перед закрытием объекта.</span><span class="sxs-lookup"><span data-stu-id="5898e-151">Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-153"><strong>Адеррфеатуренотаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-154">Объект или поставщик не могут выполнять запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="5898e-154">The object or provider is not capable of performing the requested operation.</span></span> <span data-ttu-id="5898e-155">Некоторые операции зависят от конкретной версии поставщика.</span><span class="sxs-lookup"><span data-stu-id="5898e-155">Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-157"><strong>Адерритемнотфаунд</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-158">Не удается найти элемент в семействе, соответствующем запрошенному имени или порядковому номеру.</span><span class="sxs-lookup"><span data-stu-id="5898e-158">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span> <span data-ttu-id="5898e-159">Указано неправильное имя поля или таблицы.</span><span class="sxs-lookup"><span data-stu-id="5898e-159">An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-161"><strong>Адерробжектинколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-162">Объект уже находится в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5898e-162">Object is already in collection.</span></span> <span data-ttu-id="5898e-163">Не удается добавить.</span><span class="sxs-lookup"><span data-stu-id="5898e-163">Cannot append.</span></span> <span data-ttu-id="5898e-164">Объект не может быть добавлен в одну и ту же коллекцию дважды.</span><span class="sxs-lookup"><span data-stu-id="5898e-164">An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-166"><strong>Адерробжектнотсет</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-167">Объект больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5898e-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-169"><strong>Адеррдатаконверсион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-170">Приложение использует значение неправильного типа для текущей операции.</span><span class="sxs-lookup"><span data-stu-id="5898e-170">Application uses a value of the wrong type for the current operation.</span></span> <span data-ttu-id="5898e-171">Возможно, вы задали строку для операции, которая ожидает поток, например.</span><span class="sxs-lookup"><span data-stu-id="5898e-171">You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-173"><strong>Адерробжектклосед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-174">Операция не разрешена при закрытии объекта.</span><span class="sxs-lookup"><span data-stu-id="5898e-174">Operation is not allowed when the object is closed.</span></span> <span data-ttu-id="5898e-175"><strong>Подключение</strong> или <strong>набор записей</strong> закрыты.</span><span class="sxs-lookup"><span data-stu-id="5898e-175">The <strong>Connection</strong> or <strong>Recordset</strong> has been closed.</span></span> <span data-ttu-id="5898e-176">Например, в некоторых других подпрограммах может быть закрыт глобальный объект.</span><span class="sxs-lookup"><span data-stu-id="5898e-176">For example, some other routine might have closed a global object.</span></span> <span data-ttu-id="5898e-177">Вы можете предотвратить эту ошибку, проверив свойство <strong>State</strong> перед попыткой выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="5898e-177">You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-179"><strong>Адерробжектопен</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-180">Операция не разрешена, если объект открыт.</span><span class="sxs-lookup"><span data-stu-id="5898e-180">Operation is not allowed when the object is open.</span></span> <span data-ttu-id="5898e-181">Не удается открыть открытый объект.</span><span class="sxs-lookup"><span data-stu-id="5898e-181">An object that is open cannot be opened.</span></span> <span data-ttu-id="5898e-182">Поля невозможно добавить в открытый <strong>набор записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="5898e-182">Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-184"><strong>Адеррпровидернотфаунд</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-185">Не удается найти поставщика.</span><span class="sxs-lookup"><span data-stu-id="5898e-185">Provider cannot be found.</span></span> <span data-ttu-id="5898e-186">Он может быть неправильно установлен.</span><span class="sxs-lookup"><span data-stu-id="5898e-186">It may not be properly installed.</span></span> <span data-ttu-id="5898e-187">Возможно, имя поставщика указано неправильно, указанный поставщик может не быть установлен на компьютере, на котором выполняется код, или в случае повреждения установки.</span><span class="sxs-lookup"><span data-stu-id="5898e-187">The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-189"><strong>Адеррбаундтокомманд</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-190">Свойство <strong>ActiveConnection</strong> объекта <strong>Recordset</strong> , который имеет объект <strong>Command</strong> в качестве источника, не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="5898e-190">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed.</span></span> <span data-ttu-id="5898e-191">Приложение попыталось назначить новый объект <strong>Connection</strong> для объекта <strong>Recordset</strong> , в качестве источника которого есть <strong>Командный</strong> объект.</span><span class="sxs-lookup"><span data-stu-id="5898e-191">The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-193"><strong>Адерринвалидпараминфо</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-194">Объект <strong>Parameter</strong> определен неправильно.</span><span class="sxs-lookup"><span data-stu-id="5898e-194"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="5898e-195">Предоставлены несогласованные или неполные сведения.</span><span class="sxs-lookup"><span data-stu-id="5898e-195">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-197"><strong>Адерринвалидконнектион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-198">Невозможно использовать соединение для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="5898e-198">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="5898e-199">Он либо закрывается, либо не является допустимым в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="5898e-199">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-201"><strong>Адеррнотринтрант</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-202">Не удается выполнить операцию во время обработки события.</span><span class="sxs-lookup"><span data-stu-id="5898e-202">Operation cannot be performed while processing event.</span></span> <span data-ttu-id="5898e-203">Операция не может быть выполнена в обработчике событий, что приводит к повторному срабатыванию события.</span><span class="sxs-lookup"><span data-stu-id="5898e-203">An operation cannot be performed within an event handler that causes the event to fire again.</span></span> <span data-ttu-id="5898e-204">Например, методы навигации не следует вызывать из обработчика событий <strong>события WillMove</strong> .</span><span class="sxs-lookup"><span data-stu-id="5898e-204">For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-206"><strong>Адеррстиллексекутинг</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-207">Не удается выполнить операцию во время асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="5898e-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-209"><strong>Адерроператионканцеллед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-210">Операция отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="5898e-210">Operation has been canceled by the user.</span></span> <span data-ttu-id="5898e-211">Приложение вызвало метод <strong>CancelUpdate</strong> или <strong>CancelBatch</strong> , и текущая операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="5898e-211">The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-213"><strong>Адеррстиллконнектинг</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-214">Не удается выполнить операцию во время асинхронного подключения.</span><span class="sxs-lookup"><span data-stu-id="5898e-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-216"><strong>Адерринвалидтрансактион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-217">Координация транзакции является недопустимой или не запущена.</span><span class="sxs-lookup"><span data-stu-id="5898e-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-219"><strong>Адеррнотексекутинг</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-220">Не удается выполнить операцию, пока не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5898e-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-222"><strong>Адеррунсафеоператион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-223">Параметры безопасности этого компьютера запрещают доступ к источнику данных в другом домене.</span><span class="sxs-lookup"><span data-stu-id="5898e-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-225"><strong>Адврнсекуритидиалог</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-226">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="5898e-226">For internal use only.</span></span> <span data-ttu-id="5898e-227">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="5898e-227">Don't use.</span></span> <span data-ttu-id="5898e-228">(Запись была включена в целях полноты.</span><span class="sxs-lookup"><span data-stu-id="5898e-228">(Entry was included for the sake of completeness.</span></span> <span data-ttu-id="5898e-229">Эта ошибка не должна отображаться в коде.)</span><span class="sxs-lookup"><span data-stu-id="5898e-229">This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-231"><strong>Адврнсекуритидиалогхеадер</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-232">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="5898e-232">For internal use only.</span></span> <span data-ttu-id="5898e-233">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="5898e-233">Don't use.</span></span> <span data-ttu-id="5898e-234">(Запись, включенная в целях полноты.</span><span class="sxs-lookup"><span data-stu-id="5898e-234">(Entry included for the sake of completeness.</span></span> <span data-ttu-id="5898e-235">Эта ошибка не должна отображаться в коде.)</span><span class="sxs-lookup"><span data-stu-id="5898e-235">This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-237"><strong>Адерринтегритивиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-238">Значение данных вступает в противоречие с ограничениями целостности поля.</span><span class="sxs-lookup"><span data-stu-id="5898e-238">Data value conflicts with the integrity constraints of the field.</span></span> <span data-ttu-id="5898e-239">Новое значение <strong>поля</strong> приведет к созданию повторяющегося ключа.</span><span class="sxs-lookup"><span data-stu-id="5898e-239">A new value for a <strong>Field</strong> would cause a duplicate key.</span></span> <span data-ttu-id="5898e-240">Значение, которое образует одну сторону отношения между двумя записями, может быть необновляемым.</span><span class="sxs-lookup"><span data-stu-id="5898e-240">A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-242"><strong>Адеррпермиссиондениед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-243">НеДостаточные разрешения не допускают запись в поле.</span><span class="sxs-lookup"><span data-stu-id="5898e-243">Insufficient permission prevents writing to the field.</span></span> <span data-ttu-id="5898e-244">Пользователь, указанный в строке подключения, не имеет соответствующих разрешений на запись в <strong>поле</strong>.</span><span class="sxs-lookup"><span data-stu-id="5898e-244">The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-246"><strong>Адеррдатаоверфлов</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-247">Слишком большое значение данных для представления типом данных поля.</span><span class="sxs-lookup"><span data-stu-id="5898e-247">Data value is too large to be represented by the field data type.</span></span> <span data-ttu-id="5898e-248">Числовое значение, слишком большое для предполагаемого поля, было назначено.</span><span class="sxs-lookup"><span data-stu-id="5898e-248">A numeric value that is too large for the intended field was assigned.</span></span> <span data-ttu-id="5898e-249">Например, длинное целое значение было назначено для поля short integer.</span><span class="sxs-lookup"><span data-stu-id="5898e-249">For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-251"><strong>Адеррсчемавиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-252">Значение данных вступает в противоречие с типом данных или ограничениями поля.</span><span class="sxs-lookup"><span data-stu-id="5898e-252">Data value conflicts with the data type or constraints of the field.</span></span> <span data-ttu-id="5898e-253">Для хранилища данных существуют ограничения проверки, отличные от значения <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="5898e-253">The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-255"><strong>Адеррсигнмисматч</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-256">Произошел сбой преобразования, так как значение данных было подписано, а тип данных поля, используемый поставщиком, не подписан.</span><span class="sxs-lookup"><span data-stu-id="5898e-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-258"><strong>Адерркантконвертвалуе</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-259">Значение данных не может быть преобразовано по причинам, отличным от несоответствия знака или переполнения данных.</span><span class="sxs-lookup"><span data-stu-id="5898e-259">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="5898e-260">Например, преобразование приведет к усечению данных.</span><span class="sxs-lookup"><span data-stu-id="5898e-260">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-262"><strong>Адеррканткреате</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-263">Значение данных не может быть задано или получено, так как тип данных поля неизвестен или у поставщика недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="5898e-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-265"><strong>Адеррколумннотонсисров</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-266">Запись не содержит это поле.</span><span class="sxs-lookup"><span data-stu-id="5898e-266">Record does not contain this field.</span></span> <span data-ttu-id="5898e-267">Было указано неправильное имя поля или в коллекции Fields <strong></strong> текущей записи есть ссылка.</span><span class="sxs-lookup"><span data-stu-id="5898e-267">An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-269"><strong>Адеррурлдоеснотексист</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-270">Либо исходный URL-адрес, либо родительский URL-адрес назначения не существует.</span><span class="sxs-lookup"><span data-stu-id="5898e-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="5898e-271">Ошибка в исходном или целевом URL-АДРЕСе.</span><span class="sxs-lookup"><span data-stu-id="5898e-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="5898e-272">Вы, возможно https://mysite/photo/myphoto.jpg , заХотите, чтобы https://mysite/photos/myphoto.jpg вы действительно хотите.</span><span class="sxs-lookup"><span data-stu-id="5898e-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="5898e-273">Ошибка опечатки в родительском URL-АДРЕСе (в данном случае <em>фотография</em> вместо <em>фотографий</em>) привела к ошибке.</span><span class="sxs-lookup"><span data-stu-id="5898e-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-275"><strong>Адерртрипермиссиондениед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-276">Недостаточно разрешений для доступа к дереву или поддереву.</span><span class="sxs-lookup"><span data-stu-id="5898e-276">Permissions are insufficient to access tree or subtree.</span></span> <span data-ttu-id="5898e-277">Пользователь, указанный в строке подключения, не имеет соответствующих разрешений.</span><span class="sxs-lookup"><span data-stu-id="5898e-277">The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-279"><strong>Адерринвалидурл</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-280">URL-адрес содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="5898e-280">URL contains invalid characters.</span></span> <span data-ttu-id="5898e-281">Убедитесь, что URL-адрес введен правильно.</span><span class="sxs-lookup"><span data-stu-id="5898e-281">Make sure the URL is typed correctly.</span></span> <span data-ttu-id="5898e-282">URL-адрес соответствует схеме, зарегистрированной для текущего поставщика (например, поставщик публикации в Интернете зарегистрирован для HTTP).</span><span class="sxs-lookup"><span data-stu-id="5898e-282">The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-284"><strong>Адеррресаурцелоккед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-285">Объект, представленный указанным URL-АДРЕСом, заблокирован одним или несколькими другими процессами.</span><span class="sxs-lookup"><span data-stu-id="5898e-285">Object represented by the specified URL is locked by one or more other processes.</span></span> <span data-ttu-id="5898e-286">ДоЖдитесь завершения процесса и повторите операцию.</span><span class="sxs-lookup"><span data-stu-id="5898e-286">Wait until the process has finished and attempt the operation again.</span></span> <span data-ttu-id="5898e-287">Объект, к которому вы пытаетесь получить доступ, заблокирован другим пользователем или другим процессом в приложении.</span><span class="sxs-lookup"><span data-stu-id="5898e-287">The object you are trying to access has been locked by another user or by another process in your application.</span></span> <span data-ttu-id="5898e-288">Скорее всего, это будет возникать в среде с несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="5898e-288">This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-290"><strong>Адеррресаурцеексистс</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-291">Не удается выполнить операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="5898e-291">Copy operation cannot be performed.</span></span> <span data-ttu-id="5898e-292">Объект с именем URL-адреса назначения уже существует.</span><span class="sxs-lookup"><span data-stu-id="5898e-292">Object named by destination URL already exists.</span></span> <span data-ttu-id="5898e-293">Укажите <strong>адкопйоверврите</strong> , чтобы заменить объект.</span><span class="sxs-lookup"><span data-stu-id="5898e-293">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span> <span data-ttu-id="5898e-294">Если вы не укажете <strong>адкопйоверврите</strong> при копировании файлов в каталоге, при попытке скопировать элемент, который уже существует в целевом расположении, произойдет сбой копирования.</span><span class="sxs-lookup"><span data-stu-id="5898e-294">If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-296"><strong>Адеррканноткомплете</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-297">Серверу не удается выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="5898e-297">The server cannot complete the operation.</span></span> <span data-ttu-id="5898e-298">Это может быть вызвано тем, что сервер занят с другими операциями или не хватает ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5898e-298">This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-300"><strong>Адеррволуменотфаунд</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-301">Поставщик не может определить устройство хранения данных, указанное с помощью URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5898e-301">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="5898e-302">Убедитесь, что URL-адрес введен правильно.</span><span class="sxs-lookup"><span data-stu-id="5898e-302">Make sure the URL is typed correctly.</span></span> <span data-ttu-id="5898e-303">URL-адрес устройства хранения может быть неправильным, но эта ошибка может возникать по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="5898e-303">The URL of the storage device might be incorrect, but this error can occur for other reasons.</span></span> <span data-ttu-id="5898e-304">Возможно, устройство отключено или большой объем сетевого трафика может препятствовать выполнению подключения.</span><span class="sxs-lookup"><span data-stu-id="5898e-304">The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-306"><strong>Адерраутофспаце</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-307">Не удается выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="5898e-307">Operation cannot be performed.</span></span> <span data-ttu-id="5898e-308">Поставщик не может получить достаточно места для хранения.</span><span class="sxs-lookup"><span data-stu-id="5898e-308">Provider cannot obtain enough storage space.</span></span> <span data-ttu-id="5898e-309">Недостаточно места на диске или на жестком диске для временных файлов на сервере.</span><span class="sxs-lookup"><span data-stu-id="5898e-309">There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-311"><strong>Адеррресаурцеаутофскопе</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-312">Исходный или конечный URL-адрес находится вне области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="5898e-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-314"><strong>Адеррунаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-315">Не удалось завершить операцию, состояние — недоступно.</span><span class="sxs-lookup"><span data-stu-id="5898e-315">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="5898e-316">Поле может быть недоступно или операция не была предпринята.</span><span class="sxs-lookup"><span data-stu-id="5898e-316">The field may be unavailable or the operation was not attempted.</span></span> <span data-ttu-id="5898e-317">Возможно, другой пользователь изменил или удалил поле, к которому вы пытаетесь получить доступ.</span><span class="sxs-lookup"><span data-stu-id="5898e-317">Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-319"><strong>Адеррурлнамедровдоеснотексист</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-320">Запись, указанная с помощью этого URL-адреса, не существует.</span><span class="sxs-lookup"><span data-stu-id="5898e-320">Record named by this URL does not exist.</span></span> <span data-ttu-id="5898e-321">При попытке открыть файл с помощью объекта <strong>Record</strong> либо имя файла, либо путь к файлу были написаны с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5898e-321">While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-323"><strong>Адеррделресаутофскопе</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-324">URL-адрес удаляемого объекта находится вне области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="5898e-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-326"><strong>Адерркаталогнотсет</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-327">Для операции требуется допустимый <strong>ParentCatalog</strong>.</span><span class="sxs-lookup"><span data-stu-id="5898e-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-329"><strong>Адерркантчанжеконнектион</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-330">Подключение было отклонено.</span><span class="sxs-lookup"><span data-stu-id="5898e-330">Connection was denied.</span></span> <span data-ttu-id="5898e-331">Новое запрошенное подключение имеет различные характеристики, чем оно уже используется.</span><span class="sxs-lookup"><span data-stu-id="5898e-331">The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-333"><strong>Адеррфиелдсупдатефаилед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-334">Не удалось обновить поля.</span><span class="sxs-lookup"><span data-stu-id="5898e-334">Fields update failed.</span></span> <span data-ttu-id="5898e-335">Для получения дополнительных сведений изучите свойство <strong>Status</strong> отдельных объектов Field.</span><span class="sxs-lookup"><span data-stu-id="5898e-335">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span> <span data-ttu-id="5898e-336">Эта ошибка может возникать в двух ситуациях: при изменении значения объекта <strong>field</strong> в процессе изменения или добавления записи в базу данных; и при изменении свойств самого объекта <strong>field</strong> .</span><span class="sxs-lookup"><span data-stu-id="5898e-336">This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself.</span></span> <span data-ttu-id="5898e-337">Не удалось выполнить обновление <strong>записи</strong> или <strong>набора записей</strong> из-за проблемы с одним из полей в текущей записи.</span><span class="sxs-lookup"><span data-stu-id="5898e-337">The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record.</span></span> <span data-ttu-id="5898e-338">ПереЧислите <strong></strong> коллекции Fields и проверьте свойство <strong>Status</strong> каждого поля, чтобы определить причину проблемы.</span><span class="sxs-lookup"><span data-stu-id="5898e-338">Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5898e-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-340"><strong>Адеррденинотсуппортед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-341">Поставщик не поддерживает ограничения на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="5898e-341">Provider does not support sharing restrictions.</span></span> <span data-ttu-id="5898e-342">Предпринята попытка ограничить общий доступ к файлам, а поставщик не поддерживает эту концепцию.</span><span class="sxs-lookup"><span data-stu-id="5898e-342">An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5898e-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-344"><strong>Адеррденитипенотсуппортед</strong></span><span class="sxs-lookup"><span data-stu-id="5898e-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="5898e-345">Поставщик не поддерживает запрошенный тип ограничения на совместное использование.</span><span class="sxs-lookup"><span data-stu-id="5898e-345">Provider does not support the requested kind of sharing restriction.</span></span> <span data-ttu-id="5898e-346">Предпринята попытка установить определенный тип ограничения совместного использования файлов, который не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="5898e-346">An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider.</span></span> <span data-ttu-id="5898e-347">Чтобы определить, какие ограничения общего доступа к файлам поддерживаются, обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="5898e-347">See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

