---
title: Метод TableDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: f4c9c89c-3348-d3c9-ce76-dd11e5ee11a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836703(v=office.15)
ms:contentKeyID: 48548696
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2035d4319f7821f2a0469193955c732231f30cf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314338"
---
# <a name="tabledefopenrecordset-method-dao"></a><span data-ttu-id="a9598-102">Метод TableDef.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9598-102">TableDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="a9598-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9598-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9598-104">Создает новый объект **[Recordset](recordset-object-dao.md)** и добавляет его в коллекцию **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="a9598-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9598-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9598-105">Syntax</span></span>

<span data-ttu-id="a9598-106">*выражение* .OpenRecordset(***Type***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="a9598-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="a9598-107">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="a9598-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9598-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9598-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9598-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a9598-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a9598-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="a9598-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a9598-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a9598-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a9598-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a9598-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9598-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="a9598-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="a9598-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a9598-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a9598-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="a9598-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a9598-116">Источник записей для нового объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9598-116">The source of the records for the new <strong>Recordset</strong>.</span></span> <span data-ttu-id="a9598-117">Источником может быть имя таблицы, имя запроса или оператор SQL, возвращающий записи.</span><span class="sxs-lookup"><span data-stu-id="a9598-117">The source can be a table name, a query name, or an SQL statement that returns records.</span></span> <span data-ttu-id="a9598-118">Для объектов <strong>Recordset</strong> табличного типа в базах данных ядра СУБД Microsoft Access источником может быть только имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="a9598-118">For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9598-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="a9598-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="a9598-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a9598-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="a9598-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a9598-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a9598-122">Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>, которая указывает на то, какой тип объекта <strong>Recordset</strong> нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="a9598-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="a9598-123"><strong>ПРИМЕЧАНИЕ</strong>: при открытии <STRONG>Recordset</STRONG> в рабочей области Microsoft Access, если вы не указали тип, <STRONG>OpenRecordset</STRONG> создает табличный тип <STRONG>Recordset</STRONG>, если возможно.</span><span class="sxs-lookup"><span data-stu-id="a9598-123"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="a9598-124">Вы укажете связанную таблицу или запрос, <STRONG>OpenRecordset</STRONG> создаст объект <STRONG>Recordset</STRONG> типа dynaset.</span><span class="sxs-lookup"><span data-stu-id="a9598-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9598-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="a9598-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="a9598-126">Необязательно</span><span class="sxs-lookup"><span data-stu-id="a9598-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="a9598-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a9598-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a9598-128">Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>, которые указывают характеристики нового объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9598-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="a9598-129"><strong>ПРИМЕЧАНИЕ</strong>: Константы <STRONG>dbConsistent</STRONG> и <STRONG>dbInconsistent</STRONG> являются взаимоисключающими, и использование обоих констант вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a9598-129"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="a9598-130">Предоставление аргумента lockedits, когда опции используют константы <STRONG>dbReadOnly</STRONG>, также приводит к возникновению ошибки.</span><span class="sxs-lookup"><span data-stu-id="a9598-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9598-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="a9598-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="a9598-132">Необязательно</span><span class="sxs-lookup"><span data-stu-id="a9598-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="a9598-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a9598-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a9598-134">Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>, определяющая блокировку <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9598-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="a9598-135"><strong>NOTE</strong>: вы можете использовать <STRONG>dbReadOnly</STRONG> или в аргументе параметров или в аргументе lockedits, но не одновременно.</span><span class="sxs-lookup"><span data-stu-id="a9598-135"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="a9598-136">Если вы используете его для обоих аргументов, возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a9598-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="a9598-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9598-137">Return value</span></span>

<span data-ttu-id="a9598-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="a9598-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="a9598-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9598-139">Remarks</span></span>

<span data-ttu-id="a9598-140">Обычно если у пользователя возникает эта ошибка во время обновления записи, код должен обновлять содержимое полей и возвращать измененные значения.</span><span class="sxs-lookup"><span data-stu-id="a9598-140">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values.</span></span> <span data-ttu-id="a9598-141">Если ошибка возникает при удалении записи, код может отобразить для пользователя данные новой записи и сообщение о недавнем изменении данных.</span><span class="sxs-lookup"><span data-stu-id="a9598-141">If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed.</span></span> <span data-ttu-id="a9598-142">В этот момент код может запросить у пользователя подтверждение удаления записи.</span><span class="sxs-lookup"><span data-stu-id="a9598-142">At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="a9598-143">Вы также можете использовать константу **dbSeeChanges** при открытии **Recordset** в рабочей области ODBC, подключенной к ядру СУБД Microsoft Access для таблицы Microsoft SQL Server 6.0 (или более поздней версии), содержащей столбец IDENTITY, в противном случае может возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="a9598-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="a9598-144">Открытие нескольких объектов **Recordset** для источника данных ODBC может привести к завершению работы, так как подключение будет занято предыдущим вызовом **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="a9598-144">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call.</span></span> <span data-ttu-id="a9598-145">Один из способов решения этой проблемы состоит в полном заполнении **Recordset** с помощью метода **MoveLast** непосредственно после открытия **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a9598-145">One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="a9598-146">Закрытие **Recordset** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет его из коллекции **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="a9598-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="a9598-147">Если *источник* ссылается на оператор SQL, состоящий из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a9598-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="a9598-148">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="a9598-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


