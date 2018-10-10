---
title: Field2.Attributes Property (DAO)
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
ms.openlocfilehash: 6742e8b97e3444df38a7c52d048aaa6a2f023cb0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482536"
---
# <a name="field2attributes-property-dao"></a><span data-ttu-id="12012-102">Field2.Attributes Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="12012-102">Field2.Attributes Property (DAO)</span></span>


<span data-ttu-id="12012-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="12012-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="12012-104">Задает или возвращает значение, указывающее, один или несколько характеристик объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="12012-104">Sets or returns a value that indicates one or more characteristics of a **Field2** object.</span></span> <span data-ttu-id="12012-105">Чтение и запись **времени**.</span><span class="sxs-lookup"><span data-stu-id="12012-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="12012-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12012-106">Syntax</span></span>

<span data-ttu-id="12012-107">*выражение* . Атрибуты</span><span class="sxs-lookup"><span data-stu-id="12012-107">*expression* .Attributes</span></span>

<span data-ttu-id="12012-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="12012-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="12012-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="12012-109">Remarks</span></span>

<span data-ttu-id="12012-110">Значение указывает характеристики поля, представленного объектом **поле2** и может быть комбинацией этих констант.</span><span class="sxs-lookup"><span data-stu-id="12012-110">The value specifies characteristics of the field represented by the **Field2** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12012-111">Константа</span><span class="sxs-lookup"><span data-stu-id="12012-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="12012-112">Описание</span><span class="sxs-lookup"><span data-stu-id="12012-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12012-113"><strong>dbAutoIncrField</strong></span><span class="sxs-lookup"><span data-stu-id="12012-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="12012-114">Значение поля для добавления новых записей автоматически увеличивается уникальный длинное целое число, которое нельзя изменить (в рабочую область Microsoft Access поддерживается только для таблиц базы данных ядра базы данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="12012-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12012-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="12012-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="12012-116">Поле по убыванию (от я до А или 100 до 0); Этот параметр применяется только к объекта <strong>поле2</strong> в коллекции <strong>полей</strong> объекта <strong>индекса</strong> .</span><span class="sxs-lookup"><span data-stu-id="12012-116">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field2</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object.</span></span> <span data-ttu-id="12012-117">Если опустить этой константы поле сортироваться в восходящем (A-Z или 0 до 100) порядке.</span><span class="sxs-lookup"><span data-stu-id="12012-117">If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order.</span></span> <span data-ttu-id="12012-118">Это значение по умолчанию для <strong>индексирования</strong> и <strong>TableDef</strong> полей (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="12012-118">This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12012-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="12012-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="12012-120">Размер поля имеет фиксированную (по умолчанию для числовых полей).</span><span class="sxs-lookup"><span data-stu-id="12012-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12012-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="12012-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="12012-122">Поле содержит сведения о гиперссылках (только для полей Memo).</span><span class="sxs-lookup"><span data-stu-id="12012-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12012-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="12012-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="12012-124">В поле хранится репликации сведения о репликах; не удается удалить этот тип поля (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="12012-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12012-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="12012-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="12012-126">Можно изменить значение поля.</span><span class="sxs-lookup"><span data-stu-id="12012-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12012-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="12012-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="12012-128">Размер поля — переменная (только для текстовых полей).</span><span class="sxs-lookup"><span data-stu-id="12012-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="12012-129">Для объекта еще не добавляется в конец коллекции это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="12012-129">For an object not yet appended to a collection, this property is read/write.</span></span> <span data-ttu-id="12012-130">Для объекта присоединенных **поле2** доступности свойство **Attributes** зависит от объекта, который содержит коллекцию **полей** .</span><span class="sxs-lookup"><span data-stu-id="12012-130">For an appended **Field2** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12012-131">Если принадлежит объект поля</span><span class="sxs-lookup"><span data-stu-id="12012-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="12012-132">Атрибуты — это</span><span class="sxs-lookup"><span data-stu-id="12012-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12012-133">Объект <strong>индекса</strong></span><span class="sxs-lookup"><span data-stu-id="12012-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="12012-134">Чтение и запись, пока не используется в качестве объекта <strong>TableDef</strong> , добавляемый в объект <strong>индекса</strong> для объекта <strong>базы данных</strong> ; Выберите свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="12012-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12012-135">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="12012-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="12012-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="12012-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12012-137">Объект <strong>набора записей</strong></span><span class="sxs-lookup"><span data-stu-id="12012-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="12012-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="12012-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12012-139"><strong>Отношения</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="12012-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="12012-140">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="12012-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12012-141">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="12012-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="12012-142">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="12012-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="12012-143">Если задано несколько атрибутов, их можно объединить суммируются соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="12012-143">When you set multiple attributes, you can combine them by summing the appropriate constants.</span></span> <span data-ttu-id="12012-144">Недопустимые значения, пропускаются без создания ошибку.</span><span class="sxs-lookup"><span data-stu-id="12012-144">Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="12012-145">Пример</span><span class="sxs-lookup"><span data-stu-id="12012-145">Example</span></span>

<span data-ttu-id="12012-146">В этом примере отображаются свойства **атрибуты** для объектов **поле2**, **связь**и **TableDef** базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="12012-146">This example displays the **Attributes** property for **Field2**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

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

