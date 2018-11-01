---
title: Recordset.CopyQueryDef Method (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: fee8c2fe-500e-dfb3-21ce-211e54ff334b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837296(v=office.15)
ms:contentKeyID: 48548950
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73bc9bb5063068dc3f29345b3828db4f7729110f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885327"
---
# <a name="recordsetcopyquerydef-method-dao"></a>Recordset.CopyQueryDef Method (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает объект **[QueryDef](querydef-object-dao.md)** , являющееся копией **QueryDef** , используемый для создания объекта **[набора записей](recordset-object-dao.md)** , представленного заполнитель набора записей (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражение* . CopyQueryDef

*выражение* Переменная, которая представляет собой объект **набора записей** .

### <a name="return-value"></a>Возвращаемое значение

QueryDef

## <a name="remarks"></a>Замечания

Метод **CopyQueryDef** можно использовать для создания нового **QueryDef** , дублирующих **QueryDef** , используемые для создания **записей**.

Если **QueryDef** не был создан этот **набор записей**, возникает ошибка. Сначала необходимо открыть **набора записей** с помощью метода **OpenRecordset** перед использованием метода **CopyQueryDef** .

Этот метод полезен, когда создание объекта **набора записей** из **QueryDef**и передать **набора записей** функции и функции необходимо повторно создать эквивалент SQL запроса, например, чтобы изменить каким-либо образом.

## <a name="example"></a>Пример

В этом примере используется метод **CopyQueryDef** для создания копии **QueryDef** из существующих **записей** и изменяет эту копию, добавив предложение свойство SQL. При создании постоянной **QueryDef**пробелы, точки с запятой или каретки могут быть добавлены к свойству SQL; необходимо очищено от вложения эти дополнительные символы, прежде чем любые новые предложения можно присоединить к инструкции SQL.

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

В этом примере показано возможное использование CopyQueryNew().

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

