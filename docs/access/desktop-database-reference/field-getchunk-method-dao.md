---
title: Метод Field.GetChunk (DAO)
TOCTitle: GetChunk Method
ms:assetid: b8984e79-54f7-8052-85a3-d12033daf7a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822448(v=office.15)
ms:contentKeyID: 48547328
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052871
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c7eabceb1f7c130e349428aeb6b2dc079fe4319d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293100"
---
# <a name="fieldgetchunk-method-dao"></a><span data-ttu-id="329c8-102">Метод Field.GetChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="329c8-102">Field.GetChunk method (DAO)</span></span>

<span data-ttu-id="329c8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="329c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="329c8-104">Возвращает все или часть содержимого объекта **Memo** или **Long Binary** **[Field](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** объекта **[Recordset.](recordset-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="329c8-104">Returns all or a portion of the contents of a **Memo** or **Long Binary** **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="329c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="329c8-105">Syntax</span></span>

<span data-ttu-id="329c8-106">*выражение .* GetChunk(***Offset***, ***Bytes***)</span><span class="sxs-lookup"><span data-stu-id="329c8-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="329c8-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="329c8-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="329c8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="329c8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="329c8-109">Имя</span><span class="sxs-lookup"><span data-stu-id="329c8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="329c8-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="329c8-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="329c8-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="329c8-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="329c8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="329c8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="329c8-113"><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="329c8-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="329c8-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="329c8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="329c8-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="329c8-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="329c8-116">Количество пропущенных перед началом копирования количеством пропусков.</span><span class="sxs-lookup"><span data-stu-id="329c8-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="329c8-117"><em>Bytes</em></span><span class="sxs-lookup"><span data-stu-id="329c8-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="329c8-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="329c8-118">Required</span></span></p></td>
<td><p><span data-ttu-id="329c8-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="329c8-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="329c8-120">Количество возвращаемого количества ветвей.</span><span class="sxs-lookup"><span data-stu-id="329c8-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="329c8-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="329c8-121">Return value</span></span>

<span data-ttu-id="329c8-122">Variant</span><span class="sxs-lookup"><span data-stu-id="329c8-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="329c8-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="329c8-123">Remarks</span></span>

<span data-ttu-id="329c8-124">Возвращаемая **GetChunk** величина вбавляет в переменную.</span><span class="sxs-lookup"><span data-stu-id="329c8-124">The bytes returned by **GetChunk** are assigned to variable.</span></span> <span data-ttu-id="329c8-125">Используйте **GetChunk** для возврата части общего значения данных за раз.</span><span class="sxs-lookup"><span data-stu-id="329c8-125">Use **GetChunk** to return a portion of the total data value at a time.</span></span> <span data-ttu-id="329c8-126">Для повторной разборки фрагментов можно использовать метод **[AppendChunk.](field-appendchunk-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="329c8-126">You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="329c8-127">Если смещение 0, **GetChunk** начинает копировать из первого byte поля.</span><span class="sxs-lookup"><span data-stu-id="329c8-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="329c8-128">Если количество оставшихся в поле больше количества, **GetChunk** возвращает фактическое количество оставшихся в поле.</span><span class="sxs-lookup"><span data-stu-id="329c8-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="329c8-129">Используйте поле **Memo** для текста и поместите двоичные данные только в **длинные двоичные** поля.</span><span class="sxs-lookup"><span data-stu-id="329c8-129">Use a **Memo** field for text, and put binary data only in **Long Binary** fields.</span></span> <span data-ttu-id="329c8-130">В противном случае это приведет к нежелательным результатам.</span><span class="sxs-lookup"><span data-stu-id="329c8-130">Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="329c8-131">Пример</span><span class="sxs-lookup"><span data-stu-id="329c8-131">Example</span></span>

<span data-ttu-id="329c8-132">В этом примере используются методы **AppendChunk** и **GetChunk** для заполнения поля объекта OLE данными из другой записи 32K одновременно.</span><span class="sxs-lookup"><span data-stu-id="329c8-132">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="329c8-133">В реальном приложении можно использовать процедуру, похожую на эту, для копирования записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="329c8-133">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="329c8-134">В этом примере запись просто копируется обратно в ту же таблицу.</span><span class="sxs-lookup"><span data-stu-id="329c8-134">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="329c8-135">Обратите внимание, что все манипуляции с блоками происходит в одной AddNew-Update последовательности.</span><span class="sxs-lookup"><span data-stu-id="329c8-135">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
