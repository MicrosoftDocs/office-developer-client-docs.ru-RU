---
title: Свойство Recordset2. Bookmark (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31791e9fb3c7081989232e36a90b184ed7e31866
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307450"
---
# <a name="recordset2bookmark-property-dao"></a>Свойство Recordset2. Bookmark (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает закладку, которая уникально определяет текущую запись в объекте **Recordset**.

## <a name="syntax"></a>Синтаксис

*expression* .Bookmark

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Примечания

Для объекта **Recordset** целиком на основе таблиц ядра СУБД Microsoft Access значение свойства **Bookmark** равно true, и можно использовать свойство **Bookmark** с этим набором записей. Другие продукты базы данных, однако, могут не поддерживать закладки. Например, нельзя использовать закладки в любом объекте **Recordset2** на основе связанной таблицы Paradox, не имеющей первичного ключа.

Когда вы создаете и открываете объект **Recordset**, каждая его запись уже имеет уникальную закладку. Вы можете сохранить закладку для текущей записи, назначив значение для свойства **Bookmark** для переменной. Чтобы быстро в любое время вернуться к данной записи после перехода к другой записи, задайте в объекте **Recordset** для свойства **Bookmark** значение данной переменной.

Не существует ограничений для количества закладок, которое вы можете создать. Чтобы создать закладку для записи, отличной от текущей записи, перейдите к нужной записи и назначьте для свойства **Bookmark** значение переменной **String**, которая определяет запись.

Чтобы убедиться, что объект **Recordset** поддерживает закладки, проверьте значение его свойства **[Bookmarkable](recordset2-bookmarkable-property-dao.md)**, прежде чем использовать свойство **Bookmark**. Если свойство **Bookmarkable** имеет значение False, объект **Recordset** не поддерживает закладки, а использование свойства **Bookmark** приведет к возникновению перехватываемой ошибки.

Если вы используете метод **[Clone](recordset2-clone-method-dao.md)** для создания копии объекта **Recordset**, настройки свойства **Bookmark** для исходного и дублирующего объектов **Recordset** не отличаются и являются взаимозаменяемыми. Однако, нельзя использовать закладки из разных объектов **Recordset** в качестве замены друг другу,, даже если они были созданы с помощью одного и того же объекта или оператора SQL.

Если установить для свойства **Bookmark** значение, которое представляет удаленную запись, возникает перехватываемая ошибка.

Значение свойства **Bookmark** не повторяет номер записи.

## <a name="example"></a>Пример

В этом примере используются **закладки** и свойства с **закладками** , позволяющие пользователю пометить запись в объекте Recordset и вернуться к нему позже.

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

В этом примере используется свойство **LastModified**, чтобы переместить указатель текущей записи на измененную и заново созданную записи.

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
