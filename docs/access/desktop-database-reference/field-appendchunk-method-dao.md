---
title: Метод Field.AppendChunk (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1ce1c359582194ce87dfaf4f409be4303486e09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293170"
---
# <a name="fieldappendchunk-method-dao"></a><span data-ttu-id="8649a-102">Метод Field.AppendChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="8649a-102">Field.AppendChunk method (DAO)</span></span>

<span data-ttu-id="8649a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8649a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8649a-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8649a-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8649a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8649a-105">Syntax</span></span>

<span data-ttu-id="8649a-106">*выражение .* AppendChunk(***Val***)</span><span class="sxs-lookup"><span data-stu-id="8649a-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="8649a-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="8649a-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8649a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8649a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8649a-109">Имя</span><span class="sxs-lookup"><span data-stu-id="8649a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8649a-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="8649a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8649a-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8649a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="8649a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8649a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8649a-113"><em>Val</em></span><span class="sxs-lookup"><span data-stu-id="8649a-113"><em>Val</em></span></span></p></td>
<td><p><span data-ttu-id="8649a-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="8649a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8649a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8649a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8649a-116">Выражение Variant (строка подтипа) или переменная, содержащая данные, которые необходимо применить к <strong>объекту Field.</strong></span><span class="sxs-lookup"><span data-stu-id="8649a-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8649a-117">Заметки</span><span class="sxs-lookup"><span data-stu-id="8649a-117">Remarks</span></span>

<span data-ttu-id="8649a-118">Вы можете использовать методы **AppendChunk** и **[GetChunk](field-getchunk-method-dao.md)** для доступа к подмесям данных в поле Memo или Long Binary.</span><span class="sxs-lookup"><span data-stu-id="8649a-118">You can use the **AppendChunk** and **[GetChunk](field-getchunk-method-dao.md)** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="8649a-119">Эти методы также можно использовать для экономии строковых пространств при работе с полями Memo и Long Binary.</span><span class="sxs-lookup"><span data-stu-id="8649a-119">You can also use these methods to conserve string space when you work with Memo and Long Binary fields.</span></span> <span data-ttu-id="8649a-120">Некоторые операции (например, копирование) включают временные строки.</span><span class="sxs-lookup"><span data-stu-id="8649a-120">Certain operations (copying, for example) involve temporary strings.</span></span> <span data-ttu-id="8649a-121">Если строковая область ограничена, может потребоваться работать с блоками поля, а не с всем полем.</span><span class="sxs-lookup"><span data-stu-id="8649a-121">If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="8649a-122">Если при использовании **AppendChunk** нет текущей записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8649a-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="8649a-123">Первоначальная операция **AppendChunk** (после вызова **[Edit](recordset-edit-method-dao.md)** или **[AddNew)](recordset-addnew-method-dao.md)** просто поместите данные в поле, переописав все существующие данные.</span><span class="sxs-lookup"><span data-stu-id="8649a-123">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data.</span></span> <span data-ttu-id="8649a-124">Последующие **вызовы AppendChunk** в рамках одного и того же сеанса **Edit** или **AddNew** затем добавляются к существующим данным.</span><span class="sxs-lookup"><span data-stu-id="8649a-124">Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="8649a-125">Пример</span><span class="sxs-lookup"><span data-stu-id="8649a-125">Example</span></span>

<span data-ttu-id="8649a-126">В этом примере используются методы **AppendChunk** и **GetChunk** для заполнения поля объекта OLE данными из другой записи по 32K одновременно.</span><span class="sxs-lookup"><span data-stu-id="8649a-126">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="8649a-127">В реальном приложении можно использовать процедуру, похожую на эту, для копирования записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="8649a-127">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="8649a-128">В этом примере запись просто копируется обратно в ту же таблицу.</span><span class="sxs-lookup"><span data-stu-id="8649a-128">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="8649a-129">Обратите внимание, что все манипуляции с блоками происходит в одной AddNew-Update последовательности.</span><span class="sxs-lookup"><span data-stu-id="8649a-129">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
