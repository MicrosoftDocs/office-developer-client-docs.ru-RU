---
title: Свойство Relation.ForeignTable (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fc7ee9b5bc832cc2a125024c592db2c7b13e72f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307049"
---
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="16f56-102">Свойство Relation.ForeignTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="16f56-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="16f56-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16f56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16f56-104">Задает или возвращает имя иностранной таблицы в связи (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="16f56-104">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="16f56-105">.</span><span class="sxs-lookup"><span data-stu-id="16f56-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f56-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16f56-106">Syntax</span></span>

<span data-ttu-id="16f56-107">*выражения* . ForeignTable</span><span class="sxs-lookup"><span data-stu-id="16f56-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="16f56-108">*выражение* Переменная, представляюная объект **Relation.**</span><span class="sxs-lookup"><span data-stu-id="16f56-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f56-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="16f56-109">Remarks</span></span>

<span data-ttu-id="16f56-110">Это свойство является объектом read/write для нового объекта **[Relation,](relation-object-dao.md)** еще не примыкаемого к коллекции, и только для чтения существующего объекта **Relation** в коллекции **[Relations.](relations-collection-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="16f56-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="16f56-111">Параметр **свойства ForeignTable** объекта **Relation** **[](connection-name-property-dao.md)** — это параметр свойства Name объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef,](querydef-object-dao.md)** представляюющий иностранную таблицу или запрос; Параметр **[Свойства Таблица](relation-table-property-dao.md)** — это параметр **свойства Name** объекта **TableDef** или **QueryDef,** который представляет основную таблицу или запрос.</span><span class="sxs-lookup"><span data-stu-id="16f56-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="16f56-112">Например, если в таблице ValidParts хранится список действительных кодов части (в поле с именем PartNo), можно установить связь со таблицей OrderItem так, что если код части был введен в таблицу OrderItem, он должен быть уже в таблице ValidParts.</span><span class="sxs-lookup"><span data-stu-id="16f56-112">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table.</span></span> <span data-ttu-id="16f56-113">Если код части не существовал в таблице ValidParts и **[](field-attributes-property-dao.md)** вы не заостряли свойство Атрибуты объекта **Relation** на **dbRelationDontEnforce,** может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="16f56-113">If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="16f56-114">В этом случае основной таблицей является таблица  ValidParts,  поэтому свойство Table объекта Relation будет задано validParts, а свойство **ForeignTable** объекта Relation — orderItem. </span><span class="sxs-lookup"><span data-stu-id="16f56-114">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="16f56-115">Свойства **имени** и **иностранного** имени объекта **Field** в коллекции  Поля объекта **Relation** будут задатки PartNo.</span><span class="sxs-lookup"><span data-stu-id="16f56-115">The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="16f56-116">Пример</span><span class="sxs-lookup"><span data-stu-id="16f56-116">Example</span></span>

<span data-ttu-id="16f56-117">В этом примере **показано,** как свойства **Table, ForeignTable** и **ForeignName** определяют условия связи **между** двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="16f56-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
