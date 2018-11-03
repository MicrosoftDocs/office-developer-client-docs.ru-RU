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
ms.openlocfilehash: dd6f1ef3ea1d955f3b17d4cafb7e521c54191d27
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929582"
---
# <a name="relationtable-property-dao"></a><span data-ttu-id="24816-102">Свойство Relation.Table (DAO)</span><span class="sxs-lookup"><span data-stu-id="24816-102">Relation.Table property (DAO)</span></span>


<span data-ttu-id="24816-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24816-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24816-104">Указывает имя таблицы основной объект **[связи](relation-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="24816-104">Indicates the name of a **[Relation](relation-object-dao.md)** object's primary table.</span></span> <span data-ttu-id="24816-105">Это должен быть равен **[свойства Name объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** (только для рабочих областей Microsoft Access)](connection-name-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="24816-105">This should be equal to the **[Name](connection-name-property-dao.md)** property setting of a **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="24816-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24816-106">Syntax</span></span>

<span data-ttu-id="24816-107">*выражение* . В таблице</span><span class="sxs-lookup"><span data-stu-id="24816-107">*expression* .Table</span></span>

<span data-ttu-id="24816-108">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="24816-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24816-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="24816-109">Remarks</span></span>

<span data-ttu-id="24816-110">Значение свойства **в таблице** — чтение и запись для нового объекта **отношения** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **отношения** в коллекции **[отношений](relations-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="24816-110">The **Table** property setting is read/write for a new **Relation** object not yet appended to a collection and read-only for an existing **Relation** object in a **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="24816-111">Свойство **таблицы** с помощью свойства **[таблицавнешнегоключа](relation-foreigntable-property-dao.md)** используется для определения объект **отношения** , представляющий отношение между полями в двух таблиц или запросов.</span><span class="sxs-lookup"><span data-stu-id="24816-111">Use the **Table** property with the **[ForeignTable](relation-foreigntable-property-dao.md)** property to define a **Relation** object, which represents the relationship between fields in two tables or queries.</span></span> <span data-ttu-id="24816-112">Свойство **таблицы** значение \*\*свойства Name объекта основной **TableDef** или **QueryDef** \*\* и присвойте свойству **таблицавнешнегоключа** значение \*\*свойства Name внешнего (ссылающегося) \*\*TableDef \*\*\*\* или объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="24816-112">Set the **Table** property to the **Name** property setting of the primary **TableDef** or **QueryDef** object, and set the **ForeignTable** property to the **Name** property setting of the foreign (referencing) **TableDef** or **QueryDef** object.</span></span> <span data-ttu-id="24816-113">Свойство **[Attributes](field-attributes-property-dao.md)** определяет тип отношения между двумя объектами.</span><span class="sxs-lookup"><span data-stu-id="24816-113">The **[Attributes](field-attributes-property-dao.md)** property determines the type of relationship between the two objects.</span></span>

<span data-ttu-id="24816-114">Например, если у вас есть список кодов допустимый части (в поле с именем PartNo) хранятся в таблице ValidParts может установить отношение один ко многим с таблицей OrderItem таким образом, если часть кода были введены в таблицу OrderItem, его придется уже быть в их ввода Таблица ValidParts e.</span><span class="sxs-lookup"><span data-stu-id="24816-114">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table.</span></span> <span data-ttu-id="24816-115">Если часть кода не был найден в таблице ValidParts и не было задано свойство **атрибуты** объекта **отношения** к **dbRelationDontEnforce**, возникнет перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="24816-115">If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="24816-116">В этом случае в таблице ValidParts представляет основной таблицы, поэтому устанавливается свойство **таблицы** объект **отношения** в ValidParts и свойство **таблицавнешнегоключа** объект **связи** будет иметь значение OrderItem.</span><span class="sxs-lookup"><span data-stu-id="24816-116">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="24816-117">Свойства **Name** и **ForeignName** объекта **[поля](field-object-dao.md)** в коллекции **[полей](fields-collection-dao.md)** объект **связи** будет иметь значение PartNo.</span><span class="sxs-lookup"><span data-stu-id="24816-117">The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="24816-118">Пример</span><span class="sxs-lookup"><span data-stu-id="24816-118">Example</span></span>

<span data-ttu-id="24816-119">В этом примере показано, как определить свойства **в таблице**, **таблицавнешнегоключа**и **ForeignName** условия **отношения** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="24816-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
