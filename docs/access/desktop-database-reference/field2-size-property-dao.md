---
title: Свойство Field2.Size (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f1467414729f4ea82bc2779eeb2bd162465b5ccd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292687"
---
# <a name="field2size-property-dao"></a><span data-ttu-id="7db9d-102">Свойство Field2.Size (DAO)</span><span class="sxs-lookup"><span data-stu-id="7db9d-102">Field2.Size property (DAO)</span></span>


<span data-ttu-id="7db9d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7db9d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="7db9d-104">Задает или возвращает значение, которое указывает максимальный размер объекта **Field2** (в bytes).</span><span class="sxs-lookup"><span data-stu-id="7db9d-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db9d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7db9d-105">Syntax</span></span>

<span data-ttu-id="7db9d-106">*выражение .* Размер</span><span class="sxs-lookup"><span data-stu-id="7db9d-106">*expression* .Size</span></span>

<span data-ttu-id="7db9d-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="7db9d-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7db9d-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="7db9d-108">Remarks</span></span>

<span data-ttu-id="7db9d-109">Для объекта, еще не примежаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7db9d-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="7db9d-110">Для полей (кроме полей типа Memo), содержащих данные символов, свойство **Size** указывает максимальное число символов, которые могут содержаться в поле.</span><span class="sxs-lookup"><span data-stu-id="7db9d-110">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold.</span></span> <span data-ttu-id="7db9d-111">Для числовых полей свойство **Size** указывает количество необходимых для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="7db9d-111">For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="7db9d-112">Использование свойства **Size** зависит от объекта, который содержит коллекцию **Fields,** к которой применится объект **Field2,** как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7db9d-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7db9d-113">Объект, к</span><span class="sxs-lookup"><span data-stu-id="7db9d-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="7db9d-114">Использование</span><span class="sxs-lookup"><span data-stu-id="7db9d-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7db9d-115"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="7db9d-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="7db9d-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7db9d-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7db9d-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="7db9d-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="7db9d-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7db9d-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7db9d-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="7db9d-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="7db9d-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7db9d-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7db9d-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="7db9d-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="7db9d-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7db9d-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7db9d-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="7db9d-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="7db9d-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7db9d-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7db9d-125">При создании объекта **Field2** с типом данных, не текстовым, параметр свойства **Type** автоматически определяет параметр свойства **Size;** вам не нужно его устанавливать.</span><span class="sxs-lookup"><span data-stu-id="7db9d-125">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it.</span></span> <span data-ttu-id="7db9d-126">Однако для объекта **Field2** с текстовым типом данных можно установить значение **Size** в виде любого integer до максимального размера текста (255 для баз данных яла базы данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7db9d-126">For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases).</span></span> <span data-ttu-id="7db9d-127">Если размер не установлен, поле будет иметь тот же размер, что и в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7db9d-127">If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="7db9d-128">Для объектов Long Binary и  Memo **Field2** размер всегда имеет 0.</span><span class="sxs-lookup"><span data-stu-id="7db9d-128">For Long Binary and Memo **Field2** objects, **Size** is always set to 0.</span></span> <span data-ttu-id="7db9d-129">Используйте свойство **FieldSize** объекта **Field2,** чтобы определить размер данных в определенной записи.</span><span class="sxs-lookup"><span data-stu-id="7db9d-129">Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record.</span></span> <span data-ttu-id="7db9d-130">Максимальный размер поля Long Binary или Memo ограничивается только системным ресурсом или максимальным размером, допустимым базой данных.</span><span class="sxs-lookup"><span data-stu-id="7db9d-130">The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="7db9d-131">Пример</span><span class="sxs-lookup"><span data-stu-id="7db9d-131">Example</span></span>

<span data-ttu-id="7db9d-132">В этом примере показано свойство **Size** путем нумерации имен и размеров объектов **Field2** в таблице Employees.</span><span class="sxs-lookup"><span data-stu-id="7db9d-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
