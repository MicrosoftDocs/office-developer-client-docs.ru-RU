---
title: Field2.GetChunk Method (DAO)
TOCTitle: GetChunk Method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39501d9f39c1275e9020ee228ec2ec0a4169f40f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482944"
---
# <a name="field2getchunk-method-dao"></a><span data-ttu-id="d663d-102">Field2.GetChunk Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="d663d-102">Field2.GetChunk Method (DAO)</span></span>


<span data-ttu-id="d663d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d663d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d663d-104">Возвращает все или часть содержимого **Memo** или **Длинный BinaryField2** объекта в коллекции **[полей](fields-collection-dao.md)** объекта **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="d663d-104">Returns all or a portion of the contents of a **Memo** or **Long BinaryField2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d663d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d663d-105">Syntax</span></span>

<span data-ttu-id="d663d-106">*выражение* . Методы GetChunk (***смещение***, ***в байтах***)</span><span class="sxs-lookup"><span data-stu-id="d663d-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="d663d-107">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="d663d-107">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="d663d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d663d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d663d-109">Имя</span><span class="sxs-lookup"><span data-stu-id="d663d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d663d-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="d663d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d663d-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d663d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="d663d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d663d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d663d-113">Offset</span><span class="sxs-lookup"><span data-stu-id="d663d-113">Offset</span></span></p></td>
<td><p><span data-ttu-id="d663d-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d663d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d663d-115"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="d663d-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d663d-116">Число байтов, пропустите перед начинается копирование.</span><span class="sxs-lookup"><span data-stu-id="d663d-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d663d-117">Байт</span><span class="sxs-lookup"><span data-stu-id="d663d-117">Bytes</span></span></p></td>
<td><p><span data-ttu-id="d663d-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d663d-118">Required</span></span></p></td>
<td><p><span data-ttu-id="d663d-119"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="d663d-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d663d-120">Число байтов, которые необходимо вернуть.</span><span class="sxs-lookup"><span data-stu-id="d663d-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d663d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d663d-121">Return Value</span></span>

<span data-ttu-id="d663d-122">Variant</span><span class="sxs-lookup"><span data-stu-id="d663d-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="d663d-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="d663d-123">Remarks</span></span>

<span data-ttu-id="d663d-124">Байт, возвращаемых **GetChunk** назначаются переменной.</span><span class="sxs-lookup"><span data-stu-id="d663d-124">The bytes returned by **GetChunk** are assigned to variable.</span></span> <span data-ttu-id="d663d-125">Используйте **GetChunk** для возврата значения данных за раз.</span><span class="sxs-lookup"><span data-stu-id="d663d-125">Use **GetChunk** to return a portion of the total data value at a time.</span></span> <span data-ttu-id="d663d-126">Метод **[AppendChunk](field-appendchunk-method-dao.md)** воссоздать компоненты.</span><span class="sxs-lookup"><span data-stu-id="d663d-126">You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="d663d-127">Если смещение равно 0, **GetChunk** начинает копировать из первого байта ответа от поля.</span><span class="sxs-lookup"><span data-stu-id="d663d-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="d663d-128">Если numbytes больше, чем число байтов в поле, **GetChunk** возвращает фактическое число байтов оставшихся в соответствующем поле.</span><span class="sxs-lookup"><span data-stu-id="d663d-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d663d-129">Используйте поле <STRONG>Memo</STRONG> для текста и поместить двоичные данные только в <STRONG>Длинный двоичные</STRONG> поля.</span><span class="sxs-lookup"><span data-stu-id="d663d-129">Use a <STRONG>Memo</STRONG> field for text, and put binary data only in <STRONG>Long Binary</STRONG> fields.</span></span> <span data-ttu-id="d663d-130">В противном случае это приведет к нежелательным результатам.</span><span class="sxs-lookup"><span data-stu-id="d663d-130">Doing otherwise will cause undesirable results.</span></span></P>



## <a name="example"></a><span data-ttu-id="d663d-131">Пример</span><span class="sxs-lookup"><span data-stu-id="d663d-131">Example</span></span>

<span data-ttu-id="d663d-132">В этом примере использует методы **AppendChunk** и **GetChunk** для заполнения поле объекта OLE с данными из другой записи 32 КБ за раз.</span><span class="sxs-lookup"><span data-stu-id="d663d-132">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="d663d-133">В реальном приложении один может использовать процедуру следующим образом для копирования запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="d663d-133">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="d663d-134">В этом примере запись просто копируется обратно в одной таблицы.</span><span class="sxs-lookup"><span data-stu-id="d663d-134">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="d663d-135">Обратите внимание, что все операции блока выполняется в рамках одного последовательность обновления AddNew.</span><span class="sxs-lookup"><span data-stu-id="d663d-135">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
