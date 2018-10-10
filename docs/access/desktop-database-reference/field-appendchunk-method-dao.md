---
title: Field.AppendChunk Method (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2ba2009bb9b8ccbde52c3b521c0551bf803fdb1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482675"
---
# <a name="fieldappendchunk-method-dao"></a><span data-ttu-id="8f6d6-102">Field.AppendChunk Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="8f6d6-102">Field.AppendChunk Method (DAO)</span></span>

<span data-ttu-id="8f6d6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f6d6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8f6d6-104">Добавление данных из строковое выражение Memo или Long Binary **[поля](field-object-dao.md)** объект в **[набора записей](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f6d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f6d6-105">Syntax</span></span>

<span data-ttu-id="8f6d6-106">*выражение* . AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="8f6d6-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="8f6d6-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="8f6d6-107">*expression* A variable that represents a **Field** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8f6d6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f6d6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f6d6-109">Имя</span><span class="sxs-lookup"><span data-stu-id="8f6d6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8f6d6-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="8f6d6-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8f6d6-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8f6d6-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8f6d6-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8f6d6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f6d6-113">Функция Val</span><span class="sxs-lookup"><span data-stu-id="8f6d6-113">Val</span></span></p></td>
<td><p><span data-ttu-id="8f6d6-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8f6d6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8f6d6-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8f6d6-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8f6d6-116">Выражение типа Variant (String подтип) или переменная, содержащая данные необходимо добавить объект <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="8f6d6-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8f6d6-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f6d6-117">Remarks</span></span>

<span data-ttu-id="8f6d6-118">Методы **AppendChunk** и **[GetChunk](field-getchunk-method-dao.md)** для доступа к подмножества данных можно использовать в полей Memo или Long Binary.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-118">You can use the **AppendChunk** and **[GetChunk](field-getchunk-method-dao.md)** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="8f6d6-119">Можно также использовать эти методы для экономии места строку при работе с полей Memo и Long Binary.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-119">You can also use these methods to conserve string space when you work with Memo and Long Binary fields.</span></span> <span data-ttu-id="8f6d6-120">Некоторые операции (например, копирование) включают временных строк.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-120">Certain operations (copying, for example) involve temporary strings.</span></span> <span data-ttu-id="8f6d6-121">Если строка ограничено, может потребоваться работать с частями поля, а не всего поля.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-121">If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="8f6d6-122">Если при использовании **AppendChunk**нет текущей записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="8f6d6-123">Начальное операция **AppendChunk** (после **[изменения](recordset-edit-method-dao.md)** или **[AddNew](recordset-addnew-method-dao.md)** вызова) будет просто поместить данные в поле перезапись существующих данных.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-123">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data.</span></span> <span data-ttu-id="8f6d6-124">Последующие **AppendChunk** вызывает в пределах того же **Изменение** или сеанса **AddNew** затем будут добавлены в существующих данных.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-124">Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="8f6d6-125">Пример</span><span class="sxs-lookup"><span data-stu-id="8f6d6-125">Example</span></span>

<span data-ttu-id="8f6d6-126">В этом примере использует методы **AppendChunk** и **GetChunk** для заполнения поле объекта OLE с данными из другой записи 32 КБ за раз.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-126">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time.</span></span> <span data-ttu-id="8f6d6-127">В реальном приложении один может использовать процедуру следующим образом для копирования запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-127">In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another.</span></span> <span data-ttu-id="8f6d6-128">В этом примере запись просто копируется обратно в одной таблицы.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-128">In this example, the record is simply being copied back to same table.</span></span> <span data-ttu-id="8f6d6-129">Обратите внимание, что все операции блока выполняется в рамках одного последовательность обновления AddNew.</span><span class="sxs-lookup"><span data-stu-id="8f6d6-129">Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
