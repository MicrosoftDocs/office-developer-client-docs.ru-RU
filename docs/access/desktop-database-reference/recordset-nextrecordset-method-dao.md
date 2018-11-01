---
title: Recordset.NextRecordset Method (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 4a3a6176-0aa0-efb6-b175-dbe23e266abc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193483(v=office.15)
ms:contentKeyID: 48544664
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75dd4059aa9d06e2e6552b0ab7945373add55c76
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872363"
---
# <a name="recordsetnextrecordset-method-dao"></a><span data-ttu-id="9770f-102">Recordset.NextRecordset Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="9770f-102">Recordset.NextRecordset Method (DAO)</span></span>


<span data-ttu-id="9770f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9770f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9770f-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9770f-104">Syntax</span></span>

<span data-ttu-id="9770f-105">*выражение* . NextRecordset</span><span class="sxs-lookup"><span data-stu-id="9770f-105">*expression* .NextRecordset</span></span>

<span data-ttu-id="9770f-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="9770f-106">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="9770f-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9770f-107">Return value</span></span>

<span data-ttu-id="9770f-108">Boolean</span><span class="sxs-lookup"><span data-stu-id="9770f-108">Boolean</span></span>

## <a name="remarks"></a><span data-ttu-id="9770f-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="9770f-109">Remarks</span></span>

<span data-ttu-id="9770f-110">В рабочей области технология ODBCDirect можно открыть **[набор записей](recordset-object-dao.md)** , содержащий несколько выборку в исходный аргумент **OpenRecordset**или свойство **[SQL](querydef-sql-property-dao.md)** select запроса объекта **[QueryDef](querydef-object-dao.md)** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="9770f-110">In an ODBCDirect workspace, you can open a **[Recordset](recordset-object-dao.md)** containing more than one select query in the source argument of **OpenRecordset**, or the **[SQL](querydef-sql-property-dao.md)** property of a select query **[QueryDef](querydef-object-dao.md)** object, as in the following example.</span></span>

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

<span data-ttu-id="9770f-111">Результаты первого запроса открывается возвращаемых **записей** .</span><span class="sxs-lookup"><span data-stu-id="9770f-111">The returned **Recordset** will open with the results of the first query.</span></span> <span data-ttu-id="9770f-112">Для получения результатов наборов записей из последующих запросов, используйте метод **NextRecordset** .</span><span class="sxs-lookup"><span data-stu-id="9770f-112">To obtain the result sets of records from subsequent queries, use the **NextRecordset** method.</span></span>

<span data-ttu-id="9770f-113">Если доступны дополнительные записи (то есть, возникла другой выборку в вызове **OpenRecordset** или в свойстве **SQL** ), записей, возвращенных из следующего запроса будет загружен в **записей**и будет **NextRecordset** Возвращает **значение True**, указывающего на то, что записи доступны.</span><span class="sxs-lookup"><span data-stu-id="9770f-113">If more records are available (that is, there was another select query in the **OpenRecordset** call or in the **SQL** property), the records returned from the next query will be loaded into the **Recordset**, and **NextRecordset** will return **True**, indicating that the records are available.</span></span> <span data-ttu-id="9770f-114">При наличии нескольких записей (то есть, результаты последнего select запроса были загружены в **набор записей**), а затем **NextRecordset** возвращает **значение False**, а **записей** будет пустым.</span><span class="sxs-lookup"><span data-stu-id="9770f-114">When no more records are available (that is, results of the last select query have been loaded into the **Recordset**), then **NextRecordset** will return **False**, and the **Recordset** will be empty.</span></span>

<span data-ttu-id="9770f-115">Можно также использовать метод **[Отменить](connection-cancel-method-dao.md)** очистить содержимое **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="9770f-115">You can also use the **[Cancel](connection-cancel-method-dao.md)** method to flush the contents of a **Recordset**.</span></span> <span data-ttu-id="9770f-116">Тем не менее также **Отменить** очищает любые дополнительные записи еще не загружен.</span><span class="sxs-lookup"><span data-stu-id="9770f-116">However, **Cancel** also flushes any additional records not yet loaded.</span></span>

## <a name="example"></a><span data-ttu-id="9770f-117">Пример</span><span class="sxs-lookup"><span data-stu-id="9770f-117">Example</span></span>

<span data-ttu-id="9770f-118">В этом примере используется метод **NextRecordset** для просмотра данных из составного запроса.</span><span class="sxs-lookup"><span data-stu-id="9770f-118">This example uses the **NextRecordset** method to view the data from a compound SELECT query.</span></span> <span data-ttu-id="9770f-119">Свойство **DefaultCursorDriver** должно иметь значение **dbUseODBCCursor** при выполнении таких запросов.</span><span class="sxs-lookup"><span data-stu-id="9770f-119">The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries.</span></span> <span data-ttu-id="9770f-120">Метод **NextRecordset** возвращает **значение True,** даже в том случае, если некоторые или все инструкции SELECT возвращают записей; только после проверки отдельных предложений SQL, он будет возвращать **значение False** .</span><span class="sxs-lookup"><span data-stu-id="9770f-120">The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset 
     Dim intCount As Integer 
     Dim booNext As Boolean 
     
     ' Create ODBCDirect Workspace object and open Connection 
     ' object. The DefaultCursorDriver setting is required 
     ' when using compound SQL statements. 
     Set wrkODBC = CreateWorkspace("", _ 
     "admin", "", dbUseODBC) 
     wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
     
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Construct compound SELECT statement. 
     Set rstTemp = conPubs.OpenRecordset("SELECT * " & _ 
     "FROM authors; " & _ 
     "SELECT * FROM stores; " & _ 
     "SELECT * FROM jobs") 
     
     ' Try printing results from each of the three SELECT 
     ' statements. 
     booNext = True 
     intCount = 1 
     With rstTemp 
     Do While booNext 
     Debug.Print "Contents of recordset #" & intCount 
     Do While Not .EOF 
     Debug.Print , .Fields(0), .Fields(1) 
     .MoveNext 
     Loop 
     booNext = .NextRecordset 
     Debug.Print " rstTemp.NextRecordset = " & _ 
     booNext 
     intCount = intCount + 1 
     Loop 
     End With 
     
     rstTemp.Close 
     conPubs.Close 
     wrkODBC.Close 
     
    End Sub 
```

<br/>

Другой способ выполнения этой задачи является создание подготовленной инструкции, содержащий составные инструкции SQL. <span data-ttu-id="9770f-122">Свойство **CacheSize** объекта **QueryDef** должен иметь значение 1, и объект **набора записей** должен иметь только вперед и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9770f-122">The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim intCount As Integer 
 Dim booNext As Boolean 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. The DefaultCursorDriver setting is required 
 ' when using compound SQL statements. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Create a temporary stored procedure with a compound 
 ' SELECT statement. 
 Set qdfTemp = conPubs.CreateQueryDef("", _ 
 "SELECT * FROM authors; " & _ 
 "SELECT * FROM stores; " & _ 
 "SELECT * FROM jobs") 
 ' Set CacheSize and open Recordset object with arguments 
 ' that will allow access to multiple recordsets. 
 qdfTemp.CacheSize = 1 
 Set rstTemp = qdfTemp.OpenRecordset(dbOpenForwardOnly, _ 
 dbReadOnly) 
 
 ' Try printing results from each of the three SELECT 
 ' statements. 
 booNext = True 
 intCount = 1 
 With rstTemp 
 Do While booNext 
 Debug.Print "Contents of recordset #" & intCount 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 booNext = .NextRecordset 
 Debug.Print " rstTemp.NextRecordset = " & _ 
 booNext 
 intCount = intCount + 1 
 Loop 
 End With 
 
 rstTemp.Close 
 qdfTemp.Close 
 conPubs.Close 
 wrkODBC.Close 
 
End Sub 
 
```

