---
title: Метод QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302851"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="a62e2-102">Метод QueryDef.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="a62e2-102">QueryDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="a62e2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a62e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a62e2-104">Создает новый объект **[Recordset](recordset-object-dao.md)** и добавляет его в коллекцию **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="a62e2-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a62e2-105">Syntax</span></span>

<span data-ttu-id="a62e2-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="a62e2-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="a62e2-107">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="a62e2-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a62e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a62e2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a62e2-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a62e2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a62e2-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="a62e2-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a62e2-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a62e2-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a62e2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a62e2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a62e2-113"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="a62e2-113"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="a62e2-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a62e2-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="a62e2-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a62e2-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a62e2-116">Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>, которая указывает на то, какой тип объекта <strong>Recordset</strong> нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="a62e2-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="a62e2-117"><strong>ПРИМЕЧАНИЕ</strong>: при открытии <STRONG>Recordset</STRONG> в рабочей области Microsoft Access, если вы не указали тип, <STRONG>OpenRecordset</STRONG> создает табличный тип <STRONG>Recordset</STRONG>, если возможно.</span><span class="sxs-lookup"><span data-stu-id="a62e2-117"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="a62e2-118">Вы укажете связанную таблицу или запрос, <STRONG>OpenRecordset</STRONG> создаст объект <STRONG>Recordset</STRONG> типа dynaset.</span><span class="sxs-lookup"><span data-stu-id="a62e2-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a62e2-119"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="a62e2-119"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="a62e2-120">Необязательно</span><span class="sxs-lookup"><span data-stu-id="a62e2-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="a62e2-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a62e2-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a62e2-122">Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>, которые указывают характеристики нового объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a62e2-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="a62e2-123"><strong>ПРИМЕЧАНИЕ</strong>: Константы <STRONG>dbConsistent</STRONG> и <STRONG>dbInconsistent</STRONG> являются взаимоисключающими, и использование обоих констант вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a62e2-123"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="a62e2-124">Предоставление аргумента lockedits, когда опции используют константы <STRONG>dbReadOnly</STRONG>, также приводит к возникновению ошибки.</span><span class="sxs-lookup"><span data-stu-id="a62e2-124">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a62e2-125"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="a62e2-125"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="a62e2-126">Необязательно</span><span class="sxs-lookup"><span data-stu-id="a62e2-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="a62e2-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a62e2-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a62e2-128">Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>, определяющая блокировку <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a62e2-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="a62e2-129"><strong>NOTE</strong>: вы можете использовать <STRONG>dbReadOnly</STRONG> или в аргументе параметров или в аргументе lockedits, но не одновременно.</span><span class="sxs-lookup"><span data-stu-id="a62e2-129"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="a62e2-130">Если вы используете его для обоих аргументов, возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a62e2-130">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="a62e2-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a62e2-131">Return value</span></span>

<span data-ttu-id="a62e2-132">Recordset</span><span class="sxs-lookup"><span data-stu-id="a62e2-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="a62e2-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a62e2-133">Remarks</span></span>

<span data-ttu-id="a62e2-134">Вы также можете использовать константу **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** при открытии **Recordset** в рабочей области ODBC, подключенной к ядру СУБД Microsoft Access для таблицы Microsoft SQL Server 6.0 (или более поздней версии), содержащей столбец IDENTITY, в противном случае может возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="a62e2-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="a62e2-135">Открытие нескольких объектов **Recordset** для источника данных ODBC может привести к завершении работы, так как подключение будет занято предыдущим вызовом **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="a62e2-135">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call.</span></span> <span data-ttu-id="a62e2-136">Одним из способов решения этой проблемы состоит в полном заполнении **Recordset** с помощью метода **[MoveLast](recordset-movelast-method-dao.md)** непосредственно после открытия **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a62e2-136">One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="a62e2-137">Закрытие **Recordset** с помощью метода **Close** автоматически удаляет его из коллекции **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="a62e2-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="a62e2-138">Если *источник* ссылается на оператора SQL, состоящий из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a62e2-138">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="a62e2-139">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="a62e2-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


