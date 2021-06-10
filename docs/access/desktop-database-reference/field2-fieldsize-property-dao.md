---
title: Свойство Field2.FieldSize (DAO)
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
localization_priority: Normal
ms.openlocfilehash: a7dfeb33568664a6a75f9f43de64e0c24abeb09a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292806"
---
# <a name="field2fieldsize-property-dao"></a>Свойство Field2.FieldSize (DAO)


**Область применения**: Access 2013, Office 2013


Возвращает количество bytes, используемых в базе данных (а не в памяти) объекта Memo или Long Binary **Field2** в коллекции **[Fields](fields-collection-dao.md)** объекта **[Recordset.](recordset-object-dao.md)**

## <a name="syntax"></a>Синтаксис

*выражения* . FieldSize

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

Вы можете использовать **FieldSize** с помощью методов **[AppendChunk](field-appendchunk-method-dao.md)** и **[GetChunk](field-getchunk-method-dao.md)** для управления большими полями.

Так как размер поля Long Binary или Memo может превышать 64K, необходимо назначить значение, возвращенное **FieldSize,** переменной достаточно большой, чтобы сохранить переменную **Long.**

Чтобы определить размер объекта **Field2,** помимо типов Memo и Long Binary, используйте **[свойство Size.](field-size-property-dao.md)**

  - Если сервер базы данных или драйвер ODBC не поддерживают курсоры на стороне сервера.

  - Если вы используете библиотеку курсоров ODBC (то есть свойство **DefaultCursorDriver** задавалось **dbUseODBC** или **dbUseDefault,** если сервер не поддерживает курсоры на стороне сервера).

  - Если вы используете запрос без курсоров (то есть свойство **DefaultCursorDriver** настроено на **dbUseNoCursor).**

Свойство **FieldSize** и функции VBA **Len()** или **LenB()** могут возвращать различные значения, как длина одной строки. Строки хранятся в базе данных Microsoft Access в форме набора символов многобайтного набора символов (MBCS), но доступны через VBA в формате Unicode. В результате функция **Len()** всегда возвращает количество символов, **LenB** всегда возвращает число символов X 2 (Unicode использует два bytes для каждого символа), но **FieldSize** возвращает некоторое значение между строками, если в строке есть какие-либо символы MBCS. Например, если строка состоит из трех обычных символов и двух символов MBCS, **Len()** возвращает 5, **LenB()** возвращает 10, **и FieldSize** возвращает 7, сумма 1 для каждого нормального символа и 2 для каждого символа MBCS.

## <a name="example"></a>Пример

В этом примере свойство **FieldSize** используется для списка числа bytes, используемых объектами Memo и Long Binary Field в двух разных таблицах.

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

В этом примере используются методы **AppendChunk** и **GetChunk,** чтобы заполнить объектное поле OLE данными из другой записи, 32K одновременно. В реальном приложении можно использовать процедуру, похожую на эту, чтобы скопировать запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую. В этом примере запись просто копируется обратно в ту же таблицу. Обратите внимание, что все манипуляции с фрагментами проходят в одной AddNew-Update последовательности.

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
