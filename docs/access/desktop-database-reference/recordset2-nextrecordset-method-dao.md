---
title: Метод Recordset2.NextRecordset (DAO)
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
# <a name="recordset2nextrecordset-method-dao"></a>Метод Recordset2.NextRecordset (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* NextRecordset

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="return-value"></a>Возвращаемое значение

Boolean

## <a name="remarks"></a>Примечания

В рабочей области ODBCDirect можно  открыть набор записей, содержащий несколько запросов выбора в аргументе источника **OpenRecordset,** или свойство **[SQL](querydef-sql-property-dao.md)** объекта **[select queryDef,](querydef-object-dao.md)** как по примеру ниже.

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

Возвращенный **набор записей** откроется с результатами первого запроса. Чтобы получить наборы результатов записей из последующих запросов, используйте метод **NextRecordset.**

Если доступно больше записей (то есть в вызове **OpenRecordset** или в свойстве **SQL** был другой запрос выбора), записи, возвращенные из следующего запроса, будут загружены в набор **записей,** а **NextRecordset** возвратит **true,** указав, что записи доступны. Если больше нет доступных записей (то есть результаты последнего выбранного запроса были загружены в набор записей),  **nextRecordset** возвратит **false,** и набор записей будет пустым. 

Вы также можете использовать метод **[Cancel](connection-cancel-method-dao.md)** для очистки содержимого **recordset.** Однако **отмена** также очищает все дополнительные записи, которые еще не загружены.

## <a name="example"></a>Пример

В этом примере используется **метод NextRecordset** для просмотра данных из составного запроса SELECT. При выполнении таких запросов для свойства **DefaultCursorDriver** необходимо установить значение **dbUseODBCCursor.** Метод **NextRecordset** возвращает **значение True,** даже если некоторые или все утверждения SELECT возвращают ноль записей; Он возвращает **false** только после проверки всех SQL условий.

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

Другой способ выполнить ту же задачу заключается в создании подготовленного заявления, содержащего составную SQL. Свойство **CacheSize** объекта **QueryDef** должно иметь приоритет 1, а объект **Recordset** должен быть только для перенастройки и только для чтения.

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

