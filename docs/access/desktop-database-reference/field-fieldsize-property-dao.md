---
title: Свойство Field. FieldSize (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 68a1b354b27515dd855703b9bf6344e4a9e90d7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293114"
---
# <a name="fieldfieldsize-property-dao"></a>Свойство Field. FieldSize (DAO)


**Область применения**: Access 2013, Office 2013


Возвращает число байтов, используемых в базе данных (а не в памяти) объекта MEMO или длинного двоичного **[поля](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** объекта **[Recordset](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*Expression* . (

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Комментарии

Вы можете использовать значение **FieldSize** с методами **[](field-getchunk-method-dao.md)** **[AppendChunk и](field-appendchunk-method-dao.md)** для управления большими полями.

Так как размер длинного двоичного поля или поля MEMO может превышать 64 КБ, необходимо присвоить значение, возвращенное свойством **FieldSize** , переменной, достаточно большой для хранения **длинных** переменных.

Чтобы определить размер объекта **поля** , отличноГо от MEMO и длинных двоичных типов, используйте свойство **[size](field-size-property-dao.md)** .

  - Если сервер базы данных или драйвер ODBC не поддерживает серверные курсоры.

  - Если вы используете библиотеку курсоров ODBC (то есть, свойство **дефаулткурсордривер** имеет значение **дбусеодбк**или **дбуседефаулт** , если сервер не поддерживает серверные курсоры).

  - Если используется запрос, не поддерживающий курсор (то есть для свойства **дефаулткурсордривер** задано значение **дбусенокурсор**).

Свойства **FieldSize** и VBA **Len ()** или **ДЛИНБ ()** могут возвращать различные значения в качестве длины одной и той же строки. Строки хранятся в базе данных Microsoft Access в многобайтовых наборах символов (MBCS), но доступны через VBA в формате Юникод. В результате функция **Len ()** всегда возвращает число символов, **ДЛИНБ** всегда возвращает число символов X 2 (Юникод использует два байта для каждого символа), а значение **FieldSize** возвращает некоторое значение между строкой. содержит любые символы многоБАЙТовой КОДИРОВКи. Например, если указана строка, состоящая из трех обычных символов и двух символов MBCS, то функция **Len ()** возвратит значение 5, **ДЛИНБ ()** возвратит значение 10, а значение параметра **FieldSize** будет возвращать значение 7, равное 1 для каждого обычного СИМВОЛА и 2 для каждого символа MBCS.

## <a name="example"></a>Пример

В этом примере используется свойство **FieldSize** для перечисления числа байтов, используемых объектами MEMO и длинных двоичных полей в двух разных таблицах.

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

В этом примере используются методы **AppendChunk** и GetObject для заполнения поля объекта OLE данными из другой записи (32 КБ) за раз. **** В реальном приложении можно использовать такую процедуру, как копирование записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую. В этом примере запись просто копируется обратно в ту же таблицу. Обратите внимание, что все операции с блоками выполняются в рамках одной последовательности с обновлением с помощью метода AddNew.

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
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
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
