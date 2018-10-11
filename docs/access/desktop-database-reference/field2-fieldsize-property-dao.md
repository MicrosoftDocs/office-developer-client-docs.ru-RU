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
# <a name="field2fieldsize-property-dao"></a><span data-ttu-id="7c692-102">Field2.FieldSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c692-102">Field2.FieldSize Property (DAO)</span></span>


<span data-ttu-id="7c692-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c692-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="7c692-104">Возвращает число байтов, используемых в базе данных (а не в памяти) Memo или Long Binary **поле2** объекта в коллекции **[полей](fields-collection-dao.md)** объекта **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="7c692-104">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **Field2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c692-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c692-105">Syntax</span></span>

<span data-ttu-id="7c692-106">*выражение* . FieldSize</span><span class="sxs-lookup"><span data-stu-id="7c692-106">*expression* .FieldSize</span></span>

<span data-ttu-id="7c692-107">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="7c692-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c692-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="7c692-108">Remarks</span></span>

<span data-ttu-id="7c692-109">Можно использовать **основании итогового** с методами **[AppendChunk](field-appendchunk-method-dao.md)** и **[GetChunk](field-getchunk-method-dao.md)** для работы с большие поля.</span><span class="sxs-lookup"><span data-stu-id="7c692-109">You can use **FieldSize** with the **[AppendChunk](field-appendchunk-method-dao.md)** and **[GetChunk](field-getchunk-method-dao.md)** methods to manipulate large fields.</span></span>

<span data-ttu-id="7c692-110">Поскольку размер Long Binary или Memo поля может превышать 64 КБ, следует назначить значение, возвращенное **основании итогового** переменной, достаточное для хранения **длинный** переменной.</span><span class="sxs-lookup"><span data-stu-id="7c692-110">Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.</span></span>

<span data-ttu-id="7c692-111">Чтобы определить размер объекта **поле2** отличный от Memo и длинные двоичных типов, используйте свойство **[размера](field-size-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="7c692-111">To determine the size of a **Field2** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.</span></span>

  - <span data-ttu-id="7c692-112">Если сервер базы данных или драйвера ODBC не не поддержки записей на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="7c692-112">If the database server or ODBC driver does not support server-side cursors.</span></span>

  - <span data-ttu-id="7c692-113">Если вы используете библиотека курсора ODBC (то есть, **DefaultCursorDriver** свойству **dbUseODBC**или **dbUseDefault** при сервер не поддерживает записей на стороне сервера).</span><span class="sxs-lookup"><span data-stu-id="7c692-113">If you are using the ODBC cursor library (that is, the **DefaultCursorDriver** property is set to **dbUseODBC**, or to **dbUseDefault** when the server does not support server-side cursors).</span></span>

  - <span data-ttu-id="7c692-114">Если вы используете cursorless запроса (то есть, свойство **DefaultCursorDriver** имеет значение **dbUseNoCursor**).</span><span class="sxs-lookup"><span data-stu-id="7c692-114">If you are using a cursorless query (that is, the **DefaultCursorDriver** property is set to **dbUseNoCursor**).</span></span>

<span data-ttu-id="7c692-115">Свойство **основании итогового** и функции VBA **Len()** или **LenB()** может возвращать различные значения в длине ту же строку.</span><span class="sxs-lookup"><span data-stu-id="7c692-115">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string.</span></span> <span data-ttu-id="7c692-116">Строки, хранятся в базе данных Microsoft Access в нескольких байтовых символов (MBCS) формы, но предоставляется через VBA в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7c692-116">Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format.</span></span> <span data-ttu-id="7c692-117">В результате функция **Len()** всегда возвращает число символов, **LenB** всегда возвращает число знаков (Юникод используется два байта для каждого символа) X 2, но **основании итогового** возвращает значение между том случае, если строка содержит символы MBCS.</span><span class="sxs-lookup"><span data-stu-id="7c692-117">As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters.</span></span> <span data-ttu-id="7c692-118">Например получает строку, состоящую из трех обычные символы и двух символов MBCS **Len()** возвращает 5, **LenB()** возвращает 10 и **основании итогового** возвращает 7, суммы 1 для каждого обычный знак и 2 для всех символов MBCS.</span><span class="sxs-lookup"><span data-stu-id="7c692-118">For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span></span>

## <a name="example"></a><span data-ttu-id="7c692-119">Пример</span><span class="sxs-lookup"><span data-stu-id="7c692-119">Example</span></span>

<span data-ttu-id="7c692-120">В этом примере используется свойство **основании итогового** получение списка число байтов, используемых объектов Memo и двоичные поля в двух различных таблицах.</span><span class="sxs-lookup"><span data-stu-id="7c692-120">This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.</span></span>

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

<span data-ttu-id="7c692-121">В этом примере использует методы **AppendChunk** и **GetChunk** для заполнения поле объекта OLE с данными из другой записи 32 КБ за раз.</span><span class="sxs-lookup"><span data-stu-id="7c692-121">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="7c692-122">В реальном приложении один может использовать процедуру следующим образом для копирования запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="7c692-122">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="7c692-123">В этом примере запись просто копируется обратно в одной таблицы.</span><span class="sxs-lookup"><span data-stu-id="7c692-123">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="7c692-124">Обратите внимание, что все операции блока выполняется в рамках одного последовательность обновления AddNew.</span><span class="sxs-lookup"><span data-stu-id="7c692-124">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
