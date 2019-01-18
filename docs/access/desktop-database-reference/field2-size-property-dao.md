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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699039"
---
# <a name="field2size-property-dao"></a><span data-ttu-id="22102-102">Свойство Field2.Size (DAO)</span><span class="sxs-lookup"><span data-stu-id="22102-102">Field2.Size property (DAO)</span></span>


<span data-ttu-id="22102-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22102-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="22102-104">Задает или возвращает значение, которое указывает максимальный размер в байтах, **поле2** объекта.</span><span class="sxs-lookup"><span data-stu-id="22102-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="22102-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22102-105">Syntax</span></span>

<span data-ttu-id="22102-106">*выражение* . Размер</span><span class="sxs-lookup"><span data-stu-id="22102-106">*expression* .Size</span></span>

<span data-ttu-id="22102-107">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="22102-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="22102-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="22102-108">Remarks</span></span>

<span data-ttu-id="22102-109">Для объекта еще не добавляется в конец коллекции **[полей](fields-collection-dao.md)** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="22102-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="22102-110">Для полей (кроме полей типа Memo), которые содержат символ данных свойство **Size** указывает максимальное число символов, которое может содержать поля.</span><span class="sxs-lookup"><span data-stu-id="22102-110">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold.</span></span> <span data-ttu-id="22102-111">Для числовых полей свойство **Size** указывает число байтов хранилища являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="22102-111">For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="22102-112">Использование **свойства Size** зависит от объекта, который содержит коллекцию **полей** , к которому добавляется объект **поле2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="22102-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22102-113">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="22102-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="22102-114">Применение</span><span class="sxs-lookup"><span data-stu-id="22102-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22102-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="22102-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="22102-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="22102-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22102-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="22102-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="22102-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="22102-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22102-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="22102-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="22102-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="22102-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22102-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="22102-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="22102-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="22102-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22102-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="22102-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="22102-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="22102-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22102-125">При создании объекта **поле2** с типом данных, отличный от текста, значение свойства **типа** автоматически определяет значение свойства **размера** ; его настройка не требуется.</span><span class="sxs-lookup"><span data-stu-id="22102-125">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it.</span></span> <span data-ttu-id="22102-126">Для объекта **поле2** с типом данных Text тем не менее, можно задать **размер** любое целое число до текст максимальный размер (255 для базами данных, ядро базы данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="22102-126">For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases).</span></span> <span data-ttu-id="22102-127">Если размер не установлен, это поле будет размер базы данных позволяет.</span><span class="sxs-lookup"><span data-stu-id="22102-127">If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="22102-128">Объектам-Long Binary и Memo **поле2** **размер** всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="22102-128">For Long Binary and Memo **Field2** objects, **Size** is always set to 0.</span></span> <span data-ttu-id="22102-129">Используйте свойство **основании итогового** объекта **поле2** порядок определения размера данных в конкретной записи.</span><span class="sxs-lookup"><span data-stu-id="22102-129">Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record.</span></span> <span data-ttu-id="22102-130">Максимальный размер поля Long Binary или Memo ограничивается только системных ресурсов или максимальный размер, который позволяет базы данных.</span><span class="sxs-lookup"><span data-stu-id="22102-130">The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="22102-131">Пример</span><span class="sxs-lookup"><span data-stu-id="22102-131">Example</span></span>

<span data-ttu-id="22102-132">В этом примере демонстрируется свойство **размер** перечисление имена и размеры объектов **поле2** в таблице сотрудников.</span><span class="sxs-lookup"><span data-stu-id="22102-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

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
