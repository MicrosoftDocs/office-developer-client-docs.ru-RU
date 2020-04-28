---
title: Свойство field2. FieldSize (DAO)
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
# <a name="field2fieldsize-property-dao"></a><span data-ttu-id="92fd2-102">Свойство field2. FieldSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="92fd2-102">Field2.FieldSize property (DAO)</span></span>


<span data-ttu-id="92fd2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92fd2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="92fd2-104">Возвращает число байтов, используемых в базе данных (а не в памяти) объекта MEMO или длинного двоичного объекта **field2** в коллекции **[Fields](fields-collection-dao.md)** объекта **[Recordset](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="92fd2-104">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **Field2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="92fd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92fd2-105">Syntax</span></span>

<span data-ttu-id="92fd2-106">*Expression* . (</span><span class="sxs-lookup"><span data-stu-id="92fd2-106">*expression* .FieldSize</span></span>

<span data-ttu-id="92fd2-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="92fd2-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="92fd2-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="92fd2-108">Remarks</span></span>

<span data-ttu-id="92fd2-109">Вы можете использовать значение **FieldSize** с методами **[GetChunk](field-getchunk-method-dao.md)** **[AppendChunk и](field-appendchunk-method-dao.md)** для управления большими полями.</span><span class="sxs-lookup"><span data-stu-id="92fd2-109">You can use **FieldSize** with the **[AppendChunk](field-appendchunk-method-dao.md)** and **[GetChunk](field-getchunk-method-dao.md)** methods to manipulate large fields.</span></span>

<span data-ttu-id="92fd2-110">Так как размер длинного двоичного поля или поля MEMO может превышать 64 КБ, необходимо присвоить значение, возвращенное свойством **FieldSize** , переменной, достаточно большой для хранения **длинных** переменных.</span><span class="sxs-lookup"><span data-stu-id="92fd2-110">Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.</span></span>

<span data-ttu-id="92fd2-111">Чтобы определить размер объекта **field2** , отличного от MEMO и длинных двоичных типов, используйте свойство **[size](field-size-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="92fd2-111">To determine the size of a **Field2** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.</span></span>

  - <span data-ttu-id="92fd2-112">Если сервер базы данных или драйвер ODBC не поддерживает серверные курсоры.</span><span class="sxs-lookup"><span data-stu-id="92fd2-112">If the database server or ODBC driver does not support server-side cursors.</span></span>

  - <span data-ttu-id="92fd2-113">Если вы используете библиотеку курсоров ODBC (то есть, свойство **дефаулткурсордривер** имеет значение **дбусеодбк**или **дбуседефаулт** , если сервер не поддерживает серверные курсоры).</span><span class="sxs-lookup"><span data-stu-id="92fd2-113">If you are using the ODBC cursor library (that is, the **DefaultCursorDriver** property is set to **dbUseODBC**, or to **dbUseDefault** when the server does not support server-side cursors).</span></span>

  - <span data-ttu-id="92fd2-114">Если используется запрос, не поддерживающий курсор (то есть для свойства **дефаулткурсордривер** задано значение **дбусенокурсор**).</span><span class="sxs-lookup"><span data-stu-id="92fd2-114">If you are using a cursorless query (that is, the **DefaultCursorDriver** property is set to **dbUseNoCursor**).</span></span>

<span data-ttu-id="92fd2-115">Свойства **FieldSize** и VBA **Len ()** или **ДЛИНБ ()** могут возвращать различные значения в качестве длины одной и той же строки.</span><span class="sxs-lookup"><span data-stu-id="92fd2-115">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string.</span></span> <span data-ttu-id="92fd2-116">Строки хранятся в базе данных Microsoft Access в многобайтовых наборах символов (MBCS), но доступны через VBA в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="92fd2-116">Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format.</span></span> <span data-ttu-id="92fd2-117">В результате функция **Len ()** всегда возвращает число символов, **ДЛИНБ** всегда возвращает число символов X 2 (Юникод использует два байта для каждого символа), а значение **FieldSize** , если строка содержит какие-либо символы MBCS.</span><span class="sxs-lookup"><span data-stu-id="92fd2-117">As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters.</span></span> <span data-ttu-id="92fd2-118">Например, если указана строка, состоящая из трех обычных символов и двух символов MBCS, то функция **Len ()** возвратит значение 5, **ДЛИНБ ()** возвратит значение 10, а значение параметра **FieldSize** будет возвращать значение 7, равное 1 для каждого обычного СИМВОЛА и 2 для каждого символа MBCS.</span><span class="sxs-lookup"><span data-stu-id="92fd2-118">For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span></span>

## <a name="example"></a><span data-ttu-id="92fd2-119">Пример</span><span class="sxs-lookup"><span data-stu-id="92fd2-119">Example</span></span>

<span data-ttu-id="92fd2-120">В этом примере используется свойство **FieldSize** для перечисления числа байтов, используемых объектами MEMO и длинных двоичных полей в двух разных таблицах.</span><span class="sxs-lookup"><span data-stu-id="92fd2-120">This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.</span></span>

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

<span data-ttu-id="92fd2-121">В этом примере **используются методы** **AppendChunk** и GetObject для заполнения поля объекта OLE данными из другой записи (32 КБ) за раз.</span><span class="sxs-lookup"><span data-stu-id="92fd2-121">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="92fd2-122">В реальном приложении можно использовать такую процедуру, как копирование записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="92fd2-122">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="92fd2-123">В этом примере запись просто копируется обратно в ту же таблицу.</span><span class="sxs-lookup"><span data-stu-id="92fd2-123">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="92fd2-124">Обратите внимание, что все операции с блоками выполняются в рамках одной последовательности с обновлением с помощью метода AddNew.</span><span class="sxs-lookup"><span data-stu-id="92fd2-124">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
