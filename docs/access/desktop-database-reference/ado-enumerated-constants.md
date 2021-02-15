---
title: Перечислимые константы ADO
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05e5d3a77dc7db5ef5a0d81a3f13d5fc5987f5de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283410"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="634b9-102">Перечислимые константы ADO</span><span class="sxs-lookup"><span data-stu-id="634b9-102">ADO enumerated constants</span></span>

<span data-ttu-id="634b9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="634b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="634b9-104">Для отладки в списках ADO перечисляются значения для каждой константы.</span><span class="sxs-lookup"><span data-stu-id="634b9-104">To assist in debugging, the ADO enumerations list a value for each constant.</span></span> <span data-ttu-id="634b9-105">Однако это значение является исключительно рекомендациями и может измениться с одного выпуска ADO на другой.</span><span class="sxs-lookup"><span data-stu-id="634b9-105">However, this value is purely advisory, and may change from one release of ADO to another.</span></span> <span data-ttu-id="634b9-106">Код должен зависеть только от имени, а не фактического значения каждой константы.</span><span class="sxs-lookup"><span data-stu-id="634b9-106">Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="634b9-107">Enumerated constant</span><span class="sxs-lookup"><span data-stu-id="634b9-107">Enumerated constant</span></span></th>
<th><span data-ttu-id="634b9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="634b9-108">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="634b9-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-110">Для объекта RDS <strong>Recordset</strong> указывает приоритет выполнения асинхронного потока, который извлекает данные.</span><span class="sxs-lookup"><span data-stu-id="634b9-110">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="634b9-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-112">Указывает, когда поставщик <strong>MSDataShape</strong> повторно вычисляет сводные и вычисляемые столбцы в иерархическом <strong>наборе записей.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-112">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="634b9-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-114">Указывает, какие поля можно использовать для обнаружения конфликтов во время оптимистичного обновления строки источника данных с <strong>объектом Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-114">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="634b9-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-116">Указывает, следует ли за <strong>методом UpdateBatch</strong> неявную операцию метода <strong>Resync</strong> и, если да, область этой операции.</span><span class="sxs-lookup"><span data-stu-id="634b9-116">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-117"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-117"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-118">Указывает, на какие записи влияет операция.</span><span class="sxs-lookup"><span data-stu-id="634b9-118">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-119"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-119"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-120">Указывает закладку, указывающее место начала операции.</span><span class="sxs-lookup"><span data-stu-id="634b9-120">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-122">Указывает, как следует интерпретировать аргумент команды.</span><span class="sxs-lookup"><span data-stu-id="634b9-122">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-123"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-123"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-124">Указывает относительное положение двух записей, представленных закладки.</span><span class="sxs-lookup"><span data-stu-id="634b9-124">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-126">Указывает доступные разрешения для изменения данных в <strong>connection,</strong>открытия записи или указания значений для свойства <strong>Mode</strong> объектов <strong>Record</strong> и <strong>Stream.</strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="634b9-126">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-128">Указывает, должен ли метод <strong>Open</strong> объекта <strong>Connection</strong> возвращаться после (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="634b9-128">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-130">Указывает, должно ли отображаться диалоговое окно с запросом отсутствующих параметров при открытии подключения к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="634b9-130">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-132">Указывает поведение метода <strong>CopyRecord.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-132">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-134">Указывает расположение курсора.</span><span class="sxs-lookup"><span data-stu-id="634b9-134">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-136">Указывает, для каких <strong></strong> функций должен тестироваться метод Supports.</span><span class="sxs-lookup"><span data-stu-id="634b9-136">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-138">Указывает тип курсора, используемого в <strong>объекте Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-138">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-139"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-139"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-140">Указывает тип данных <strong>поля,</strong> <strong>параметра</strong>или <strong>свойства.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-140">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-141"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-141"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-142">Указывает состояние редактирования записи.</span><span class="sxs-lookup"><span data-stu-id="634b9-142">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-144">Указывает тип ошибки во время работы ADO.</span><span class="sxs-lookup"><span data-stu-id="634b9-144">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-145"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-145"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-146">Указывает причину возникновения события.</span><span class="sxs-lookup"><span data-stu-id="634b9-146">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-147"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-147"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-148">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="634b9-148">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-150">Указывает, как поставщик должен выполнять команду.</span><span class="sxs-lookup"><span data-stu-id="634b9-150">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-151"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-151"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-152">Указывает специальные поля, на которые ссылается коллекция <strong>Fields</strong> объекта <strong>Record.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-152">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-154">Указывает один или несколько атрибутов объекта <strong>Field.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-154">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-156">Указывает состояние объекта <strong>Field.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-156">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-158">Указывает группу записей, которые необходимо отфильтровать из <strong>наборов записей.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-158">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-160">Указывает количество записей, извлекаемого из <strong>recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-160">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-162">Указывает уровень изоляции транзакций для объекта <strong>Connection.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-162">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-164">Указывает символ, используемый в качестве деспаратора строк в текстовых <strong>объектах Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-164">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-165"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-165"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-166">Указывает тип блокировки записей во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="634b9-166">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-168">Указывает, какие записи должны быть возвращены на сервер.</span><span class="sxs-lookup"><span data-stu-id="634b9-168">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-170">Указывает поведение метода <strong></strong> <strong>MoveRecord</strong> объекта Record.</span><span class="sxs-lookup"><span data-stu-id="634b9-170">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-171"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-171"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-172">Указывает, является ли объект открытым или закрытым, подключением к источнику данных, выполнением команды или извлечением данных.</span><span class="sxs-lookup"><span data-stu-id="634b9-172">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-174">Указывает атрибуты объекта <strong>Parameter.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-174">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-176">Указывает, является <strong></strong> ли параметр входным параметром, выходным параметром или и тем, и другим, или является ли параметр возвращаемой величиной из хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="634b9-176">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-177"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-177"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-178">Указывает формат, в котором необходимо сохранить <strong>набор записей.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-178">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-179"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-179"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-180">Указывает текущую позицию указателя записи в <strong>наборе записей.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-180">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-182">Указывает атрибуты объекта <strong>Property.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-182">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-184">Указывает для метода Open <strong>объекта</strong> <strong>Record,</strong> следует ли открывать существующую <strong></strong> запись или создавать новую запись. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="634b9-184">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-186">Указывает параметры открытия <strong>записи.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-186">Specifies options for opening a <strong>Record</strong>.</span></span> <span data-ttu-id="634b9-187">Эти значения могут быть объединены с помощью оператора OR.</span><span class="sxs-lookup"><span data-stu-id="634b9-187">These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-189">Указывает состояние записи в отношении пакетных обновлений и других массовых операций.</span><span class="sxs-lookup"><span data-stu-id="634b9-189">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-191">Указывает тип объекта <strong>Record.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-191">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-192"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-192"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-193">Указывает, перезаписываются ли значения в результате вызова <strong>Resync.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-193">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-195">Указывает, следует ли создавать или перезаписывать файл при сохранении из <strong>объекта Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-195">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object.</span></span> <span data-ttu-id="634b9-196">Значения можно объединить с оператором AND.</span><span class="sxs-lookup"><span data-stu-id="634b9-196">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-197"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-197"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-198">Указывает тип наборов <strong>записей</strong> схемы, извлекаемого <strong>методом OpenSchema.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-198">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves.</span></span> <span data-ttu-id="634b9-199">Указывает направление поиска записей в <strong>наборе записей.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-199">Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-201">Указывает направление поиска записей в <strong>наборе записей.</strong> Указывает тип seek <strong>для</strong> выполнения.</span><span class="sxs-lookup"><span data-stu-id="634b9-201">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-202"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-202"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-203">Указывает тип seek <strong>для</strong> выполнения. Указывает параметры открытия объекта <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-203">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="634b9-204">Значения можно объединить с оператором AND.</span><span class="sxs-lookup"><span data-stu-id="634b9-204">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-206">Указывает параметры открытия объекта <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-206">Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="634b9-207">Значения можно объединить с оператором AND. Указывает, следует ли читать весь поток или следующую строку из <strong>объекта Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-207">The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-208"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-208"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-209">Указывает, следует ли читать весь поток или следующую строку из <strong>объекта Stream.</strong> Указывает тип данных, хранимых в <strong>объекте Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-209">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-211">Указывает тип данных, хранимых в <strong>объекте Stream.</strong> Указывает, будет ли к строке, записанной в объект Stream, будет ли к строке, записанной в <strong>объект Stream, будет ли сепаратор строки.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-211">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-213">Указывает, будет ли к строке, записанной в объект Stream, будет ли к строке, записанной в <strong>объект Stream, будет ли сепаратор строки.</strong> Указывает формат при искомом наборе <strong>записей в</strong> виде строки.</span><span class="sxs-lookup"><span data-stu-id="634b9-213">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634b9-214"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-214"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-215">Указывает формат при искомом наборе <strong>записей в</strong> виде строки. Указывает атрибуты транзакции объекта <strong>Connection.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-215">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634b9-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="634b9-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="634b9-217">Указывает атрибуты транзакции объекта <strong>Connection.</strong></span><span class="sxs-lookup"><span data-stu-id="634b9-217">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

