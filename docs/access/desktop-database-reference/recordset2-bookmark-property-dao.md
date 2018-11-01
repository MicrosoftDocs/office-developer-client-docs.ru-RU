---
title: Recordset2.Bookmark Property (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5336c0993230b7d380b335e6f8e7eaa1af9b306c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867827"
---
# <a name="recordset2bookmark-property-dao"></a>Recordset2.Bookmark Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает закладки, который уникальным образом определяет текущую запись в объект **набора записей** .

## <a name="syntax"></a>Синтаксис

*выражение* . Закладка

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Для объекта **набора записей** на основании полностью таблиц ядра базы данных Microsoft Access значение свойства **Bookmarkable** имеет значение True, а свойство **закладки** с этого набора записей. Другие базы данных могут не поддерживать закладки, однако. Например нельзя использовать закладки в любой объект **Recordset2** для связанной таблицы Paradox, не имеющей первичного ключа.

При создании или открывает объект **набора записей** каждой записи уже имеет уникальный закладка. Можно сохранить закладку для текущей записи, присвоить значение свойства **Bookmark** переменной. Чтобы быстро вернуться на эту запись в любое время после перехода на другой записи, объекта **набора записей** **закладку** свойству присвоить значение переменной.

Нет ограничений на номер закладки, которые можно устанавливать. Чтобы создать закладку для записи, отличных от текущей записи, перемещение к нужной записи и присвоить значение свойства **Bookmark** **строковой** переменной, идентифицирующий эту запись.

Чтобы убедиться в том, что объекта **набора записей** поддерживает закладки, проверьте значению ее свойства **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** прежде чем использовать свойство **закладку** . Если свойство **Bookmarkable** имеет значение False, объект **набора записей** не поддерживает закладки и **закладок** с помощью свойства приводит к перехватываемые ошибки.

При использовании метода **[клонирования](recordset2-clone-method-dao.md)** для создания копии объекта **набора записей** параметры свойства **закладку** для исходной и повторяющихся **записей** объектов идентичны и являются взаимозаменяемыми. Тем не менее закладок из разных объектов **набора записей** нельзя использовать попеременно, даже в том случае, если они были созданы с помощью тот же объект или же инструкции SQL.

Если значение свойства **Bookmark** значение, которое представляет запись, то перехватываемые возникает ошибка.

Значение свойства **закладки** не совпадает с номером записи.

## <a name="example"></a>Пример

В этом примере с помощью свойства **закладки** и **Bookmarkable** сообщите флаг пользователя записи в наборе записей и вернуться к нему позже.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

В этом примере используется свойство **LastModified** для перемещения указатель текущей записи запись, которая была изменена и только что созданная запись.

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
