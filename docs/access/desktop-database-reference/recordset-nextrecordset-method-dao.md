---
title: Метод Recordset.NextRecordset (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 4a3a6176-0aa0-efb6-b175-dbe23e266abc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193483(v=office.15)
ms:contentKeyID: 48544664
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 39e508830b41e7b3f74f548451a30132723d210f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284499"
---
# <a name="recordsetnextrecordset-method-dao"></a>Метод Recordset.NextRecordset (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . NextRecordset

*expression*: переменная, представляющая объект **Recordset**.

## <a name="return-value"></a>Возвращаемое значение

Boolean

## <a name="remarks"></a>Примечания

В рабочей области ODBCDirect можно открыть объект **[Recordset](recordset-object-dao.md)** , содержащий несколько запросов на выборку в аргументе Source объекта **OpenRecordset**, или свойство **[SQL](querydef-sql-property-dao.md)** объекта "Select Query **[QueryDef](querydef-object-dao.md)** ", как показано в следующем примере.

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

Возвращенный **набор записей** будет открыт с результатами первого запроса. Чтобы получить результирующие наборы записей из последующих запросов, используйте метод **NextRecordset** .

Если доступны дополнительные записи (то есть еще один запрос SELECT в вызове **OpenRecordset** или в свойстве **SQL** ), то записи, возвращенные из следующего запроса, будут загружены в **набор записей**, и **NextRecordset** будет Возвращает **значение true**, указывающее, что доступны записи. Если нет доступных записей (то есть результаты последнего запроса SELECT были загружены в **набор записей**), то **NextRecordset** будет возвращать **значение false**, а **набор записей** будет пустым.

Кроме того, можно использовать метод **[Cancel](connection-cancel-method-dao.md)** для очистки содержимого объекта **Recordset**. Тем не менее, **Отмена** также очищает все дополнительные записи, еще не загруженные.

## <a name="example"></a>Пример

В этом примере используется метод **NextRecordset** для просмотра данных из составного запроса на выборку. При выполнении таких запросов свойству **дефаулткурсордривер** должно быть присвоено значение **дбусеодбккурсор** . Метод **NextRecordset** будет возвращать **значение true** , даже если некоторые или все инструкции SELECT возвращают нулевые записи; он возвратит **значение false** только после того, как все отдельные предложения SQL будут проверены.

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

Другой способ выполнить ту же задачу — создать подготовленный оператор, содержащий составной оператор SQL. Свойству **CacheSize** объекта **QueryDef** должно быть присвоено значение 1, а объект **Recordset** должен быть доступен только для чтения и доступен только для чтения.

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

