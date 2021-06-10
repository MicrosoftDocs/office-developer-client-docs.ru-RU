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
# <a name="field2size-property-dao"></a><span data-ttu-id="80624-102">Свойство Field2.Size (DAO)</span><span class="sxs-lookup"><span data-stu-id="80624-102">Field2.Size property (DAO)</span></span>


<span data-ttu-id="80624-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80624-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="80624-104">Задает или возвращает значение, которое указывает максимальный размер в bytes объекта **Field2.**</span><span class="sxs-lookup"><span data-stu-id="80624-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="80624-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80624-105">Syntax</span></span>

<span data-ttu-id="80624-106">*выражения* . Размер</span><span class="sxs-lookup"><span data-stu-id="80624-106">*expression* .Size</span></span>

<span data-ttu-id="80624-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="80624-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="80624-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="80624-108">Remarks</span></span>

<span data-ttu-id="80624-109">Для объекта, еще не примыкаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство является чтением и написанием.</span><span class="sxs-lookup"><span data-stu-id="80624-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="80624-110">Для полей (кроме полей типа Memo), содержащих данные символов, свойство **Size** указывает максимальное количество символов, которые может содержать поле.</span><span class="sxs-lookup"><span data-stu-id="80624-110">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold.</span></span> <span data-ttu-id="80624-111">Для числовых полей свойство **Size** указывает, сколько запасов хранилища требуется.</span><span class="sxs-lookup"><span data-stu-id="80624-111">For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="80624-112">Использование свойства **Size** зависит от объекта, который содержит коллекцию **Полей,** к которой примыкает объект **Field2,** как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="80624-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80624-113">Объект, приданный</span><span class="sxs-lookup"><span data-stu-id="80624-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="80624-114">Usage</span><span class="sxs-lookup"><span data-stu-id="80624-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80624-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="80624-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="80624-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="80624-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80624-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="80624-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="80624-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80624-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80624-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="80624-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="80624-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80624-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80624-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="80624-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="80624-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="80624-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80624-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="80624-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="80624-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80624-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80624-125">При создании объекта **Field2** с типом данных, не текстовым, параметр **Type** свойством автоматически определяет **параметр Свойства Size;** вам не нужно его устанавливать.</span><span class="sxs-lookup"><span data-stu-id="80624-125">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it.</span></span> <span data-ttu-id="80624-126">Однако для **объекта Field2** с типом текстовых  данных можно установить Размер для любого набора до максимального размера текста (255 для баз данных баз данных базы данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="80624-126">For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases).</span></span> <span data-ttu-id="80624-127">Если размер не установлен, поле будет таким же большим, как позволяет база данных.</span><span class="sxs-lookup"><span data-stu-id="80624-127">If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="80624-128">Для объектов Long Binary и **Memo Field2** **размер** всегда устанавливается до 0.</span><span class="sxs-lookup"><span data-stu-id="80624-128">For Long Binary and Memo **Field2** objects, **Size** is always set to 0.</span></span> <span data-ttu-id="80624-129">Для определения размера данных в определенной записи используйте свойство **FieldSize** объекта **Field2.**</span><span class="sxs-lookup"><span data-stu-id="80624-129">Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record.</span></span> <span data-ttu-id="80624-130">Максимальный размер поля Long Binary или Memo ограничен только ресурсами системы или максимальным размером, который позволяет база данных.</span><span class="sxs-lookup"><span data-stu-id="80624-130">The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="80624-131">Пример</span><span class="sxs-lookup"><span data-stu-id="80624-131">Example</span></span>

<span data-ttu-id="80624-132">В этом примере демонстрируется свойство **Size** путем переумерия имен и размеров объектов **Field2** в таблице Employees.</span><span class="sxs-lookup"><span data-stu-id="80624-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

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
