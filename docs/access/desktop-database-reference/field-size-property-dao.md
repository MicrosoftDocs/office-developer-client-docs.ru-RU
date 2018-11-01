---
title: Field.Size Property (DAO)
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
ms.openlocfilehash: 53a76c26bca9d36b853c7aa6b0620788389cb765
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886489"
---
# <a name="fieldsize-property-dao"></a><span data-ttu-id="f0f3f-102">Field.Size Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f0f3f-102">Field.Size Property (DAO)</span></span>


<span data-ttu-id="f0f3f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0f3f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f0f3f-104">Задает или возвращает значение, которое указывает максимальный размер в байтах, объект **[поля](field-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="f0f3f-104">Sets or returns a value that indicates the maximum size, in bytes, of a **[Field](field-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f3f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0f3f-105">Syntax</span></span>

<span data-ttu-id="f0f3f-106">*выражение* . Размер</span><span class="sxs-lookup"><span data-stu-id="f0f3f-106">*expression* .Size</span></span>

<span data-ttu-id="f0f3f-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="f0f3f-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0f3f-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="f0f3f-108">Remarks</span></span>

<span data-ttu-id="f0f3f-109">Для объекта еще не добавляется в конец коллекции **[полей](fields-collection-dao.md)** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="f0f3f-110">Для полей (кроме полей типа Memo), которые содержат символ данных свойство **Size** указывает максимальное число символов, которое может содержать поля.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-110">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold.</span></span> <span data-ttu-id="f0f3f-111">Для числовых полей свойство **Size** указывает число байтов хранилища являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-111">For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="f0f3f-112">Использование **свойства Size** зависит от объекта, которое содержит коллекцию **полей** , к которому добавляется объект **поля** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0f3f-113">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="f0f3f-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="f0f3f-114">Применение</span><span class="sxs-lookup"><span data-stu-id="f0f3f-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0f3f-115"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="f0f3f-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f3f-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0f3f-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f3f-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="f0f3f-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f3f-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0f3f-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f3f-119"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="f0f3f-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f3f-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0f3f-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f3f-121"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="f0f3f-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f3f-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0f3f-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f3f-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="f0f3f-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f3f-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0f3f-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f0f3f-125">При создании объекта **поля** с типом данных, отличный от текста, значение свойства **[типа](field-type-property-dao.md)** автоматически определяет значение свойства **размера** ; его настройка не требуется.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-125">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it.</span></span> <span data-ttu-id="f0f3f-126">Для объекта **поля** с типом данных Text тем не менее, можно задать **размер** любое целое число до текст максимальный размер (255 для баз данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f0f3f-126">For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases).</span></span> <span data-ttu-id="f0f3f-127">Если размер не установлен, это поле будет размер базы данных позволяет.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-127">If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="f0f3f-128">Объектам-Long Binary и Memo **поля** **размер** всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-128">For Long Binary and Memo **Field** objects, **Size** is always set to 0.</span></span> <span data-ttu-id="f0f3f-129">Свойство **[основании итогового](field-fieldsize-property-dao.md)** объекта **поля** для определения размера данных в конкретной записи.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-129">Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record.</span></span> <span data-ttu-id="f0f3f-130">Максимальный размер поля Long Binary или Memo ограничивается только системных ресурсов или максимальный размер, который позволяет базы данных.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-130">The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="f0f3f-131">Пример</span><span class="sxs-lookup"><span data-stu-id="f0f3f-131">Example</span></span>

<span data-ttu-id="f0f3f-132">В этом примере демонстрируется свойство **размер** перечисление имена и размеры объектов **поля** в таблице сотрудников.</span><span class="sxs-lookup"><span data-stu-id="f0f3f-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span></span>

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
