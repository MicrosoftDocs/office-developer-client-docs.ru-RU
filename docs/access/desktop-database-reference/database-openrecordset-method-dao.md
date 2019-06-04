---
title: Метод Database.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 06/04/2019
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b13abd7f3f2c856a0f1a1288717d6f8affb81252
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675745"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="ad848-102">Метод Database.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="ad848-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="ad848-103">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad848-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="ad848-104">Создает новый объект **[Recordset](recordset-object-dao.md)** и добавляет его в коллекцию **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ad848-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad848-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad848-105">Syntax</span></span>

<span data-ttu-id="ad848-106">*выражение*.**OpenRecordset** (_Name_, _Type_, _Options_, _LockEdit_)</span><span class="sxs-lookup"><span data-stu-id="ad848-106">*expression*.**OpenRecordset** (_Name_, _Type_, _Options_, _LockEdit_)</span></span>

<span data-ttu-id="ad848-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="ad848-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad848-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad848-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad848-109">Имя</span><span class="sxs-lookup"><span data-stu-id="ad848-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ad848-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="ad848-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ad848-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ad848-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ad848-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ad848-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad848-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ad848-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ad848-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ad848-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ad848-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ad848-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ad848-116">Источник записей для нового объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad848-116">The source of the records for the new <strong>Recordset</strong>.</span></span> <span data-ttu-id="ad848-117">Источником может быть имя таблицы, имя запроса или оператор SQL, возвращающий записи.</span><span class="sxs-lookup"><span data-stu-id="ad848-117">The source can be a table name, a query name, or an SQL statement that returns records.</span></span> <span data-ttu-id="ad848-118">Для объектов <strong>Recordset</strong> табличного типа в базах данных ядра СУБД Microsoft Access источником может быть только имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="ad848-118">For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad848-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="ad848-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="ad848-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ad848-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="ad848-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ad848-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ad848-122">Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>, которая указывает на то, какой тип объекта <strong>Recordset</strong> нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="ad848-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="ad848-123"><strong>ПРИМЕЧАНИЕ</strong>: при открытии <strong>Recordset</strong> в рабочей области Microsoft Access, если вы не указали тип, <strong>OpenRecordset</strong> создает табличный тип <strong>Recordset</strong>, если возможно.</span><span class="sxs-lookup"><span data-stu-id="ad848-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="ad848-124">Вы укажете связанную таблицу или запрос, <strong>OpenRecordset</strong> создаст объект <strong>Recordset</strong> типа dynaset.</span><span class="sxs-lookup"><span data-stu-id="ad848-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad848-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="ad848-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="ad848-126">Необязательно</span><span class="sxs-lookup"><span data-stu-id="ad848-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="ad848-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ad848-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ad848-128">Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>, которые указывают характеристики нового объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad848-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="ad848-129"><strong>ПРИМЕЧАНИЕ</strong>. Константы <strong>dbConsistent</strong> и <strong>dbInconsistent</strong> являются взаимоисключающими, и использование обеих констант вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ad848-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="ad848-130">Предоставление аргумента LockEdit, когда в качестве аргумента Options используется константа <strong>dbReadOnly</strong>, также приводит к возникновению ошибки.</span><span class="sxs-lookup"><span data-stu-id="ad848-130">Supplying a LockEdit argument when Options uses the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad848-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="ad848-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="ad848-132">Необязательно</span><span class="sxs-lookup"><span data-stu-id="ad848-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="ad848-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ad848-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ad848-134">Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>, определяющая блокировку <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad848-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="ad848-135"><strong>ПРИМЕЧАНИЕ</strong>. Вы можете использовать <strong>dbReadOnly</strong> в аргументе Options или в аргументе LockedEdit, но не одновременно.</span><span class="sxs-lookup"><span data-stu-id="ad848-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="ad848-136">Если вы используете его для обоих аргументов, возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ad848-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ad848-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad848-137">Return value</span></span>

<span data-ttu-id="ad848-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="ad848-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="ad848-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad848-139">Remarks</span></span>

<span data-ttu-id="ad848-140">Обычно если у пользователя возникает эта ошибка во время обновления записи, код должен обновлять содержимое полей и возвращать измененные значения.</span><span class="sxs-lookup"><span data-stu-id="ad848-140">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values.</span></span> <span data-ttu-id="ad848-141">Если ошибка возникает при удалении записи, код может отобразить для пользователя данные новой записи и сообщение о недавнем изменении данных.</span><span class="sxs-lookup"><span data-stu-id="ad848-141">If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed.</span></span> <span data-ttu-id="ad848-142">В этот момент код может запросить у пользователя подтверждение удаления записи.</span><span class="sxs-lookup"><span data-stu-id="ad848-142">At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="ad848-143">Вы также можете использовать константу **dbSeeChanges** при открытии **Recordset** в рабочей области ODBC, подключенной к ядру СУБД Microsoft Access для таблицы Microsoft SQL Server 6.0 (или более поздней версии), содержащей столбец IDENTITY, в противном случае может возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="ad848-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="ad848-144">Открытие нескольких объектов **Recordset** для источника данных ODBC может привести к завершению работы, так как подключение будет занято предыдущим вызовом **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="ad848-144">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call.</span></span> <span data-ttu-id="ad848-145">Один из способов решения этой проблемы состоит в полном заполнении **Recordset** с помощью метода **MoveLast** непосредственно после открытия **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ad848-145">One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="ad848-146">Закрытие **Recordset** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет его из коллекции **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ad848-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="ad848-147">Если *источник* ссылается на оператор SQL, состоящий из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ad848-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="ad848-148">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="ad848-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="ad848-149">**Ссылка, предоставляемая** сообществом [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="ad848-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="ad848-150">UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ad848-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="ad848-151">Перенос данных из Access в Excel</span><span class="sxs-lookup"><span data-stu-id="ad848-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="ad848-152">Пример</span><span class="sxs-lookup"><span data-stu-id="ad848-152">Example</span></span>

<span data-ttu-id="ad848-153">В приведенном ниже примере показано, как открыть объект Recordset на основании запроса параметра.</span><span class="sxs-lookup"><span data-stu-id="ad848-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="ad848-154">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="ad848-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="ad848-155">В приведенном ниже примере показано, как открыть объект Recordset на основании таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="ad848-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="ad848-156">В приведенном ниже примере показано, как открыть объект Recordset на основании оператора SQL.</span><span class="sxs-lookup"><span data-stu-id="ad848-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="ad848-157">В примере ниже показано, как использовать свойство Filter для определения записей, которые нужно включить в открываемый впоследствии объект Recordset.</span><span class="sxs-lookup"><span data-stu-id="ad848-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



