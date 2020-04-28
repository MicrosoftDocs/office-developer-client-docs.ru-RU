---
title: Свойство relation. Table (DAO)
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
# <a name="relationtable-property-dao"></a><span data-ttu-id="9d3d8-102">Свойство relation. Table (DAO)</span><span class="sxs-lookup"><span data-stu-id="9d3d8-102">Relation.Table property (DAO)</span></span>


<span data-ttu-id="9d3d8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d3d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d3d8-104">Указывает имя основной таблицы объекта **[связи](relation-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="9d3d8-104">Indicates the name of a **[Relation](relation-object-dao.md)** object's primary table.</span></span> <span data-ttu-id="9d3d8-105">Это значение должно совпадать с параметром свойства **[Name](connection-name-property-dao.md)** объекта **[tabledef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9d3d8-105">This should be equal to the **[Name](connection-name-property-dao.md)** property setting of a **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3d8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d3d8-106">Syntax</span></span>

<span data-ttu-id="9d3d8-107">*Expression* . Приведен</span><span class="sxs-lookup"><span data-stu-id="9d3d8-107">*expression* .Table</span></span>

<span data-ttu-id="9d3d8-108">*Expression (выражение* ) Переменная, представляющая объект **связи** .</span><span class="sxs-lookup"><span data-stu-id="9d3d8-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d3d8-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d3d8-109">Remarks</span></span>

<span data-ttu-id="9d3d8-110">Параметр свойства **Table** доступен для чтения и записи для нового объекта **relation** , который еще не добавлен в коллекцию и доступен только для чтения для существующего объекта **relation** в коллекции **[связей](relations-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="9d3d8-110">The **Table** property setting is read/write for a new **Relation** object not yet appended to a collection and read-only for an existing **Relation** object in a **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="9d3d8-111">Используйте свойство **Table** со свойством **[ForeignTable](relation-foreigntable-property-dao.md)** , чтобы определить объект **связи** , который представляет связь между полями в двух таблицах или запросах.</span><span class="sxs-lookup"><span data-stu-id="9d3d8-111">Use the **Table** property with the **[ForeignTable](relation-foreigntable-property-dao.md)** property to define a **Relation** object, which represents the relationship between fields in two tables or queries.</span></span> <span data-ttu-id="9d3d8-112">Присвойте свойству **Table** значение свойства " **имя** " основного объекта **tabledef** или **QueryDef** и присвойте свойству **ForeignTable** значение свойства " **имя** " внешнего объекта (ссылки) **tabledef** или **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="9d3d8-112">Set the **Table** property to the **Name** property setting of the primary **TableDef** or **QueryDef** object, and set the **ForeignTable** property to the **Name** property setting of the foreign (referencing) **TableDef** or **QueryDef** object.</span></span> <span data-ttu-id="9d3d8-113">Свойство **[Attributes](field-attributes-property-dao.md)** определяет тип связи между двумя объектами.</span><span class="sxs-lookup"><span data-stu-id="9d3d8-113">The **[Attributes](field-attributes-property-dao.md)** property determines the type of relationship between the two objects.</span></span>

<span data-ttu-id="9d3d8-114">Например, если у вас есть список допустимых кодов частей (в поле с именем Партно), хранящихся в таблице Валидпартс, можно установить связь "один ко многим" с таблицей Ордеритем, в случае если код части был введен в таблицу Ордеритем, он должен быть уже включен в таблицу Валидпартс.</span><span class="sxs-lookup"><span data-stu-id="9d3d8-114">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table.</span></span> <span data-ttu-id="9d3d8-115">Если код части не существовал в таблице Валидпартс и не присвоено свойству **Attributes** объекта **relation** значение **дбрелатиондонтенфорце**, возникнет Перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="9d3d8-115">If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="9d3d8-116">В этом случае таблица Валидпартс является основной таблицей, поэтому свойству **Table** объекта **relation** будет присвоено значение валидпартс, а свойству **ForeignTable** объекта **relation** будет присвоено значение ордеритем.</span><span class="sxs-lookup"><span data-stu-id="9d3d8-116">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="9d3d8-117">Свойства **Name** и **фореигннаме** объекта **[field](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** объекта **relation** задаются как партно.</span><span class="sxs-lookup"><span data-stu-id="9d3d8-117">The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="9d3d8-118">Пример</span><span class="sxs-lookup"><span data-stu-id="9d3d8-118">Example</span></span>

<span data-ttu-id="9d3d8-119">В этом примере показано, как свойства **Table**, **ForeignTable**и **фореигннаме** определяют условия **связи** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="9d3d8-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
