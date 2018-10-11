---
title: Field2.FieldSize Property (DAO)
TOCTitle: FieldSize Property
ms:assetid: d609801d-7761-663f-2840-de5923bb120c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835039(v=office.15)
ms:contentKeyID: 48547976
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052870
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e87c8eba8f8db9eb54bebc9e2e7098e7c26b1b9d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479825"
---
# <a name="field2fieldsize-property-dao"></a>Field2.FieldSize Property (DAO)


**Применимо к**: Access 2013 | Office 2013


Возвращает число байтов, используемых в базе данных (а не в памяти) Memo или Long Binary **поле2** объекта в коллекции **[полей](fields-collection-dao.md)** объекта **[набора записей](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . FieldSize

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Можно использовать **основании итогового** с методами **[AppendChunk](field-appendchunk-method-dao.md)** и **[GetChunk](field-getchunk-method-dao.md)** для работы с большие поля.

Поскольку размер Long Binary или Memo поля может превышать 64 КБ, следует назначить значение, возвращенное **основании итогового** переменной, достаточное для хранения **длинный** переменной.

Чтобы определить размер объекта **поле2** отличный от Memo и длинные двоичных типов, используйте свойство **[размера](field-size-property-dao.md)** .

  - Если сервер базы данных или драйвера ODBC не не поддержки записей на стороне сервера.

  - Если вы используете библиотека курсора ODBC (то есть, **DefaultCursorDriver** свойству **dbUseODBC**или **dbUseDefault** при сервер не поддерживает записей на стороне сервера).

  - Если вы используете cursorless запроса (то есть, свойство **DefaultCursorDriver** имеет значение **dbUseNoCursor**).

Свойство **основании итогового** и функции VBA **Len()** или **LenB()** может возвращать различные значения в длине ту же строку. Строки, хранятся в базе данных Microsoft Access в нескольких байтовых символов (MBCS) формы, но предоставляется через VBA в формате Юникод. В результате функция **Len()** всегда возвращает число символов, **LenB** всегда возвращает число знаков (Юникод используется два байта для каждого символа) X 2, но **основании итогового** возвращает значение между том случае, если строка содержит символы MBCS. Например получает строку, состоящую из трех обычные символы и двух символов MBCS **Len()** возвращает 5, **LenB()** возвращает 10 и **основании итогового** возвращает 7, суммы 1 для каждого обычный знак и 2 для всех символов MBCS.

## <a name="example"></a>Пример

В этом примере используется свойство **основании итогового** получение списка число байтов, используемых объектов Memo и двоичные поля в двух различных таблицах.

```vb
    Sub FieldSizeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenDynaset) 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     Debug.Print _ 
     "Field sizes from records in Categories table" 
     
     With rstCategories 
     Debug.Print " CategoryName - " & _ 
     "Description (bytes) - Picture (bytes)" 
     
     ' Enumerate the Categories Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !CategoryName & " - " & _ 
     !Description.FieldSize & " - " & _ 
     !Picture.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     Debug.Print "Field sizes from records in Employees table" 
     
     With rstEmployees 
     Debug.Print " LastName - Notes (bytes) - " & _ 
     "Photo (bytes)" 
     
     ' Enumerate the Employees Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & " - " & _ 
     !Notes.FieldSize & " - " & !Photo.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

В этом примере использует методы **AppendChunk** и **GetChunk** для заполнения поле объекта OLE с данными из другой записи 32 КБ за раз. В реальном приложении один может использовать процедуру следующим образом для копирования запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую. В этом примере запись просто копируется обратно в одной таблицы. Обратите внимание, что все операции блока выполняется в рамках одного последовательность обновления AddNew.

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field2, _ 
     fldDestination As Field2) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```
