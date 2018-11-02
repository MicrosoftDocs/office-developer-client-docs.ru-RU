---
title: Свойство Workspace.DefaultCursorDriver (DAO)
TOCTitle: DefaultCursorDriver Property
ms:assetid: 15a8356d-7ae0-3c8e-fbb7-2d8ad6d9a582
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845499(v=office.15)
ms:contentKeyID: 48543413
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053582
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 03379b3d4ab6be7252aea45a07dfae4b49471136
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922484"
---
# <a name="workspacedefaultcursordriver-property-dao"></a><span data-ttu-id="2839a-102">Свойство Workspace.DefaultCursorDriver (DAO)</span><span class="sxs-lookup"><span data-stu-id="2839a-102">Workspace.DefaultCursorDriver property (DAO)</span></span>


<span data-ttu-id="2839a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2839a-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="syntax"></a><span data-ttu-id="2839a-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2839a-104">Syntax</span></span>

<span data-ttu-id="2839a-105">*выражение* . DefaultCursorDriver</span><span class="sxs-lookup"><span data-stu-id="2839a-105">*expression* .DefaultCursorDriver</span></span>

<span data-ttu-id="2839a-106">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="2839a-106">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2839a-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="2839a-107">Remarks</span></span>

<span data-ttu-id="2839a-108">Параметр или возвращаемое значение может быть установлено одно константы **[CursorDriverEnum](cursordriverenum-enumeration-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="2839a-108">The setting or return value can be set to one of the **[CursorDriverEnum](cursordriverenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="2839a-109">Значение этого свойства влияет только на подключения, установленные после установки свойства.</span><span class="sxs-lookup"><span data-stu-id="2839a-109">This property setting only affects connections established after the property has been set.</span></span> <span data-ttu-id="2839a-110">Изменение свойства **DefaultCursorDriver** не влияет на существующие подключения.</span><span class="sxs-lookup"><span data-stu-id="2839a-110">Changing the **DefaultCursorDriver** property has no effect on existing connections.</span></span>

## <a name="example"></a><span data-ttu-id="2839a-111">Пример</span><span class="sxs-lookup"><span data-stu-id="2839a-111">Example</span></span>

<span data-ttu-id="2839a-112">В этом примере используется метод **NextRecordset** для просмотра данных из составного запроса.</span><span class="sxs-lookup"><span data-stu-id="2839a-112">This example uses the **NextRecordset** method to view the data from a compound SELECT query.</span></span> <span data-ttu-id="2839a-113">Свойство **DefaultCursorDriver** должно иметь значение **dbUseODBCCursor** при выполнении таких запросов.</span><span class="sxs-lookup"><span data-stu-id="2839a-113">The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries.</span></span> <span data-ttu-id="2839a-114">Метод **NextRecordset** возвращает **значение True,** даже в том случае, если некоторые или все инструкции SELECT возвращают записей; только после проверки отдельных предложений SQL, он будет возвращать **значение False** .</span><span class="sxs-lookup"><span data-stu-id="2839a-114">The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

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

Другой способ выполнения этой задачи является создание подготовленной инструкции, содержащий составные инструкции SQL. <span data-ttu-id="2839a-116">Свойство **CacheSize** объекта **QueryDef** должен иметь значение 1, и объект **набора записей** должен иметь только вперед и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2839a-116">The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

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

<br/>

В этом примере с помощью свойства **RecordStatus** и **DefaultCursorDriver** для отображения способ отслеживания изменений в локальном **набора записей** во время обновления пакета. <span data-ttu-id="2839a-118">Функция RecordStatusOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="2839a-118">The RecordStatusOutput function is required for this procedure to run.</span></span>

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```

