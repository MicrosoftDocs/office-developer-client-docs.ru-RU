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
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="8b238-102">Свойство Relation.ForeignTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="8b238-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="8b238-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b238-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b238-104">Задает или возвращает имя внешней таблицы в связи (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8b238-104">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8b238-105">.</span><span class="sxs-lookup"><span data-stu-id="8b238-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b238-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b238-106">Syntax</span></span>

<span data-ttu-id="8b238-107">*выражение .* ForeignTable</span><span class="sxs-lookup"><span data-stu-id="8b238-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="8b238-108">*выражение* Переменная, представляюная объект **Relation.**</span><span class="sxs-lookup"><span data-stu-id="8b238-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b238-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="8b238-109">Remarks</span></span>

<span data-ttu-id="8b238-110">Это свойство доступно для чтения и записи для нового объекта **[Relation,](relation-object-dao.md)** который еще не был придан коллекции, и доступно только для чтения для существующего объекта **Relation** в коллекции **[Relations.](relations-collection-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="8b238-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="8b238-111">Параметр **свойства ForeignTable** объекта **Relation** — это параметр свойства **[Name](connection-name-property-dao.md)** объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef,](querydef-object-dao.md)** который представляет собой инофровую таблицу или запрос; Параметр **[свойства Table](relation-table-property-dao.md)** — это параметр свойства **Name** объекта **TableDef** или **QueryDef,** который представляет основную таблицу или запрос.</span><span class="sxs-lookup"><span data-stu-id="8b238-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="8b238-112">Например, если в таблице ValidParts хранится список допустимого кода части (в поле с именем PartNo), можно установить связь с таблицей OrderItem таким образом, чтобы если бы код части был введен в таблицу OrderItem, он должен был бы уже быть в таблице ValidParts.</span><span class="sxs-lookup"><span data-stu-id="8b238-112">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table.</span></span> <span data-ttu-id="8b238-113">Если код части не существует в таблице ValidParts и вы не установили для свойства **[Attributes](field-attributes-property-dao.md)** объекта **Relation** значение **dbRelationDontEnforce,** произойдет перехватимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="8b238-113">If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="8b238-114">В этом случае таблица ValidParts является основной, поэтому свойство **Table** объекта **Relation** будет иметь свойство ValidParts, а свойство **ForeignTable** объекта **Relation** — OrderItem.</span><span class="sxs-lookup"><span data-stu-id="8b238-114">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="8b238-115">Свойства **Name** и **ForeignName** объекта **Field** в коллекции **Fields** объекта **Relation** будут иметь имя PartNo.</span><span class="sxs-lookup"><span data-stu-id="8b238-115">The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="8b238-116">Пример</span><span class="sxs-lookup"><span data-stu-id="8b238-116">Example</span></span>

<span data-ttu-id="8b238-117">В этом примере показано, как свойства **Table,** **ForeignTable** и **ForeignName** определяют термины **отношения** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="8b238-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
