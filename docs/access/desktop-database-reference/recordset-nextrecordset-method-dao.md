---
title: Recordset.NextRecordset Method (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 4a3a6176-0aa0-efb6-b175-dbe23e266abc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193483(v=office.15)
ms:contentKeyID: 48544664
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df017e68fd2778acacdefeea09e0787f497ab225
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480368"
---
# <a name="recordsetnextrecordset-method-dao"></a>Recordset.NextRecordset Method (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . NextRecordset

*выражение* Переменная, которая представляет собой объект **набора записей** .

### <a name="return-value"></a>Возвращаемое значение

Boolean

## <a name="remarks"></a>Замечания

В рабочей области технология ODBCDirect можно открыть **[набор записей](recordset-object-dao.md)** , содержащий несколько выборку в исходный аргумент **OpenRecordset**или свойство **[SQL](querydef-sql-property-dao.md)** select запроса объекта **[QueryDef](querydef-object-dao.md)** , как показано в следующем примере.

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

Результаты первого запроса открывается возвращаемых **записей** . Для получения результатов наборов записей из последующих запросов, используйте метод **NextRecordset** .

Если доступны дополнительные записи (то есть, возникла другой выборку в вызове **OpenRecordset** или в свойстве **SQL** ), записей, возвращенных из следующего запроса будет загружен в **записей**и будет **NextRecordset** Возвращает **значение True**, указывающего на то, что записи доступны. При наличии нескольких записей (то есть, результаты последнего select запроса были загружены в **набор записей**), а затем **NextRecordset** возвращает **значение False**, а **записей** будет пустым.

Можно также использовать метод **[Отменить](connection-cancel-method-dao.md)** очистить содержимое **набора записей**. Тем не менее также **Отменить** очищает любые дополнительные записи еще не загружен.

## <a name="example"></a>Пример

В этом примере используется метод **NextRecordset** для просмотра данных из составного запроса. Свойство **DefaultCursorDriver** должно иметь значение **dbUseODBCCursor** при выполнении таких запросов. Метод **NextRecordset** возвращает **значение True,** даже в том случае, если некоторые или все инструкции SELECT возвращают записей; только после проверки отдельных предложений SQL, он будет возвращать **значение False** .

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

Другой способ выполнения этой задачи является создание подготовленной инструкции, содержащий составные инструкции SQL. Свойство **CacheSize** объекта **QueryDef** должен иметь значение 1, и объект **набора записей** должен иметь только вперед и только для чтения.

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

