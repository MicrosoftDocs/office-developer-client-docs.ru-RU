---
title: Метод Field. AppendChunk (DAO)
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
# <a name="fieldappendchunk-method-dao"></a><span data-ttu-id="0897b-102">Метод Field. AppendChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="0897b-102">Field.AppendChunk method (DAO)</span></span>

<span data-ttu-id="0897b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0897b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0897b-104">Добавляет данные из строкового выражения в объект MEMO или длинного двоичного **[поля](field-object-dao.md)** в **[наборе записей](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="0897b-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0897b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0897b-105">Syntax</span></span>

<span data-ttu-id="0897b-106">*Expression* . AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="0897b-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="0897b-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="0897b-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="0897b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0897b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0897b-109">Имя</span><span class="sxs-lookup"><span data-stu-id="0897b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0897b-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="0897b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="0897b-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0897b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="0897b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0897b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0897b-113"><em>Val</em></span><span class="sxs-lookup"><span data-stu-id="0897b-113"><em>Val</em></span></span></p></td>
<td><p><span data-ttu-id="0897b-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0897b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0897b-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0897b-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0897b-116">Выражение типа Variant (String подтип) или переменная, содержащие данные, которые требуется добавить в объект <strong>field</strong> .</span><span class="sxs-lookup"><span data-stu-id="0897b-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0897b-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="0897b-117">Remarks</span></span>

<span data-ttu-id="0897b-118">Вы можете использовать методы **AppendChunk** и **[](field-getchunk-method-dao.md)** , чтобы получить доступ к подмножествам данных в поле MEMO или длинном двоичном поле.</span><span class="sxs-lookup"><span data-stu-id="0897b-118">You can use the **AppendChunk** and **[GetChunk](field-getchunk-method-dao.md)** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="0897b-119">Вы также можете использовать эти методы для экономии пространства строк при работе с полями MEMO и длинных двоичных полей.</span><span class="sxs-lookup"><span data-stu-id="0897b-119">You can also use these methods to conserve string space when you work with Memo and Long Binary fields.</span></span> <span data-ttu-id="0897b-120">Некоторые операции (например, копирование) включают временные строки.</span><span class="sxs-lookup"><span data-stu-id="0897b-120">Certain operations (copying, for example) involve temporary strings.</span></span> <span data-ttu-id="0897b-121">Если пространство строк ограничено, может потребоваться работа с фрагментами поля, а не с полем целиком.</span><span class="sxs-lookup"><span data-stu-id="0897b-121">If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="0897b-122">Если при использовании **AppendChunk**отсутствует текущая запись, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="0897b-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="0897b-123">Начальная операция **AppendChunk** (после вызова метода **[Edit](recordset-edit-method-dao.md)** или **[AddNew](recordset-addnew-method-dao.md)** ) просто поместит данные в поле, перезаписывая существующие данные.</span><span class="sxs-lookup"><span data-stu-id="0897b-123">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data.</span></span> <span data-ttu-id="0897b-124">Последующие вызовы **AppendChunk** в рамках одного сеанса **редактирования** или **AddNew** будут добавляться к существующим данным.</span><span class="sxs-lookup"><span data-stu-id="0897b-124">Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="0897b-125">Пример</span><span class="sxs-lookup"><span data-stu-id="0897b-125">Example</span></span>

<span data-ttu-id="0897b-126">В этом примере используются методы **AppendChunk** и GetObject для заполнения поля объекта OLE данными из другой записи (32 КБ) за раз. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0897b-126">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="0897b-127">В реальном приложении можно использовать такую процедуру, как копирование записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="0897b-127">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="0897b-128">В этом примере запись просто копируется обратно в ту же таблицу.</span><span class="sxs-lookup"><span data-stu-id="0897b-128">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="0897b-129">Обратите внимание, что все операции с блоками выполняются в рамках одной последовательности с обновлением с помощью метода AddNew.</span><span class="sxs-lookup"><span data-stu-id="0897b-129">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
