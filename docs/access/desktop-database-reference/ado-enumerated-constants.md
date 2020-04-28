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
# <a name="ado-enumerated-constants"></a><span data-ttu-id="4b5eb-102">Перечислимые константы ADO</span><span class="sxs-lookup"><span data-stu-id="4b5eb-102">ADO enumerated constants</span></span>

<span data-ttu-id="4b5eb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b5eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b5eb-104">Для облегчения отладки перечисление ADO перечислит значения для каждой константы.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-104">To assist in debugging, the ADO enumerations list a value for each constant.</span></span> <span data-ttu-id="4b5eb-105">Однако это значение является исключительно рекомендацией и может изменяться от одного выпуска ADO к другому.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-105">However, this value is purely advisory, and may change from one release of ADO to another.</span></span> <span data-ttu-id="4b5eb-106">Код должен зависеть только от имени (а не фактического значения) каждой перечислимой константы.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-106">Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="4b5eb-107">Перечислимая константа</span><span class="sxs-lookup"><span data-stu-id="4b5eb-107">Enumerated constant</span></span></th>
<th><span data-ttu-id="4b5eb-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4b5eb-108">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-110">Для объекта <strong>RECORDSET</strong> RDS указывает приоритет выполнения асинхронного потока, который получает данные.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-110">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-112">Указывает, когда поставщик <strong>мсдаташапе</strong> выполняет повторное вычисление статистических и вычисляемых столбцов в иерархическом <strong>наборе записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-112">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-114">Указывает, какие поля можно использовать для обнаружения конфликтов во время оптимистического обновления строки источника данных с помощью объекта <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-114">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-116">Указывает, следует ли метод <strong>UpdateBatch</strong> выполнить неявную операцию метода <strong>Resync</strong> и, если это так, область этой операции.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-116">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-117"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-117"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-118">Указывает, какие записи затрагиваются операцией.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-118">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-119"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-119"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-120">Указывает на закладку, указывающую, где должна начинаться операция.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-120">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-122">Указывает, как должен интерпретироваться аргумент команды.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-122">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-123"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-123"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-124">Задает относительное положение двух записей, представленных в закладках.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-124">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-126">Указывает доступные разрешения для изменения данных в <strong>подключении</strong>, открытия <strong>записи</strong>или указания значений для свойства <strong>mode</strong> объектов <strong>Record</strong> и <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-126">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-128">Указывает, должен ли метод <strong>Open</strong> объекта <strong>Connection</strong> возвращаться (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-128">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-130">Указывает, следует ли отображать диалоговое окно с запросом на отсутствие параметров при открытии подключения к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-130">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-132">Задает поведение метода <strong>CopyRecord</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-132">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-134">Указывает расположение обработчика курсора.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-134">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-136">Определяет, для каких функциональных возможностей метод <strong>поддерживает</strong> проверку.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-136">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-138">Указывает тип курсора, используемого в объекте <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-138">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-139"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-139"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-140">Указывает тип данных <strong>поля</strong>, <strong>параметра</strong>или <strong>Свойства</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-140">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-141"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-141"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-142">Задает состояние редактирования записи.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-142">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-144">Задает тип ошибки времени выполнения ADO.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-144">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-145"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-145"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-146">Указывает причину, по которой возникло событие.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-146">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-147"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-147"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-148">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-148">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-150">Указывает, как поставщик должен выполнять команду.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-150">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-151"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-151"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-152">Указывает специальные поля, указанные в коллекции <strong>Fields</strong> объекта <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-152">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-154">Задает один или несколько атрибутов объекта <strong>field</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-154">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-156">Задает состояние объекта <strong>field</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-156">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-158">Задает группу записей для фильтрации из <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-158">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-160">Указывает количество записей, извлекаемых из <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-160">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-162">Задает уровень изоляции транзакции для объекта <strong>подключения</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-162">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-164">Указывает символ, используемый в качестве разделителя строк в текстовых объектах <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-164">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-165"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-165"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-166">Указывает тип блокировки, помещаемой в записи во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-166">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-168">Указывает, какие записи должны возвращаться на сервер.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-168">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-170">Задает поведение метода <strong>MoveRecord</strong> объекта <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-170">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-171"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-171"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-172">Указывает, является ли объект открытым или закрытым, подключается к источнику данных, выполняя команду или извлечение данных.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-172">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-174">Задает атрибуты объекта <strong>Parameter</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-174">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-176">Указывает, представляет ли <strong>параметр</strong> входной параметр, выходной параметр или и то, и другое, если параметр является возвращаемым значением из хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-176">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-177"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-177"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-178">Задает формат, в котором будет сохранен <strong>набор записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-178">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-179"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-179"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-180">Задает текущее положение указателя записи в <strong>наборе записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-180">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-182">Задает атрибуты объекта <strong>Property</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-182">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-184">Указывает, следует ли открыть существующую <strong>запись</strong> в методе <strong>Open</strong> объекта <strong>Record</strong> или создать новую <strong>запись</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-184">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-186">Задает параметры открытия <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-186">Specifies options for opening a <strong>Record</strong>.</span></span> <span data-ttu-id="4b5eb-187">Эти значения можно объединять с помощью оператора OR.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-187">These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-189">Указывает состояние записи по отношению к пакетным обновлениям и другим массовым операциям.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-189">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-191">Указывает тип объекта <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-191">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-192"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-192"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-193">Указывает, перезаписываются ли базовые значения при вызове метода повторной <strong>синхронизации</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-193">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-195">Указывает, следует ли создать или перезаписать файл при сохранении из объекта <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-195">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object.</span></span> <span data-ttu-id="4b5eb-196">Значения можно сочетать с помощью оператора AND.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-196">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-197"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-197"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-198">Указывает тип <strong>набора записей</strong> схемы, извлекаемый методом <strong>OpenSchema</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-198">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves.</span></span> <span data-ttu-id="4b5eb-199">Задает направление поиска записи в <strong>наборе записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-199">Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-201">Задает направление поиска записи в <strong>наборе записей</strong>. Указывает тип выполняемого <strong>поиска</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-201">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-202"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-202"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-203">Указывает тип выполняемого <strong>поиска</strong> . Задает параметры открытия объекта <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-203">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="4b5eb-204">Значения можно сочетать с помощью оператора AND.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-204">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-206">Задает параметры открытия объекта <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-206">Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="4b5eb-207">Значения можно сочетать с помощью оператора AND. Указывает, следует ли считывать весь поток или следующую строку из объекта <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-207">The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-208"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-208"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-209">Указывает, следует ли считывать весь поток или следующую строку из объекта <strong>Stream</strong> . Указывает тип данных, хранящихся в объекте <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-209">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-211">Указывает тип данных, хранящихся в объекте <strong>Stream</strong> . Указывает, добавляется ли разделитель строк в строку, записанную в объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-211">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-213">Указывает, добавляется ли разделитель строк в строку, записанную в объект <strong>Stream</strong> . Задает формат при получении объекта <strong>Recordset</strong> в виде строки.</span><span class="sxs-lookup"><span data-stu-id="4b5eb-213">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5eb-214"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-214"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-215">Задает формат при получении объекта <strong>Recordset</strong> в виде строки. Задает атрибуты транзакции для объекта <strong>Connection</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-215">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5eb-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="4b5eb-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="4b5eb-217">Задает атрибуты транзакции для объекта <strong>Connection</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b5eb-217">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

