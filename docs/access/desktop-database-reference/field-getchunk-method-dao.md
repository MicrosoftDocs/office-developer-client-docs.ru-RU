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
ms.openlocfilehash: f8d245223549d51c49e769eedd0b92bb335357cf
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996995"
---
# <a name="fieldgetchunk-method-dao"></a><span data-ttu-id="80508-102">Метод Field.GetChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="80508-102">Field.GetChunk method (DAO)</span></span>

<span data-ttu-id="80508-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80508-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80508-104">Возвращает все или часть содержимого объекта **Memo** или **Long Binary** **[поле](field-object-dao.md)** в коллекции **[полей](fields-collection-dao.md)** объекта **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="80508-104">Returns all or a portion of the contents of a **Memo** or **Long Binary** **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="80508-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80508-105">Syntax</span></span>

<span data-ttu-id="80508-106">*выражение* . Методы GetChunk (***смещение***, ***в байтах***)</span><span class="sxs-lookup"><span data-stu-id="80508-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="80508-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="80508-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="80508-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="80508-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80508-109">Имя</span><span class="sxs-lookup"><span data-stu-id="80508-109">Name</span></span></p></th>
<th><p><span data-ttu-id="80508-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="80508-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="80508-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="80508-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="80508-112">Описание</span><span class="sxs-lookup"><span data-stu-id="80508-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80508-113"><em>Смещение</em></span><span class="sxs-lookup"><span data-stu-id="80508-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="80508-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80508-114">Required</span></span></p></td>
<td><p><span data-ttu-id="80508-115"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="80508-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="80508-116">Число байтов, пропустите перед начинается копирование.</span><span class="sxs-lookup"><span data-stu-id="80508-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80508-117"><em>Байт</em></span><span class="sxs-lookup"><span data-stu-id="80508-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="80508-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80508-118">Required</span></span></p></td>
<td><p><span data-ttu-id="80508-119"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="80508-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="80508-120">Число байтов, которые необходимо вернуть.</span><span class="sxs-lookup"><span data-stu-id="80508-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="80508-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80508-121">Return value</span></span>

<span data-ttu-id="80508-122">Variant</span><span class="sxs-lookup"><span data-stu-id="80508-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="80508-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="80508-123">Remarks</span></span>

<span data-ttu-id="80508-124">Байт, возвращаемых **GetChunk** назначаются переменной.</span><span class="sxs-lookup"><span data-stu-id="80508-124">The bytes returned by **GetChunk** are assigned to variable.</span></span> <span data-ttu-id="80508-125">Используйте **GetChunk** для возврата значения данных за раз.</span><span class="sxs-lookup"><span data-stu-id="80508-125">Use **GetChunk** to return a portion of the total data value at a time.</span></span> <span data-ttu-id="80508-126">Метод **[AppendChunk](field-appendchunk-method-dao.md)** воссоздать компоненты.</span><span class="sxs-lookup"><span data-stu-id="80508-126">You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="80508-127">Если смещение равно 0, **GetChunk** начинает копировать из первого байта ответа от поля.</span><span class="sxs-lookup"><span data-stu-id="80508-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="80508-128">Если numbytes больше, чем число байтов в поле, **GetChunk** возвращает фактическое число байтов оставшихся в соответствующем поле.</span><span class="sxs-lookup"><span data-stu-id="80508-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="80508-129">Используйте поле **Memo** для текста и поместить двоичные данные только в **Длинный двоичные** поля.</span><span class="sxs-lookup"><span data-stu-id="80508-129">Use a **Memo** field for text, and put binary data only in **Long Binary** fields.</span></span> <span data-ttu-id="80508-130">В противном случае это приведет к нежелательным результатам.</span><span class="sxs-lookup"><span data-stu-id="80508-130">Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="80508-131">Пример</span><span class="sxs-lookup"><span data-stu-id="80508-131">Example</span></span>

<span data-ttu-id="80508-132">В этом примере использует методы **AppendChunk** и **GetChunk** для заполнения поле объекта OLE с данными из другой записи 32 КБ за раз.</span><span class="sxs-lookup"><span data-stu-id="80508-132">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="80508-133">В реальном приложении один может использовать процедуру следующим образом для копирования запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="80508-133">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="80508-134">В этом примере запись просто копируется обратно в одной таблицы.</span><span class="sxs-lookup"><span data-stu-id="80508-134">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="80508-135">Обратите внимание, что все операции блока выполняется в рамках одного последовательность обновления AddNew.</span><span class="sxs-lookup"><span data-stu-id="80508-135">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
