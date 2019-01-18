---
title: Метод Connection.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abbb7a4f58714aef0e085d0f37b5ee49378e0f51
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708881"
---
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="bf2a6-102">Метод Connection.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="bf2a6-102">Connection.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="bf2a6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf2a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf2a6-104">Создает новый объект **[набора записей](recordset-object-dao.md)** и добавляет его в коллекцию **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="bf2a6-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf2a6-105">Syntax</span></span>

<span data-ttu-id="bf2a6-106">*выражение* . OpenRecordset (***имя***, ***Тип***, ***Параметры***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="bf2a6-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="bf2a6-107">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="bf2a6-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf2a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf2a6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf2a6-109">Имя</span><span class="sxs-lookup"><span data-stu-id="bf2a6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="bf2a6-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="bf2a6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="bf2a6-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bf2a6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="bf2a6-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bf2a6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf2a6-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="bf2a6-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="bf2a6-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf2a6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="bf2a6-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="bf2a6-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2a6-116">Источник записей для нового <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-116">The source of the records for the new <strong>Recordset</strong>.</span></span> <span data-ttu-id="bf2a6-117">Источник может быть имя таблицы, имя запроса или инструкции SQL, которая возвращает записи.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-117">The source can be a table name, a query name, or an SQL statement that returns records.</span></span> <span data-ttu-id="bf2a6-118">Для объектов <strong>наборов записей</strong> в таблице типа в базами данных, ядро базы данных Microsoft Access источник может быть только имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-118">For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2a6-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="bf2a6-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="bf2a6-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="bf2a6-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="bf2a6-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="bf2a6-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2a6-122">Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> , указывающая тип <strong>набора записей</strong> , чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="bf2a6-123"><strong>Примечание</strong>: при открытии <strong>набора записей</strong> в рабочей области Microsoft Access и тип не указан, <strong>OpenRecordset</strong> создает табличного типа <strong>записей</strong>, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="bf2a6-124">При указании связанной таблицы или запроса, <strong>OpenRecordset</strong> создает добавляющий <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2a6-125"><em>Варианты</em></span><span class="sxs-lookup"><span data-stu-id="bf2a6-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="bf2a6-126">Необязательный</span><span class="sxs-lookup"><span data-stu-id="bf2a6-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="bf2a6-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="bf2a6-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2a6-128">Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> , которые задают характеристики нового <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="bf2a6-129"><strong>Примечание</strong>: константы <strong>dbConsistent</strong> и <strong>dbInconsistent</strong> являются взаимоисключающими и использовании обоих приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="bf2a6-130">Также указав аргумент lockedits параметров с помощью константу <strong>dbReadOnly</strong> приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-130">Supplying a lockedits argument when options use the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2a6-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="bf2a6-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="bf2a6-132">Необязательный</span><span class="sxs-lookup"><span data-stu-id="bf2a6-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="bf2a6-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="bf2a6-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2a6-134">Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> , определяющая блокировки для <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="bf2a6-135"><strong>Примечание</strong>: можно использовать <strong>dbReadOnly</strong> в аргументе параметры или аргумент lockedits, но не оба.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="bf2a6-136">При использовании обоих аргументов, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="bf2a6-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf2a6-137">Return value</span></span>

<span data-ttu-id="bf2a6-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="bf2a6-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="bf2a6-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="bf2a6-139">Remarks</span></span>

<span data-ttu-id="bf2a6-140">Как правило если пользователь получает Эта ошибка при обновлении записи, код должен обновить содержимое полей и извлечение измененные значения.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-140">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values.</span></span> <span data-ttu-id="bf2a6-141">Если ошибка возникает при удалении записи, кода удалось отобразить новые записи данных для пользователя и сообщение, указывающее, что недавно были изменены данные.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-141">If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed.</span></span> <span data-ttu-id="bf2a6-142">На этом этапе кода можно запросить подтверждения, что по-прежнему требуется удалить эту запись.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-142">At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="bf2a6-143">Константа **dbSeeChanges** также следует использовать при открытии **набора записей** в таблице Microsoft Access базы данных подключен модуль ODBC рабочей области для Microsoft SQL Server 6.0 (или более поздней версии), которая имеет столбец ИДЕНТИФИКАТОРОВ, в противном случае может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="bf2a6-144">Открытие более одного **набора записей** в источник данных ODBC могут завершиться с ошибкой из-за занятости с предыдущего вызова **OpenRecordset** подключение.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-144">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call.</span></span> <span data-ttu-id="bf2a6-145">Один способ, является полностью заполнить **набора записей** с помощью метода **MoveLast** сразу же после открытия **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="bf2a6-145">One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="bf2a6-146">Закрытие набора **записей** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет из коллекции **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="bf2a6-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="bf2a6-147">Если *источник* относится к инструкции SQL состоит из строки объединяется с дробное значение и системных параметров укажите десятичных знаков например запятыми (, например strSQL = «PRICE &gt; " &amp; lngPrice и lngPrice = 125,50), возникает ошибка при попытке открыть **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="bf2a6-148">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="bf2a6-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


