---
title: Метод QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3948ba2bd8eb63176483a97942984823b9f45b0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997149"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="23f34-102">Метод QueryDef.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="23f34-102">QueryDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="23f34-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23f34-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23f34-104">Создает новый объект **[набора записей](recordset-object-dao.md)** и добавляет его в коллекцию **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="23f34-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f34-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23f34-105">Syntax</span></span>

<span data-ttu-id="23f34-106">*выражение* . OpenRecordset (***Тип***, ***Параметры*** ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="23f34-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="23f34-107">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="23f34-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="23f34-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23f34-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23f34-109">Имя</span><span class="sxs-lookup"><span data-stu-id="23f34-109">Name</span></span></p></th>
<th><p><span data-ttu-id="23f34-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="23f34-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="23f34-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="23f34-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="23f34-112">Описание</span><span class="sxs-lookup"><span data-stu-id="23f34-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23f34-113"><em>Тип</em></span><span class="sxs-lookup"><span data-stu-id="23f34-113"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="23f34-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="23f34-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="23f34-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="23f34-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="23f34-116">Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> , указывающая тип <strong>набора записей</strong> , чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="23f34-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="23f34-117"><strong>Примечание</strong>: при открытии <STRONG>набора записей</STRONG> в рабочей области Microsoft Access и тип не указан, <STRONG>OpenRecordset</STRONG> создает табличного типа <STRONG>записей</STRONG>, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="23f34-117"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="23f34-118">При указании связанной таблицы или запроса, <STRONG>OpenRecordset</STRONG> создает добавляющий <STRONG>набора записей</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="23f34-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23f34-119"><em>Варианты</em></span><span class="sxs-lookup"><span data-stu-id="23f34-119"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="23f34-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="23f34-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="23f34-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="23f34-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="23f34-122">Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> , которые задают характеристики нового <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="23f34-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="23f34-123"><strong>Примечание</strong>: константы <STRONG>dbConsistent</STRONG> и <STRONG>dbInconsistent</STRONG> являются взаимоисключающими и использовании обоих приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="23f34-123"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="23f34-124">Также указав аргумент lockedits при параметры использует константу <STRONG>dbReadOnly</STRONG> приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="23f34-124">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23f34-125"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="23f34-125"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="23f34-126">Необязательный</span><span class="sxs-lookup"><span data-stu-id="23f34-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="23f34-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="23f34-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="23f34-128">Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> , определяющая блокировки для <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="23f34-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="23f34-129"><strong>Примечание</strong>: можно использовать <STRONG>dbReadOnly</STRONG> в аргументе параметры или аргумент lockedits, но не оба.</span><span class="sxs-lookup"><span data-stu-id="23f34-129"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="23f34-130">При использовании обоих аргументов, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="23f34-130">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="23f34-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23f34-131">Return value</span></span>

<span data-ttu-id="23f34-132">Набор записей</span><span class="sxs-lookup"><span data-stu-id="23f34-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="23f34-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="23f34-133">Remarks</span></span>

<span data-ttu-id="23f34-134">Константа **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** также следует использовать при открытии **набора записей** в таблице Microsoft Access базы данных подключен модуль ODBC рабочей области для Microsoft SQL Server 6.0 (или более поздней версии), которая имеет столбец ИДЕНТИФИКАТОРОВ, в противном случае может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="23f34-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="23f34-135">Открытие более одного **набора записей** в источник данных ODBC могут завершиться с ошибкой из-за занятости с предыдущего вызова **OpenRecordset** подключение.</span><span class="sxs-lookup"><span data-stu-id="23f34-135">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call.</span></span> <span data-ttu-id="23f34-136">Один способ, является полностью заполнить **набора записей** с помощью метода **[MoveLast](recordset-movelast-method-dao.md)** сразу же после открытия **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="23f34-136">One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="23f34-137">Закрытие набора **записей** с помощью метода **Close** автоматически удаляет из коллекции **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="23f34-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="23f34-138">Если *источник* относится к инструкции SQL состоит из строки объединяется с дробное значение и системных параметров укажите десятичных знаков например запятыми (, например strSQL = «PRICE &gt; " &amp; lngPrice и lngPrice = 125,50), возникает ошибка при попытке открыть **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="23f34-138">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="23f34-139">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="23f34-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


