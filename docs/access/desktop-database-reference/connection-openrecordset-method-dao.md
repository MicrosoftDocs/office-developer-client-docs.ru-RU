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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295851"
---
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="1a5aa-102">Метод Connection.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="1a5aa-102">Connection.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="1a5aa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a5aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a5aa-104">Создает новый объект **[Recordset](recordset-object-dao.md)** и добавляет его в коллекцию **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a5aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a5aa-105">Syntax</span></span>

<span data-ttu-id="1a5aa-106">*выражение .* OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="1a5aa-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="1a5aa-107">*выражение*: переменная, представляющая объект **Connection**.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a5aa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a5aa-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a5aa-109">Имя</span><span class="sxs-lookup"><span data-stu-id="1a5aa-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1a5aa-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="1a5aa-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1a5aa-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1a5aa-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1a5aa-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1a5aa-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a5aa-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="1a5aa-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="1a5aa-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1a5aa-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1a5aa-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1a5aa-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1a5aa-116">Источник записей для нового объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-116">The source of the records for the new <strong>Recordset</strong>.</span></span> <span data-ttu-id="1a5aa-117">Источником может быть имя таблицы, имя запроса или оператор SQL, возвращающий записи.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-117">The source can be a table name, a query name, or an SQL statement that returns records.</span></span> <span data-ttu-id="1a5aa-118">Для объектов <strong>Recordset</strong> табличного типа в базах данных ядра СУБД Microsoft Access источником может быть только имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-118">For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5aa-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="1a5aa-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="1a5aa-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="1a5aa-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="1a5aa-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1a5aa-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1a5aa-122">Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>, которая указывает на то, какой тип объекта <strong>Recordset</strong> нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="1a5aa-123"><strong>ПРИМЕЧАНИЕ</strong>: при открытии <strong>Recordset</strong> в рабочей области Microsoft Access, если вы не указали тип, <strong>OpenRecordset</strong> создает табличный тип <strong>Recordset</strong>, если возможно.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="1a5aa-124">Вы укажете связанную таблицу или запрос, <strong>OpenRecordset</strong> создаст объект <strong>Recordset</strong> типа dynaset.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a5aa-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="1a5aa-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="1a5aa-126">Необязательно</span><span class="sxs-lookup"><span data-stu-id="1a5aa-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="1a5aa-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1a5aa-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1a5aa-128">Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>, которые указывают характеристики нового объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="1a5aa-129"><strong>ПРИМЕЧАНИЕ</strong>. Константы <strong>dbConsistent</strong> и <strong>dbInconsistent</strong> являются взаимоисключающими, и использование обеих констант вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="1a5aa-130">Если предоставить аргумент lockedits при использовании константы <strong>dbReadOnly,</strong> также будет выступать ошибка.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-130">Supplying a lockedits argument when options use the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5aa-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="1a5aa-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="1a5aa-132">Необязательно</span><span class="sxs-lookup"><span data-stu-id="1a5aa-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="1a5aa-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1a5aa-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1a5aa-134">Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>, определяющая блокировку <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="1a5aa-135"><strong>NOTE</strong>: вы можете использовать <strong>dbReadOnly</strong> или в аргументе параметров или в аргументе lockedits, но не одновременно.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="1a5aa-136">Если вы используете его для обоих аргументов, возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="1a5aa-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a5aa-137">Return value</span></span>

<span data-ttu-id="1a5aa-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="1a5aa-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="1a5aa-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a5aa-139">Remarks</span></span>

<span data-ttu-id="1a5aa-140">Обычно если у пользователя возникает эта ошибка во время обновления записи, код должен обновлять содержимое полей и возвращать измененные значения.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-140">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values.</span></span> <span data-ttu-id="1a5aa-141">Если ошибка возникает при удалении записи, код может отобразить для пользователя данные новой записи и сообщение о недавнем изменении данных.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-141">If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed.</span></span> <span data-ttu-id="1a5aa-142">В этот момент код может запросить у пользователя подтверждение удаления записи.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-142">At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="1a5aa-143">Вы также можете использовать константу **dbSeeChanges** при открытии **Recordset** в рабочей области ODBC, подключенной к ядру СУБД Microsoft Access для таблицы Microsoft SQL Server 6.0 (или более поздней версии), содержащей столбец IDENTITY, в противном случае может возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="1a5aa-144">Открытие нескольких объектов **Recordset** для источника данных ODBC может привести к завершению работы, так как подключение будет занято предыдущим вызовом **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-144">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call.</span></span> <span data-ttu-id="1a5aa-145">Один из способов решения этой проблемы состоит в полном заполнении **Recordset** с помощью метода **MoveLast** непосредственно после открытия **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-145">One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="1a5aa-146">Закрытие **Recordset** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет его из коллекции **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="1a5aa-147">Если *источник* ссылается на оператор SQL, состоящий из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="1a5aa-148">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


