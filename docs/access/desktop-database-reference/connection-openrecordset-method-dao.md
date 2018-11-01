---
title: Connection.OpenRecordset Method (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fec0e2717c39ea2aeb4a41d7630998c79ce9c52
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872720"
---
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="70a84-102">Connection.OpenRecordset Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="70a84-102">Connection.OpenRecordset Method (DAO)</span></span>


<span data-ttu-id="70a84-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70a84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70a84-104">Создает новый объект **[набора записей](recordset-object-dao.md)** и добавляет его в коллекцию **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="70a84-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a84-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70a84-105">Syntax</span></span>

<span data-ttu-id="70a84-106">*выражение* . OpenRecordset (***имя***, ***Тип***, ***Параметры***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="70a84-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="70a84-107">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="70a84-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="70a84-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="70a84-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70a84-109">Имя</span><span class="sxs-lookup"><span data-stu-id="70a84-109">Name</span></span></p></th>
<th><p><span data-ttu-id="70a84-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="70a84-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="70a84-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="70a84-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="70a84-112">Описание</span><span class="sxs-lookup"><span data-stu-id="70a84-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70a84-113">Имя</span><span class="sxs-lookup"><span data-stu-id="70a84-113">Name</span></span></p></td>
<td><p><span data-ttu-id="70a84-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="70a84-114">Required</span></span></p></td>
<td><p><span data-ttu-id="70a84-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="70a84-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="70a84-116">Источник записей для нового <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="70a84-116">The source of the records for the new <strong>Recordset</strong>.</span></span> <span data-ttu-id="70a84-117">Источник может быть имя таблицы, имя запроса или инструкции SQL, которая возвращает записи.</span><span class="sxs-lookup"><span data-stu-id="70a84-117">The source can be a table name, a query name, or an SQL statement that returns records.</span></span> <span data-ttu-id="70a84-118">Для объектов <strong>наборов записей</strong> в таблице типа в базами данных, ядро базы данных Microsoft Access источник может быть только имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="70a84-118">For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70a84-119">Тип</span><span class="sxs-lookup"><span data-stu-id="70a84-119">Type</span></span></p></td>
<td><p><span data-ttu-id="70a84-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="70a84-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="70a84-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="70a84-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="70a84-122">Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> , указывающая тип <strong>набора записей</strong> , чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="70a84-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <span data-ttu-id="70a84-123">При открытии **набора записей** в рабочей области Microsoft Access и тип не указан, **OpenRecordset** создает табличного типа **записей**, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="70a84-123">If you open a **Recordset** in a Microsoft Access workspace and you don't specify a type, **OpenRecordset** creates a table-type **Recordset**, if possible.</span></span> <span data-ttu-id="70a84-124">При указании связанной таблицы или запроса, **OpenRecordset** создает добавляющий **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="70a84-124">If you specify a linked table or query, **OpenRecordset** creates a dynaset-type **Recordset**.</span></span>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70a84-125">Options</span><span class="sxs-lookup"><span data-stu-id="70a84-125">Options</span></span></p></td>
<td><p><span data-ttu-id="70a84-126">Необязательный</span><span class="sxs-lookup"><span data-stu-id="70a84-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="70a84-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="70a84-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="70a84-128">Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> , которые задают характеристики нового <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="70a84-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="70a84-129">Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими и использовании обоих приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="70a84-129">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="70a84-130">Также указав аргумент lockedits параметров с помощью константу **dbReadOnly** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="70a84-130">Supplying a lockedits argument when options use the **dbReadOnly** constant also causes an error.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70a84-131">LockEdit</span><span class="sxs-lookup"><span data-stu-id="70a84-131">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="70a84-132">Необязательный</span><span class="sxs-lookup"><span data-stu-id="70a84-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="70a84-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="70a84-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="70a84-134">Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> , определяющая блокировки для <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="70a84-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="70a84-135">Можно использовать **dbReadOnly** в аргументе параметры или аргумент lockedits, но не оба.</span><span class="sxs-lookup"><span data-stu-id="70a84-135">You can use **dbReadOnly** in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="70a84-136">При использовании обоих аргументов, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="70a84-136">If you use it for both arguments, a run-time error occurs.</span></span>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="70a84-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70a84-137">Return value</span></span>

<span data-ttu-id="70a84-138">Набор записей</span><span class="sxs-lookup"><span data-stu-id="70a84-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="70a84-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="70a84-139">Remarks</span></span>

<span data-ttu-id="70a84-140">Как правило если пользователь получает Эта ошибка при обновлении записи, код должен обновить содержимое полей и извлечение измененные значения.</span><span class="sxs-lookup"><span data-stu-id="70a84-140">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values.</span></span> <span data-ttu-id="70a84-141">Если ошибка возникает при удалении записи, кода удалось отобразить новые записи данных для пользователя и сообщение, указывающее, что недавно были изменены данные.</span><span class="sxs-lookup"><span data-stu-id="70a84-141">If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed.</span></span> <span data-ttu-id="70a84-142">На этом этапе кода можно запросить подтверждения, что по-прежнему требуется удалить эту запись.</span><span class="sxs-lookup"><span data-stu-id="70a84-142">At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="70a84-143">Константа **dbSeeChanges** также следует использовать при открытии **набора записей** в таблице Microsoft Access базы данных подключен модуль ODBC рабочей области для Microsoft SQL Server 6.0 (или более поздней версии), которая имеет столбец ИДЕНТИФИКАТОРОВ, в противном случае может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="70a84-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="70a84-144">Открытие более одного **набора записей** в источник данных ODBC могут завершиться с ошибкой из-за занятости с предыдущего вызова **OpenRecordset** подключение.</span><span class="sxs-lookup"><span data-stu-id="70a84-144">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call.</span></span> <span data-ttu-id="70a84-145">Один способ, является полностью заполнить **набора записей** с помощью метода **MoveLast** сразу же после открытия **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="70a84-145">One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="70a84-146">Закрытие набора **записей** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет из коллекции **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="70a84-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="70a84-147">Если *источник* относится к инструкции SQL состоит из строки объединяется с дробное значение и системных параметров укажите десятичных знаков например запятыми (, например strSQL = «PRICE &gt; " &amp; lngPrice и lngPrice = 125,50), возникает ошибка при попытке открыть **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="70a84-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="70a84-148">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="70a84-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


