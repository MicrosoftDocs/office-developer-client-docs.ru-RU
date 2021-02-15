---
title: Свойство Relation.Table (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 91a3262d92350618c2385013983020669b28ea5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306995"
---
# <a name="relationtable-property-dao"></a><span data-ttu-id="a0000-102">Свойство Relation.Table (DAO)</span><span class="sxs-lookup"><span data-stu-id="a0000-102">Relation.Table property (DAO)</span></span>


<span data-ttu-id="a0000-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0000-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0000-104">Указывает имя основной таблицы объекта **[Relation.](relation-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="a0000-104">Indicates the name of a **[Relation](relation-object-dao.md)** object's primary table.</span></span> <span data-ttu-id="a0000-105">Это должно быть равно параметру **[свойства Name](connection-name-property-dao.md)** объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a0000-105">This should be equal to the **[Name](connection-name-property-dao.md)** property setting of a **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0000-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0000-106">Syntax</span></span>

<span data-ttu-id="a0000-107">*выражение .* Таблица</span><span class="sxs-lookup"><span data-stu-id="a0000-107">*expression* .Table</span></span>

<span data-ttu-id="a0000-108">*выражение* Переменная, представляюная объект **Relation.**</span><span class="sxs-lookup"><span data-stu-id="a0000-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0000-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="a0000-109">Remarks</span></span>

<span data-ttu-id="a0000-110">Параметр **свойства Table** для нового объекта **Relation** еще не был сдан в коллекцию и доступно только для чтения для существующего объекта **Relation** в коллекции **[Relations.](relations-collection-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="a0000-110">The **Table** property setting is read/write for a new **Relation** object not yet appended to a collection and read-only for an existing **Relation** object in a **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="a0000-111">Используйте свойство **Table** со **[свойством ForeignTable](relation-foreigntable-property-dao.md)** для определения объекта **Relation,** который представляет отношение между полями в двух таблицах или запросах.</span><span class="sxs-lookup"><span data-stu-id="a0000-111">Use the **Table** property with the **[ForeignTable](relation-foreigntable-property-dao.md)** property to define a **Relation** object, which represents the relationship between fields in two tables or queries.</span></span> <span data-ttu-id="a0000-112">Установите для свойства **Table** параметр свойства **Name** основного объекта **TableDef** или **QueryDef** и задайте для свойства **ForeignTable** параметр свойства **Name** внешнего (ссылаясь) **объекта TableDef** или **QueryDef.**</span><span class="sxs-lookup"><span data-stu-id="a0000-112">Set the **Table** property to the **Name** property setting of the primary **TableDef** or **QueryDef** object, and set the **ForeignTable** property to the **Name** property setting of the foreign (referencing) **TableDef** or **QueryDef** object.</span></span> <span data-ttu-id="a0000-113">Свойство **[Attributes](field-attributes-property-dao.md)** определяет тип связи между двумя объектами.</span><span class="sxs-lookup"><span data-stu-id="a0000-113">The **[Attributes](field-attributes-property-dao.md)** property determines the type of relationship between the two objects.</span></span>

<span data-ttu-id="a0000-114">Например, если у вас есть список действительных кодов части (в поле с именем PartNo), хранимый в таблице ValidParts, можно установить отношение "один к многим" с таблицей OrderItem таким образом, что если код части был введен в таблицу OrderItem, он должен уже быть в таблице ValidParts.</span><span class="sxs-lookup"><span data-stu-id="a0000-114">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table.</span></span> <span data-ttu-id="a0000-115">Если код части не существует в таблице ValidParts и вы не установили для свойства **Attributes** объекта **Relation** значение **dbRelationDontEnforce,** произойдет перехватимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="a0000-115">If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="a0000-116">В этом случае таблица ValidParts является основной, поэтому свойству **Table** объекта **Relation** будет задано свойство ValidParts, а свойству **ForeignTable** объекта **Relation** — OrderItem.</span><span class="sxs-lookup"><span data-stu-id="a0000-116">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="a0000-117">Свойства **Name** и **ForeignName** объекта **[Field](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** объекта **Relation** будут иметь имя PartNo.</span><span class="sxs-lookup"><span data-stu-id="a0000-117">The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="a0000-118">Пример</span><span class="sxs-lookup"><span data-stu-id="a0000-118">Example</span></span>

<span data-ttu-id="a0000-119">В этом примере показано, как свойства **Table,** **ForeignTable** и **ForeignName** определяют термины **отношения** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="a0000-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

```vb
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
