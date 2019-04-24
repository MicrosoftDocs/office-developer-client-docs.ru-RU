---
title: Метод Recordset.CopyQueryDef (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: fee8c2fe-500e-dfb3-21ce-211e54ff334b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837296(v=office.15)
ms:contentKeyID: 48548950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa6c5aab5f357eef8c62c63c6fca873e64031411
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300562"
---
# <a name="recordsetcopyquerydef-method-dao"></a>Метод Recordset.CopyQueryDef (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает объект **[QueryDef](querydef-object-dao.md)**, который является копией **QueryDef** и используется для создания объекта **[Recordset](recordset-object-dao.md)**, представленного заполнителем recordset (только для рабочие области Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*Expression* . CopyQueryDef

*expression*: переменная, представляющая объект **Recordset**.

## <a name="return-value"></a>Возвращаемое значение

QueryDef

## <a name="remarks"></a>Замечания

С помощью метода **CopyQueryDef** можно создать новый объект **QueryDef** , который является дубликатом объекта **QueryDef** , использованного для создания объекта **Recordset**.

Если объект **QueryDef** не использовался для создания этого объекта **Recordset**, возникает ошибка. Прежде чем использовать метод **CopyQueryDef** , необходимо сначала открыть объект **Recordset** с помощью метода **OpenRecordset** .

Этот метод полезен при создании объекта **Recordset** из объекта **QueryDef**и передаче объекта **Recordset** в функцию, а функция должна повторно создать эквивалент SQL запроса, например, чтобы изменить его каким-либо образом.

## <a name="example"></a>Пример

В этом примере используется метод **CopyQueryDef** для создания копии объекта **QueryDef** из существующего **набора записей** и изменения копии путем добавления предложения в свойство SQL. При создании постоянного объекта **QueryDef**в свойство SQL можно добавить пробелы, пробелы, точки с запятой или символы переноса строки; Эти дополнительные символы необходимо отключать до того, как все новые предложения можно присоединить к оператору SQL.

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```

<br/>

В этом примере показано возможное использование Копикуеринев ().

```vb 
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

