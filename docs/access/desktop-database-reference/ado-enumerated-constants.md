---
title: Перечислимые константы ADO
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0e6a6dee6d2882b1d7d1c277584ca8ba46d6db28
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910952"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="3bdb2-102">Перечислимые константы ADO</span><span class="sxs-lookup"><span data-stu-id="3bdb2-102">ADO enumerated constants</span></span>

<span data-ttu-id="3bdb2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bdb2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bdb2-104">Чтобы помочь в отладке, перечислений ADO списка значение для каждого константу.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-104">To assist in debugging, the ADO enumerations list a value for each constant.</span></span> <span data-ttu-id="3bdb2-105">Тем не менее это значение исключительно рекомендации и может измениться в разных выпусках ADO в другую.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-105">However, this value is purely advisory, and may change from one release of ADO to another.</span></span> <span data-ttu-id="3bdb2-106">Код должен только зависят от имени, а не фактические значения каждого перечисляемые константы.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-106">Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="3bdb2-107">Константа перечисления</span><span class="sxs-lookup"><span data-stu-id="3bdb2-107">Enumerated constant</span></span></th>
<th><span data-ttu-id="3bdb2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3bdb2-108">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-110">Объект служб удаленных рабочих СТОЛОВ <strong>записей</strong> указывает приоритет выполнения асинхронного потока, который получает данные.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-110">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-112">Указывает, когда поставщик <strong>MSDataShape</strong> повторно вычисляет статистические и вычисляемые столбцы в иерархической <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-112">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-114">Задает поля, которые можно использовать для определения конфликтов при обновлении оптимистичный строки из источника данных с помощью объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-114">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-116">Указывает, будет ли метод <strong>UpdateBatch</strong> следуют неявных <strong>выполнить повторную синхронизацию</strong> метод операции и, если да, области действия этой операции.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-116">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-117"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-117"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-118">Указывает, какие записи, влияют операции.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-118">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-119"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-119"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-120">Указывает, указывающее, где следует начать операцию закладку.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-120">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-122">Указывает, как интерпретировать аргумент команды.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-122">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-123"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-123"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-124">Задает относительное положение двух записей, представленное закладок.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-124">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-126">Задает разрешения, доступные для изменения данных в <strong>подключения</strong>, открытие <strong>записи</strong>или указания значения для свойства <strong>режима</strong> объектов <strong>потока</strong> и <strong>запись</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-126">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-128">Указывает, должен ли возвращать метод <strong>Open</strong> объекта <strong>подключения</strong> после (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-128">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-130">Указывает, следует ли отображать диалоговое окно запрашивать отсутствующие параметры при открытии подключения к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-130">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-132">Задает поведение метода <strong>CopyRecord</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-132">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-134">Указывает расположение обработчика курсора.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-134">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-136">Указывает, какие функции <strong>поддерживает</strong> метод, следует проверить наличие.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-136">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-138">Указывает тип курсора, используемого в объекте <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-138">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-139"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-139"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-140">Указывает тип данных <strong>параметра</strong>, <strong>поля</strong>или <strong>Свойства</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-140">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-141"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-141"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-142">Указывает состояние редактирования записи.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-142">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-144">Указывает тип ADO ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-144">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-145"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-145"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-146">Указывает причину, вызвавшего событие будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-146">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-147"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-147"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-148">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-148">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-150">Указывает, как поставщик должен выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-150">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-151"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-151"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-152">Задает особых полей, указанных в коллекции <strong>полей</strong> объект <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-152">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-154">Задает один или несколько атрибутов объекта <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-154">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-156">Указывает состояние объекта <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-156">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-158">Указывает группу записей для фильтрации из <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-158">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-160">Указывает количество записей для извлечения из <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-160">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-162">Указывает уровень изоляции транзакций для объекта <strong>подключения</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-162">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-164">Указывает символ, используемый в качестве разделителя строки в объектах <strong>потока</strong> текста.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-164">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-165"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-165"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-166">Указывает тип блокировки, помещенные на записей во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-166">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-168">Указывает, какие записи должны быть возвращены на сервер.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-168">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-170">Задает поведение объекта <strong>записи</strong> метод <strong>MoveRecord</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-170">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-171"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-171"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-172">Указывает, является ли объект открытой или закрытой, подключение к источнику данных, выполнение команды или извлечение данных.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-172">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-174">Определяет атрибуты объект <strong>параметра</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-174">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-176">Задает <strong>параметр</strong> представляет входного параметра и выходной параметр, или если параметр имеет значение, возвращаемое хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-176">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-177"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-177"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-178">Задает формат для сохранения <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-178">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-179"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-179"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-180">Указывает текущую позицию указателя записи в наборе <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-180">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-182">Указывает атрибуты <strong>Свойства</strong> объекта.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-182">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-184">Указывает метод <strong>Open</strong> объекта <strong>записи</strong> ли открывать существующей <strong>записи</strong> или новую <strong>запись</strong> должен быть создан.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-184">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-186">Задает параметры открытия для <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-186">Specifies options for opening a <strong>Record</strong>.</span></span> <span data-ttu-id="3bdb2-187">Эти значения можно объединять с помощью оператора OR.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-187">These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-189">Указывает состояние записи по отношению к пакета обновлений и других массовых операций.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-189">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-191">Указывает тип объекта <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-191">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-192"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-192"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-193">Указывает, будут перезаписаны ли базовых значений с помощью вызова <strong>выполнить повторную синхронизацию</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-193">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-195">Указывает, создан или перезаписан при сохранении из объекта <strong>потока</strong> файла.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-195">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object.</span></span> <span data-ttu-id="3bdb2-196">Значения может использоваться совместно с оператора AND.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-196">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-197"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-197"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-198">Указывает тип схемы <strong>OpenSchema</strong> метод извлекает <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-198">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves.</span></span> <span data-ttu-id="3bdb2-199">Задает направление поиска записи в наборе <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-199">Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-201">Задает направление поиска записи в наборе <strong>записей</strong>. Указывает тип <strong>поиска</strong> для выполнения.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-201">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-202"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-202"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-203">Указывает тип <strong>поиска</strong> для выполнения. Задает параметры открытия объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-203">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="3bdb2-204">Значения может использоваться совместно с оператора AND.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-204">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-206">Задает параметры открытия объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-206">Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="3bdb2-207">Значения может использоваться совместно с оператора AND. Указывает, следует ли считывать весь поток или следующую строку из объекта <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-207">The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-208"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-208"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-209">Указывает, следует ли считывать весь поток или следующую строку из объекта <strong>потока</strong> . Указывает тип данных, сохраненных в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-209">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-211">Указывает тип данных, сохраненных в объект <strong>потока</strong> . Указывает, добавлены ли разделитель к строке, записанные в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-211">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-213">Указывает, добавлены ли разделитель к строке, записанные в объект <strong>потока</strong> . Задает формат при извлечении <strong>набора записей</strong> как строку.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-213">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bdb2-214"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-214"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-215">Задает формат при извлечении <strong>набора записей</strong> как строку. Задает атрибуты транзакций объект <strong>подключения</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-215">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bdb2-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3bdb2-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3bdb2-217">Задает атрибуты транзакций объект <strong>подключения</strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb2-217">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

