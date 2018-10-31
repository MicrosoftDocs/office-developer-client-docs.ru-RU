---
title: Field.GetChunk Method (DAO)
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
ms.openlocfilehash: 691b4d0b18b31c4c4a40f73e232a1829101913f1
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863278"
---
# <a name="fieldgetchunk-method-dao"></a><span data-ttu-id="3d045-102">Field.GetChunk Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="3d045-102">Field.GetChunk Method (DAO)</span></span>


<span data-ttu-id="3d045-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d045-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3d045-104">Возвращает все или часть содержимого объекта **Memo** или **Long Binary** **[поле](field-object-dao.md)** в коллекции **[полей](fields-collection-dao.md)** объекта **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="3d045-104">Returns all or a portion of the contents of a **Memo** or **Long Binary** **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d045-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d045-105">Syntax</span></span>

<span data-ttu-id="3d045-106">*выражение* . Методы GetChunk (***смещение***, ***в байтах***)</span><span class="sxs-lookup"><span data-stu-id="3d045-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="3d045-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="3d045-107">*expression* A variable that represents a **Field** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="3d045-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d045-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d045-109">Имя</span><span class="sxs-lookup"><span data-stu-id="3d045-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3d045-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="3d045-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="3d045-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3d045-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="3d045-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3d045-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d045-113">Offset</span><span class="sxs-lookup"><span data-stu-id="3d045-113">Offset</span></span></p></td>
<td><p><span data-ttu-id="3d045-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3d045-114">Required</span></span></p></td>
<td><p><span data-ttu-id="3d045-115"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="3d045-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="3d045-116">Число байтов, пропустите перед начинается копирование.</span><span class="sxs-lookup"><span data-stu-id="3d045-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d045-117">Байт</span><span class="sxs-lookup"><span data-stu-id="3d045-117">Bytes</span></span></p></td>
<td><p><span data-ttu-id="3d045-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3d045-118">Required</span></span></p></td>
<td><p><span data-ttu-id="3d045-119"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="3d045-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="3d045-120">Число байтов, которые необходимо вернуть.</span><span class="sxs-lookup"><span data-stu-id="3d045-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3d045-121"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3d045-121"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="3d045-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d045-122">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="3d045-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d045-123">Return value</span></span>
>>>>>>> <span data-ttu-id="3d045-124">образец</span><span class="sxs-lookup"><span data-stu-id="3d045-124">master</span></span>

<span data-ttu-id="3d045-125">Variant</span><span class="sxs-lookup"><span data-stu-id="3d045-125">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="3d045-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d045-126">Remarks</span></span>

<span data-ttu-id="3d045-127">Байт, возвращаемых **GetChunk** назначаются переменной.</span><span class="sxs-lookup"><span data-stu-id="3d045-127">The bytes returned by **GetChunk** are assigned to variable.</span></span> <span data-ttu-id="3d045-128">Используйте **GetChunk** для возврата значения данных за раз.</span><span class="sxs-lookup"><span data-stu-id="3d045-128">Use **GetChunk** to return a portion of the total data value at a time.</span></span> <span data-ttu-id="3d045-129">Метод **[AppendChunk](field-appendchunk-method-dao.md)** воссоздать компоненты.</span><span class="sxs-lookup"><span data-stu-id="3d045-129">You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="3d045-130">Если смещение равно 0, **GetChunk** начинает копировать из первого байта ответа от поля.</span><span class="sxs-lookup"><span data-stu-id="3d045-130">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="3d045-131">Если numbytes больше, чем число байтов в поле, **GetChunk** возвращает фактическое число байтов оставшихся в соответствующем поле.</span><span class="sxs-lookup"><span data-stu-id="3d045-131">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>


> [!NOTE]
> <span data-ttu-id="3d045-132">Используйте поле **Memo** для текста и поместить двоичные данные только в **Длинный двоичные** поля.</span><span class="sxs-lookup"><span data-stu-id="3d045-132">Use a **Memo** field for text, and put binary data only in **Long Binary** fields.</span></span> <span data-ttu-id="3d045-133">В противном случае это приведет к нежелательным результатам.</span><span class="sxs-lookup"><span data-stu-id="3d045-133">Doing otherwise will cause undesirable results.</span></span>



## <a name="example"></a><span data-ttu-id="3d045-134">Пример</span><span class="sxs-lookup"><span data-stu-id="3d045-134">Example</span></span>

<span data-ttu-id="3d045-135">В этом примере использует методы **AppendChunk** и **GetChunk** для заполнения поле объекта OLE с данными из другой записи 32 КБ за раз.</span><span class="sxs-lookup"><span data-stu-id="3d045-135">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="3d045-136">В реальном приложении один может использовать процедуру следующим образом для копирования запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="3d045-136">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="3d045-137">В этом примере запись просто копируется обратно в одной таблицы.</span><span class="sxs-lookup"><span data-stu-id="3d045-137">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="3d045-138">Обратите внимание, что все операции блока выполняется в рамках одного последовательность обновления AddNew.</span><span class="sxs-lookup"><span data-stu-id="3d045-138">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
