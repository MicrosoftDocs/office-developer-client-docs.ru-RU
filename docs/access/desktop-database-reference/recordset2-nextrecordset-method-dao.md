---
title: Метод Recordset2. NextRecordset (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 33288131-d4f3-0159-1736-f401346087f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192318(v=office.15)
ms:contentKeyID: 48544096
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053575
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 54d0e49dfbe9dc3fb87eb10af9eefe3aa2f83709
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307240"
---
# <a name="recordset2nextrecordset-method-dao"></a><span data-ttu-id="47f20-102">Метод Recordset2. NextRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="47f20-102">Recordset2.NextRecordset method (DAO)</span></span>


<span data-ttu-id="47f20-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47f20-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="47f20-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47f20-104">Syntax</span></span>

<span data-ttu-id="47f20-105">*Expression* . NextRecordset</span><span class="sxs-lookup"><span data-stu-id="47f20-105">*expression* .NextRecordset</span></span>

<span data-ttu-id="47f20-106">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="47f20-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="47f20-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47f20-107">Return value</span></span>

<span data-ttu-id="47f20-108">Boolean</span><span class="sxs-lookup"><span data-stu-id="47f20-108">Boolean</span></span>

## <a name="remarks"></a><span data-ttu-id="47f20-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="47f20-109">Remarks</span></span>

<span data-ttu-id="47f20-110">В рабочей области ODBCDirect можно открыть объект **Recordset** , содержащий несколько запросов на выборку в аргументе Source объекта **OpenRecordset**, или свойство **[SQL](querydef-sql-property-dao.md)** объекта "Select Query **[QueryDef](querydef-object-dao.md)** ", как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="47f20-110">In an ODBCDirect workspace, you can open a **Recordset** containing more than one select query in the source argument of **OpenRecordset**, or the **[SQL](querydef-sql-property-dao.md)** property of a select query **[QueryDef](querydef-object-dao.md)** object, as in the following example.</span></span>

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

<span data-ttu-id="47f20-111">Возвращенный **набор записей** будет открыт с результатами первого запроса.</span><span class="sxs-lookup"><span data-stu-id="47f20-111">The returned **Recordset** will open with the results of the first query.</span></span> <span data-ttu-id="47f20-112">Чтобы получить результирующие наборы записей из последующих запросов, используйте метод **NextRecordset** .</span><span class="sxs-lookup"><span data-stu-id="47f20-112">To obtain the result sets of records from subsequent queries, use the **NextRecordset** method.</span></span>

<span data-ttu-id="47f20-113">Если доступны дополнительные записи (то есть еще один запрос SELECT в вызове **OpenRecordset** или в свойстве **SQL** ), то записи, возвращенные из следующего запроса, будут загружены в **набор записей**, и **NextRecordset** будет Возвращает **значение true**, указывающее, что доступны записи.</span><span class="sxs-lookup"><span data-stu-id="47f20-113">If more records are available (that is, there was another select query in the **OpenRecordset** call or in the **SQL** property), the records returned from the next query will be loaded into the **Recordset**, and **NextRecordset** will return **True**, indicating that the records are available.</span></span> <span data-ttu-id="47f20-114">Если нет доступных записей (то есть результаты последнего запроса SELECT были загружены в **набор записей**), то **NextRecordset** будет возвращать **значение false**, а **набор записей** будет пустым.</span><span class="sxs-lookup"><span data-stu-id="47f20-114">When no more records are available (that is, results of the last select query have been loaded into the **Recordset**), then **NextRecordset** will return **False**, and the **Recordset** will be empty.</span></span>

<span data-ttu-id="47f20-115">Кроме того, можно использовать метод **[Cancel](connection-cancel-method-dao.md)** для очистки содержимого объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="47f20-115">You can also use the **[Cancel](connection-cancel-method-dao.md)** method to flush the contents of a **Recordset**.</span></span> <span data-ttu-id="47f20-116">Тем не менее, **Отмена** также очищает все дополнительные записи, еще не загруженные.</span><span class="sxs-lookup"><span data-stu-id="47f20-116">However, **Cancel** also flushes any additional records not yet loaded.</span></span>

## <a name="example"></a><span data-ttu-id="47f20-117">Пример</span><span class="sxs-lookup"><span data-stu-id="47f20-117">Example</span></span>

<span data-ttu-id="47f20-118">В этом примере используется метод **NextRecordset** для просмотра данных из составного запроса на выборку.</span><span class="sxs-lookup"><span data-stu-id="47f20-118">This example uses the **NextRecordset** method to view the data from a compound SELECT query.</span></span> <span data-ttu-id="47f20-119">При выполнении таких запросов свойству **дефаулткурсордривер** должно быть присвоено значение **дбусеодбккурсор** .</span><span class="sxs-lookup"><span data-stu-id="47f20-119">The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries.</span></span> <span data-ttu-id="47f20-120">Метод **NextRecordset** будет возвращать **значение true** , даже если некоторые или все инструкции SELECT возвращают нулевые записи; он возвратит **значение false** только после того, как все отдельные предложения SQL будут проверены.</span><span class="sxs-lookup"><span data-stu-id="47f20-120">The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset2 
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

Другой способ выполнить ту же задачу — создать подготовленный оператор, содержащий составной оператор SQL. <span data-ttu-id="47f20-122">Свойству **CacheSize** объекта **QueryDef** должно быть присвоено значение 1, а объект **Recordset** должен быть доступен только для чтения и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="47f20-122">The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset2 
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

