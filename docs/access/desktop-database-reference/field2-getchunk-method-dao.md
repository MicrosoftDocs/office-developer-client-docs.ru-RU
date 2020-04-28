---
title: Метод field2. (DAO)
TOCTitle: GetChunk method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a4b850658ca4ab36b0d4f4cbed7266d39b4ff8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292778"
---
# <a name="field2getchunk-method-dao"></a><span data-ttu-id="ba950-102">Метод field2. (DAO)</span><span class="sxs-lookup"><span data-stu-id="ba950-102">Field2.GetChunk method (DAO)</span></span>

<span data-ttu-id="ba950-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba950-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba950-104">Возвращает полностью или часть содержимого объекта **MEMO** или **длинного объекта BinaryField2** в коллекции **[Fields](fields-collection-dao.md)** объекта **[Recordset](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="ba950-104">Returns all or a portion of the contents of a **Memo** or **Long BinaryField2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba950-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba950-105">Syntax</span></span>

<span data-ttu-id="ba950-106">*Expression* . Перефрагмент (***offset***, ***bytes***)</span><span class="sxs-lookup"><span data-stu-id="ba950-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="ba950-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="ba950-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba950-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba950-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba950-109">Имя</span><span class="sxs-lookup"><span data-stu-id="ba950-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ba950-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="ba950-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ba950-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ba950-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ba950-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ba950-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba950-113"><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="ba950-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="ba950-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ba950-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ba950-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="ba950-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="ba950-116">Число байтов, которые необходимо пропустить перед началом копирования.</span><span class="sxs-lookup"><span data-stu-id="ba950-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba950-117"><em>Числа</em></span><span class="sxs-lookup"><span data-stu-id="ba950-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="ba950-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ba950-118">Required</span></span></p></td>
<td><p><span data-ttu-id="ba950-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="ba950-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="ba950-120">Число возвращаемых байтов.</span><span class="sxs-lookup"><span data-stu-id="ba950-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ba950-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba950-121">Return value</span></span>

<span data-ttu-id="ba950-122">Variant</span><span class="sxs-lookup"><span data-stu-id="ba950-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="ba950-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba950-123">Remarks</span></span>

<span data-ttu-id="ba950-124">Возвращаемые **методом GetBytes байты присваиваются переменной** .</span><span class="sxs-lookup"><span data-stu-id="ba950-124">The bytes returned by **GetChunk** are assigned to variable.</span></span> <span data-ttu-id="ba950-125">Используйте параметрического **блока** , чтобы возвратить часть значения данных за раз.</span><span class="sxs-lookup"><span data-stu-id="ba950-125">Use **GetChunk** to return a portion of the total data value at a time.</span></span> <span data-ttu-id="ba950-126">Для повторной сборки частей можно использовать метод **[AppendChunk](field-appendchunk-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="ba950-126">You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="ba950-127">Если смещение равно 0, то операция- **блок** начинает копироваться с первого байта поля.</span><span class="sxs-lookup"><span data-stu-id="ba950-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="ba950-128">Если нумбитес больше, чем число байтов в **поле, то** параметр GetBytes возвращает фактическое количество оставшихся байтов в поле.</span><span class="sxs-lookup"><span data-stu-id="ba950-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="ba950-129">Используйте поле **MEMO** для текста и разместите двоичные данные только в **длинных двоичных** полях.</span><span class="sxs-lookup"><span data-stu-id="ba950-129">Use a **Memo** field for text, and put binary data only in **Long Binary** fields.</span></span> <span data-ttu-id="ba950-130">В противном случае могут возникнуть нежелательные результаты.</span><span class="sxs-lookup"><span data-stu-id="ba950-130">Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="ba950-131">Пример</span><span class="sxs-lookup"><span data-stu-id="ba950-131">Example</span></span>

<span data-ttu-id="ba950-132">В этом примере **используются методы** **AppendChunk** и GetObject для заполнения поля объекта OLE данными из другой записи (32 КБ) за раз.</span><span class="sxs-lookup"><span data-stu-id="ba950-132">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="ba950-133">В реальном приложении можно использовать такую процедуру, как копирование записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="ba950-133">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="ba950-134">В этом примере запись просто копируется обратно в ту же таблицу.</span><span class="sxs-lookup"><span data-stu-id="ba950-134">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="ba950-135">Обратите внимание, что все операции с блоками выполняются в рамках одной последовательности с обновлением с помощью метода AddNew.</span><span class="sxs-lookup"><span data-stu-id="ba950-135">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
