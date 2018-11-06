---
title: Метод Database.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 00b39fc81e929ad32a19ef81d3dc9fa5633308f7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997270"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="70071-102">Метод Database.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="70071-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="70071-103">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="70071-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="70071-104">Создает новый объект **[набора записей](recordset-object-dao.md)** и добавляет его в коллекцию **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="70071-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="70071-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70071-105">Syntax</span></span>

<span data-ttu-id="70071-106">*выражение* . OpenRecordset (_**имя**_, _**Тип**_, _**Параметры**_, _**LockEdit**_)</span><span class="sxs-lookup"><span data-stu-id="70071-106">*expression* .OpenRecordset(_**Name**_, _**Type**_, _**Options**_, _**LockEdit**_)</span></span>

<span data-ttu-id="70071-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="70071-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="70071-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="70071-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70071-109">Имя</span><span class="sxs-lookup"><span data-stu-id="70071-109">Name</span></span></p></th>
<th><p><span data-ttu-id="70071-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="70071-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="70071-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="70071-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="70071-112">Описание</span><span class="sxs-lookup"><span data-stu-id="70071-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70071-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="70071-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="70071-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="70071-114">Required</span></span></p></td>
<td><p><span data-ttu-id="70071-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="70071-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="70071-116">Источник записей для нового <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="70071-116">The source of the records for the new <strong>Recordset</strong>.</span></span> <span data-ttu-id="70071-117">Источник может быть имя таблицы, имя запроса или инструкции SQL, которая возвращает записи.</span><span class="sxs-lookup"><span data-stu-id="70071-117">The source can be a table name, a query name, or an SQL statement that returns records.</span></span> <span data-ttu-id="70071-118">Для объектов <strong>наборов записей</strong> в таблице типа в базами данных, ядро базы данных Microsoft Access источник может быть только имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="70071-118">For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70071-119"><em>Тип</em></span><span class="sxs-lookup"><span data-stu-id="70071-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="70071-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="70071-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="70071-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="70071-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="70071-122">Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> , указывающая тип <strong>набора записей</strong> , чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="70071-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="70071-123"><strong>Примечание</strong>: при открытии <strong>набора записей</strong> в рабочей области Microsoft Access и тип не указан, <strong>OpenRecordset</strong> создает табличного типа <strong>записей</strong>, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="70071-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="70071-124">При указании связанной таблицы или запроса, <strong>OpenRecordset</strong> создает добавляющий <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="70071-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70071-125"><em>Варианты</em></span><span class="sxs-lookup"><span data-stu-id="70071-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="70071-126">Необязательный</span><span class="sxs-lookup"><span data-stu-id="70071-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="70071-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="70071-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="70071-128">Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> , которые задают характеристики нового <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="70071-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="70071-129"><strong>Примечание</strong>: константы <strong>dbConsistent</strong> и <strong>dbInconsistent</strong> являются взаимоисключающими и использовании обоих приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="70071-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="70071-130">Также указав аргумент LockEdit, когда параметры использует константу <strong>dbReadOnly</strong> приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="70071-130">Supplying a LockEdit argument when Options uses the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70071-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="70071-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="70071-132">Необязательный</span><span class="sxs-lookup"><span data-stu-id="70071-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="70071-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="70071-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="70071-134">Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> , определяющая блокировки для <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="70071-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="70071-135"><strong>Примечание</strong>: можно использовать <strong>dbReadOnly</strong> в аргументе параметры или аргумент LockedEdit, но не оба.</span><span class="sxs-lookup"><span data-stu-id="70071-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="70071-136">При использовании обоих аргументов, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="70071-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="70071-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70071-137">Return value</span></span>

<span data-ttu-id="70071-138">Набор записей</span><span class="sxs-lookup"><span data-stu-id="70071-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="70071-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="70071-139">Remarks</span></span>

<span data-ttu-id="70071-140">Как правило если пользователь получает Эта ошибка при обновлении записи, код должен обновить содержимое полей и извлечение измененные значения.</span><span class="sxs-lookup"><span data-stu-id="70071-140">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values.</span></span> <span data-ttu-id="70071-141">Если ошибка возникает при удалении записи, кода удалось отобразить новые записи данных для пользователя и сообщение, указывающее, что недавно были изменены данные.</span><span class="sxs-lookup"><span data-stu-id="70071-141">If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed.</span></span> <span data-ttu-id="70071-142">На этом этапе кода можно запросить подтверждения, что по-прежнему требуется удалить эту запись.</span><span class="sxs-lookup"><span data-stu-id="70071-142">At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="70071-143">Константа **dbSeeChanges** также следует использовать при открытии **набора записей** в таблице Microsoft Access базы данных подключен модуль ODBC рабочей области для Microsoft SQL Server 6.0 (или более поздней версии), которая имеет столбец ИДЕНТИФИКАТОРОВ, в противном случае может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="70071-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="70071-144">Открытие более одного **набора записей** в источник данных ODBC могут завершиться с ошибкой из-за занятости с предыдущего вызова **OpenRecordset** подключение.</span><span class="sxs-lookup"><span data-stu-id="70071-144">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call.</span></span> <span data-ttu-id="70071-145">Один способ, является полностью заполнить **набора записей** с помощью метода **MoveLast** сразу же после открытия **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="70071-145">One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="70071-146">Закрытие набора **записей** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет из коллекции **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="70071-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="70071-147">Если *источник* относится к инструкции SQL состоит из строки объединяется с дробное значение и системных параметров укажите десятичных знаков например запятыми (, например strSQL = «PRICE &gt; " &amp; lngPrice и lngPrice = 125,50), возникает ошибка при попытке открыть **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="70071-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="70071-148">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="70071-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="70071-149">**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="70071-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="70071-150">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="70071-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="70071-151">Передача данных из Access в Excel</span><span class="sxs-lookup"><span data-stu-id="70071-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="70071-152">Пример</span><span class="sxs-lookup"><span data-stu-id="70071-152">Example</span></span>

<span data-ttu-id="70071-153">Следующем примере показано, как открыть записей, основанный на параметр запроса.</span><span class="sxs-lookup"><span data-stu-id="70071-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="70071-154">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="70071-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="70071-155">Следующем примере показано, как открыть набор записей на основе таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="70071-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="70071-156">Следующем примере показано, как открыть записей, на основе инструкции структурированный язык запросов (SQL).</span><span class="sxs-lookup"><span data-stu-id="70071-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="70071-157">В следующем примере показано, как использовать свойство фильтр для определения записей, включаемых в последующем открыт записей.</span><span class="sxs-lookup"><span data-stu-id="70071-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
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



