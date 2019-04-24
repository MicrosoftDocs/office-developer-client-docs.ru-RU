---
title: Свойство field2. size (DAO)
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
# <a name="field2size-property-dao"></a><span data-ttu-id="946a5-102">Свойство field2. size (DAO)</span><span class="sxs-lookup"><span data-stu-id="946a5-102">Field2.Size property (DAO)</span></span>


<span data-ttu-id="946a5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="946a5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="946a5-104">Задает или возвращает значение, которое указывает максимальный размер объекта **field2** в байтах.</span><span class="sxs-lookup"><span data-stu-id="946a5-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="946a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="946a5-105">Syntax</span></span>

<span data-ttu-id="946a5-106">*Expression* . Размер</span><span class="sxs-lookup"><span data-stu-id="946a5-106">*expression* .Size</span></span>

<span data-ttu-id="946a5-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="946a5-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="946a5-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="946a5-108">Remarks</span></span>

<span data-ttu-id="946a5-109">Для объекта, который еще не добавлен в коллекцию **[Fields](fields-collection-dao.md)** , это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="946a5-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="946a5-110">Для полей (отличных от полей типа MEMO), содержащих символьные данные, свойство **size** указывает максимальное число знаков, которое может содержать поле.</span><span class="sxs-lookup"><span data-stu-id="946a5-110">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold.</span></span> <span data-ttu-id="946a5-111">Для числовых полей свойство **size** указывает, сколько байтов хранения необходимо.</span><span class="sxs-lookup"><span data-stu-id="946a5-111">For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="946a5-112">Использование свойства **size** зависит от объекта, содержащего коллекцию Fields, \*\*\*\* к которой добавляется объект **field2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="946a5-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="946a5-113">Объект, добавленный в</span><span class="sxs-lookup"><span data-stu-id="946a5-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="946a5-114">Использование</span><span class="sxs-lookup"><span data-stu-id="946a5-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="946a5-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="946a5-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="946a5-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="946a5-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946a5-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="946a5-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="946a5-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="946a5-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="946a5-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="946a5-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="946a5-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="946a5-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946a5-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="946a5-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="946a5-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="946a5-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="946a5-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="946a5-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="946a5-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="946a5-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="946a5-125">При создании объекта **field2** с типом данных, отличным от Text, параметр свойства **Type** автоматически определяет значение свойства **size** ; задавать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="946a5-125">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it.</span></span> <span data-ttu-id="946a5-126">Однако для объекта **field2** с типом данных Text можно задать любое целое число вплоть до максимального размера текста (255 для баз данных ядра СУБД Microsoft Access). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="946a5-126">For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases).</span></span> <span data-ttu-id="946a5-127">Если размер не задан, размер поля будет максимально велик для базы данных.</span><span class="sxs-lookup"><span data-stu-id="946a5-127">If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="946a5-128">Для больших двоичных объектов и полей MEMO **field2** **Размер** всегда равен 0.</span><span class="sxs-lookup"><span data-stu-id="946a5-128">For Long Binary and Memo **Field2** objects, **Size** is always set to 0.</span></span> <span data-ttu-id="946a5-129">Используйте свойство **FieldSize** объекта **field2** , чтобы определить размер данных в определенной записи.</span><span class="sxs-lookup"><span data-stu-id="946a5-129">Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record.</span></span> <span data-ttu-id="946a5-130">Максимальный размер длинного двоичного поля или поля MEMO ограничен только системными ресурсами или максимальным размером, разрешенным в базе данных.</span><span class="sxs-lookup"><span data-stu-id="946a5-130">The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="946a5-131">Пример</span><span class="sxs-lookup"><span data-stu-id="946a5-131">Example</span></span>

<span data-ttu-id="946a5-132">В этом примере показано свойство **size** , которое перечисляет имена и размеры объектов **field2** в таблице Employees.</span><span class="sxs-lookup"><span data-stu-id="946a5-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

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
