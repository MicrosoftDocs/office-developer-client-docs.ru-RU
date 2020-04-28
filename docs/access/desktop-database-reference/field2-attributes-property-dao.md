---
title: Свойство field2. Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a655cfa5c6f0427b1a26a01f01e991564ab8e387
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292890"
---
# <a name="field2attributes-property-dao"></a><span data-ttu-id="be473-102">Свойство field2. Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="be473-102">Field2.Attributes property (DAO)</span></span>


<span data-ttu-id="be473-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be473-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="be473-104">Задает или возвращает значение, которое указывает одну или несколько характеристик объекта **field2** .</span><span class="sxs-lookup"><span data-stu-id="be473-104">Sets or returns a value that indicates one or more characteristics of a **Field2** object.</span></span> <span data-ttu-id="be473-105">Для чтения и записи, **Long**.</span><span class="sxs-lookup"><span data-stu-id="be473-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="be473-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be473-106">Syntax</span></span>

<span data-ttu-id="be473-107">*expression* .Attributes</span><span class="sxs-lookup"><span data-stu-id="be473-107">*expression* .Attributes</span></span>

<span data-ttu-id="be473-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="be473-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="be473-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="be473-109">Remarks</span></span>

<span data-ttu-id="be473-110">Значение указывает характеристики поля, представленного объектом **field2** , и может быть сочетанием этих констант.</span><span class="sxs-lookup"><span data-stu-id="be473-110">The value specifies characteristics of the field represented by the **Field2** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be473-111">Константа</span><span class="sxs-lookup"><span data-stu-id="be473-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="be473-112">Описание</span><span class="sxs-lookup"><span data-stu-id="be473-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be473-113"><strong>dbAutoIncrField</strong></span><span class="sxs-lookup"><span data-stu-id="be473-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="be473-114">Значение поля для новых записей автоматически увеличивается на уникальные длинное целочисленное значение, которое нельзя изменить (в рабочей области Microsoft Access, поддерживается только для таблиц базы данных ядра СУБД Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="be473-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be473-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="be473-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="be473-116">Поле сортируется в порядке убывания (от я до A или 100 до 0); Этот параметр применяется только к объекту <strong>field2</strong> в коллекции <strong>Fields</strong> объекта <strong>index</strong> .</span><span class="sxs-lookup"><span data-stu-id="be473-116">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field2</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object.</span></span> <span data-ttu-id="be473-117">Если опустить эту константу, поле сортируется в порядке возрастания (от А до Я или от 0 до 100).</span><span class="sxs-lookup"><span data-stu-id="be473-117">If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order.</span></span> <span data-ttu-id="be473-118">Это значение по умолчанию для полей <strong>Index</strong> и <strong>TableDef</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="be473-118">This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be473-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="be473-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="be473-120">Размер поля закреплен (по умолчанию для числовых полей).</span><span class="sxs-lookup"><span data-stu-id="be473-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be473-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="be473-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="be473-122">Поле содержит сведения о гиперссылке (только для полей Memo).</span><span class="sxs-lookup"><span data-stu-id="be473-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be473-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="be473-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="be473-124">В поле хранятся сведения о репликации для реплик; Вы не можете удалить этот тип поля (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="be473-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be473-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="be473-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="be473-126">Можно изменить значение данного поля.</span><span class="sxs-lookup"><span data-stu-id="be473-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be473-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="be473-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="be473-128">Переменный размер поля (только для текстовых полей).</span><span class="sxs-lookup"><span data-stu-id="be473-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be473-129">Для объекта, который еще не добавлен в коллекцию, это свойство предназначено для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="be473-129">For an object not yet appended to a collection, this property is read/write.</span></span> <span data-ttu-id="be473-130">Для добавленного объекта **field2** доступность свойства **Attributes** зависит от объекта, содержащего коллекцию **Fields** .</span><span class="sxs-lookup"><span data-stu-id="be473-130">For an appended **Field2** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be473-131">Если объект Field принадлежит к</span><span class="sxs-lookup"><span data-stu-id="be473-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="be473-132">тогда атрибуты будут</span><span class="sxs-lookup"><span data-stu-id="be473-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be473-133">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="be473-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="be473-134">Чтение и запись до того момента, пока объект <strong>TableDef</strong>, который добавляется к объекту <strong>Index</strong>, добавляется к объекту <strong>Database</strong>; после чего свойство будет доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="be473-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be473-135">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="be473-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="be473-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="be473-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be473-137">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="be473-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="be473-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="be473-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be473-139">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="be473-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="be473-140">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="be473-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be473-141">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="be473-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="be473-142">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be473-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be473-143">Если вы задаете несколько атрибутов, их можно объединить, суммируя соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="be473-143">When you set multiple attributes, you can combine them by summing the appropriate constants.</span></span> <span data-ttu-id="be473-144">Любые недопустимые значения игнорируются без сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="be473-144">Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="be473-145">Пример</span><span class="sxs-lookup"><span data-stu-id="be473-145">Example</span></span>

<span data-ttu-id="be473-146">В этом примере показано, как отобразить свойство **Attributes** для объектов **field2**, **relation**и **tabledef** в базе данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="be473-146">This example displays the **Attributes** property for **Field2**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

