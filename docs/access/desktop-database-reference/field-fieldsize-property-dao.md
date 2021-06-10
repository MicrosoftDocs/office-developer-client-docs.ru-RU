---
title: Свойство Field.FieldSize (DAO)
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
# <a name="fieldfieldsize-property-dao"></a><span data-ttu-id="22239-102">Свойство Field.FieldSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="22239-102">Field.FieldSize property (DAO)</span></span>


<span data-ttu-id="22239-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22239-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="22239-104">Возвращает количество bytes, используемых в базе данных (а не в памяти) объекта Memo или Long Binary **[Field](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** объекта **[Recordset.](recordset-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="22239-104">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="22239-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22239-105">Syntax</span></span>

<span data-ttu-id="22239-106">*выражения* . FieldSize</span><span class="sxs-lookup"><span data-stu-id="22239-106">*expression* .FieldSize</span></span>

<span data-ttu-id="22239-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="22239-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="22239-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="22239-108">Remarks</span></span>

<span data-ttu-id="22239-109">Вы можете использовать **FieldSize** с помощью методов **[AppendChunk](field-appendchunk-method-dao.md)** и **[GetChunk](field-getchunk-method-dao.md)** для управления большими полями.</span><span class="sxs-lookup"><span data-stu-id="22239-109">You can use **FieldSize** with the **[AppendChunk](field-appendchunk-method-dao.md)** and **[GetChunk](field-getchunk-method-dao.md)** methods to manipulate large fields.</span></span>

<span data-ttu-id="22239-110">Так как размер поля Long Binary или Memo может превышать 64K, необходимо назначить значение, возвращенное **FieldSize,** переменной достаточно большой, чтобы сохранить переменную **Long.**</span><span class="sxs-lookup"><span data-stu-id="22239-110">Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.</span></span>

<span data-ttu-id="22239-111">Чтобы определить размер объекта **Field,** помимо типов Memo и Long Binary, используйте **[свойство Size.](field-size-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="22239-111">To determine the size of a **Field** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.</span></span>

  - <span data-ttu-id="22239-112">Если сервер базы данных или драйвер ODBC не поддерживают курсоры на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="22239-112">If the database server or ODBC driver does not support server-side cursors.</span></span>

  - <span data-ttu-id="22239-113">Если вы используете библиотеку курсоров ODBC (то есть свойство **DefaultCursorDriver** задавалось **dbUseODBC** или **dbUseDefault,** если сервер не поддерживает курсоры на стороне сервера).</span><span class="sxs-lookup"><span data-stu-id="22239-113">If you are using the ODBC cursor library (that is, the **DefaultCursorDriver** property is set to **dbUseODBC**, or to **dbUseDefault** when the server does not support server-side cursors).</span></span>

  - <span data-ttu-id="22239-114">Если вы используете запрос без курсоров (то есть свойство **DefaultCursorDriver** настроено на **dbUseNoCursor).**</span><span class="sxs-lookup"><span data-stu-id="22239-114">If you are using a cursorless query (that is, the **DefaultCursorDriver** property is set to **dbUseNoCursor**).</span></span>

<span data-ttu-id="22239-115">Свойство **FieldSize** и функции VBA **Len()** или **LenB()** могут возвращать различные значения, как длина одной строки.</span><span class="sxs-lookup"><span data-stu-id="22239-115">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string.</span></span> <span data-ttu-id="22239-116">Строки хранятся в базе данных Microsoft Access в форме набора символов многобайтного набора символов (MBCS), но доступны через VBA в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="22239-116">Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format.</span></span> <span data-ttu-id="22239-117">В результате функция **Len()** всегда возвращает количество символов, **LenB** всегда возвращает число символов X 2 (Unicode использует два bytes для каждого символа), но **FieldSize** возвращает некоторое значение между строками, если в строке есть какие-либо символы MBCS.</span><span class="sxs-lookup"><span data-stu-id="22239-117">As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters.</span></span> <span data-ttu-id="22239-118">Например, если строка состоит из трех обычных символов и двух символов MBCS, **Len()** возвращает 5, **LenB()** возвращает 10, **и FieldSize** возвращает 7, сумма 1 для каждого нормального символа и 2 для каждого символа MBCS.</span><span class="sxs-lookup"><span data-stu-id="22239-118">For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span></span>

## <a name="example"></a><span data-ttu-id="22239-119">Пример</span><span class="sxs-lookup"><span data-stu-id="22239-119">Example</span></span>

<span data-ttu-id="22239-120">В этом примере свойство **FieldSize** используется для списка числа bytes, используемых объектами Memo и Long Binary Field в двух разных таблицах.</span><span class="sxs-lookup"><span data-stu-id="22239-120">This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.</span></span>

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

<span data-ttu-id="22239-121">В этом примере используются методы **AppendChunk** и **GetChunk,** чтобы заполнить объектное поле OLE данными из другой записи, 32K одновременно.</span><span class="sxs-lookup"><span data-stu-id="22239-121">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="22239-122">В реальном приложении можно использовать процедуру, похожую на эту, чтобы скопировать запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="22239-122">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="22239-123">В этом примере запись просто копируется обратно в ту же таблицу.</span><span class="sxs-lookup"><span data-stu-id="22239-123">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="22239-124">Обратите внимание, что все манипуляции с фрагментами проходят в одной AddNew-Update последовательности.</span><span class="sxs-lookup"><span data-stu-id="22239-124">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
