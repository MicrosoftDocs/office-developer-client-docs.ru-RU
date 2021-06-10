---
title: Метод Field2.AppendChunk (DAO)
TOCTitle: AppendChunk Method
ms:assetid: 540cd02d-1fc6-81d1-ac08-1e3df72a7208
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194088(v=office.15)
ms:contentKeyID: 48544886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052867
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fda1ab5a3e339d951225f4f43ab4275cce2cdb80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292883"
---
# <a name="field2appendchunk-method-dao"></a><span data-ttu-id="92b60-102">Метод Field2.AppendChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="92b60-102">Field2.AppendChunk method (DAO)</span></span>

<span data-ttu-id="92b60-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92b60-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92b60-104">Применит данные из строки к объекту Memo или Long Binary **Field2** в **[Наборе записей.](recordset-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="92b60-104">Appends data from a string expression to a Memo or Long Binary **Field2** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b60-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92b60-105">Syntax</span></span>

<span data-ttu-id="92b60-106">*выражения* . AppendChunk ***(Val)***</span><span class="sxs-lookup"><span data-stu-id="92b60-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="92b60-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="92b60-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="92b60-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="92b60-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92b60-109">Имя</span><span class="sxs-lookup"><span data-stu-id="92b60-109">Name</span></span></p></th>
<th><p><span data-ttu-id="92b60-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="92b60-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="92b60-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="92b60-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="92b60-112">Описание</span><span class="sxs-lookup"><span data-stu-id="92b60-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92b60-113"><em>Val</em></span><span class="sxs-lookup"><span data-stu-id="92b60-113"><em>Val</em></span></span></p></td>
<td><p><span data-ttu-id="92b60-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="92b60-114">Required</span></span></p></td>
<td><p><span data-ttu-id="92b60-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="92b60-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="92b60-116">Выражение Variant (String subtype) или переменная, содержащая данные, которые необходимо примыкать к объекту <strong>Field2.</strong></span><span class="sxs-lookup"><span data-stu-id="92b60-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field2</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="92b60-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="92b60-117">Remarks</span></span>

<span data-ttu-id="92b60-118">Вы можете использовать методы **AppendChunk** и **GetChunk** для доступа к подмесям данных в поле Memo или Long Binary.</span><span class="sxs-lookup"><span data-stu-id="92b60-118">You can use the **AppendChunk** and **GetChunk** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="92b60-119">Эти методы также можно использовать для сохранения пространства строк при работе с полями Memo и Long Binary.</span><span class="sxs-lookup"><span data-stu-id="92b60-119">You can also use these methods to conserve string space when you work with Memo and Long Binary fields.</span></span> <span data-ttu-id="92b60-120">Некоторые операции (например, копирование) включают временные строки.</span><span class="sxs-lookup"><span data-stu-id="92b60-120">Certain operations (copying, for example) involve temporary strings.</span></span> <span data-ttu-id="92b60-121">Если пространство строк ограничено, может потребоваться работать с кусками поля вместо всего поля.</span><span class="sxs-lookup"><span data-stu-id="92b60-121">If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="92b60-122">Если при использовании **AppendChunk** нет текущей записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="92b60-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="92b60-123">Первоначальная операция **AppendChunk** (после вызова **[Edit](recordset-edit-method-dao.md)** или **[AddNew)](recordset-addnew-method-dao.md)** будет просто разместить данные в поле, переописав все существующие данные.</span><span class="sxs-lookup"><span data-stu-id="92b60-123">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data.</span></span> <span data-ttu-id="92b60-124">Последующие **вызовы AppendChunk** в том же сеансе **Редактирование** или **AddNew** затем добавят к существующим данным.</span><span class="sxs-lookup"><span data-stu-id="92b60-124">Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="92b60-125">Пример</span><span class="sxs-lookup"><span data-stu-id="92b60-125">Example</span></span>

<span data-ttu-id="92b60-126">В этом примере используются методы **AppendChunk** и **GetChunk,** чтобы заполнить объектное поле OLE данными из другой записи, 32K одновременно.</span><span class="sxs-lookup"><span data-stu-id="92b60-126">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="92b60-127">В реальном приложении можно использовать процедуру, похожую на эту, чтобы скопировать запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="92b60-127">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="92b60-128">В этом примере запись просто копируется обратно в ту же таблицу.</span><span class="sxs-lookup"><span data-stu-id="92b60-128">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="92b60-129">Обратите внимание, что все манипуляции с фрагментами проходят в одной AddNew-Update последовательности.</span><span class="sxs-lookup"><span data-stu-id="92b60-129">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
