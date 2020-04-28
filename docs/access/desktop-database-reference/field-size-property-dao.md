---
title: Свойство Field.Size (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 16ce8a9e63c18ded2738035f23e9a1baeff4cc8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293018"
---
# <a name="fieldsize-property-dao"></a><span data-ttu-id="e9bd2-102">Свойство Field.Size (DAO)</span><span class="sxs-lookup"><span data-stu-id="e9bd2-102">Field.Size property (DAO)</span></span>


<span data-ttu-id="e9bd2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9bd2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e9bd2-104">Задает или возвращает значение, которое указывает максимальный размер объекта **[field](field-object-dao.md)** в байтах.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-104">Sets or returns a value that indicates the maximum size, in bytes, of a **[Field](field-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9bd2-105">Syntax</span></span>

<span data-ttu-id="e9bd2-106">*Expression* . Размер</span><span class="sxs-lookup"><span data-stu-id="e9bd2-106">*expression* .Size</span></span>

<span data-ttu-id="e9bd2-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9bd2-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9bd2-108">Remarks</span></span>

<span data-ttu-id="e9bd2-109">Для объекта, который еще не добавлен в коллекцию **[Fields](fields-collection-dao.md)** , это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="e9bd2-110">Для полей (отличных от полей типа MEMO), содержащих символьные данные, свойство **size** указывает максимальное число знаков, которое может содержать поле.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-110">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold.</span></span> <span data-ttu-id="e9bd2-111">Для числовых полей свойство **size** указывает, сколько байтов хранения необходимо.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-111">For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="e9bd2-112">Использование свойства **size** зависит от объекта, содержащего коллекцию **Fields** , к которой добавляется объект **field** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9bd2-113">Объект, добавленный в</span><span class="sxs-lookup"><span data-stu-id="e9bd2-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="e9bd2-114">Применение</span><span class="sxs-lookup"><span data-stu-id="e9bd2-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9bd2-115"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="e9bd2-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="e9bd2-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e9bd2-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9bd2-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="e9bd2-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e9bd2-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9bd2-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9bd2-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="e9bd2-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="e9bd2-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9bd2-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9bd2-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="e9bd2-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="e9bd2-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e9bd2-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9bd2-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="e9bd2-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e9bd2-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9bd2-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e9bd2-125">При создании объекта **field** с типом данных, отличным от Text, параметр свойства **[Type](field-type-property-dao.md)** автоматически определяет значение свойства **size** ; задавать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-125">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it.</span></span> <span data-ttu-id="e9bd2-126">Однако для объекта **field** с типом данных text **можно задать любое** целое число вплоть до максимального размера текста (255 для баз данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e9bd2-126">For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases).</span></span> <span data-ttu-id="e9bd2-127">Если размер не задан, размер поля будет максимально велик для базы данных.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-127">If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="e9bd2-128">Для больших двоичных объектов и **полей** MEMO **Размер** всегда устанавливается равным 0.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-128">For Long Binary and Memo **Field** objects, **Size** is always set to 0.</span></span> <span data-ttu-id="e9bd2-129">Используйте свойство **[FieldSize](field-fieldsize-property-dao.md)** объекта **field** , чтобы определить размер данных в определенной записи.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-129">Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record.</span></span> <span data-ttu-id="e9bd2-130">Максимальный размер длинного двоичного поля или поля MEMO ограничен только системными ресурсами или максимальным размером, разрешенным в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-130">The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="e9bd2-131">Пример</span><span class="sxs-lookup"><span data-stu-id="e9bd2-131">Example</span></span>

<span data-ttu-id="e9bd2-132">В этом примере показано свойство **size** , которое перечисляет имена и размеры объектов **field** в таблице Employees (сотрудники).</span><span class="sxs-lookup"><span data-stu-id="e9bd2-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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
