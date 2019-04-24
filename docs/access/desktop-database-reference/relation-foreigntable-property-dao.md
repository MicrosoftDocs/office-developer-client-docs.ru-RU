---
title: Свойство relation. ForeignTable (DAO)
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
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="a303c-102">Свойство relation. ForeignTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="a303c-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="a303c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a303c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a303c-104">Задает или возвращает имя внешней таблицы в отношении (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a303c-104">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="a303c-105">.</span><span class="sxs-lookup"><span data-stu-id="a303c-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="a303c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a303c-106">Syntax</span></span>

<span data-ttu-id="a303c-107">*Expression* . ForeignTable</span><span class="sxs-lookup"><span data-stu-id="a303c-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="a303c-108">*Expression (выражение* ) Переменная, представляющая объект **связи** .</span><span class="sxs-lookup"><span data-stu-id="a303c-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a303c-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="a303c-109">Remarks</span></span>

<span data-ttu-id="a303c-110">Это свойство доступно для чтения и записи для нового объекта **[relation](relation-object-dao.md)** , который еще не добавлен в коллекцию и доступен только для чтения для существующего объекта **relation** в коллекции **[связей](relations-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="a303c-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="a303c-111">Значение свойства **ForeignTable** объекта **relation** — это свойство **[имени](connection-name-property-dao.md)** объекта **[tabledef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** объекта, представляющего внешние таблицы или запросы; Свойство **[Table](relation-table-property-dao.md)** — это значение свойства **Name** объекта **tabledef** или **QueryDef** , представляющего основную таблицу или запрос.</span><span class="sxs-lookup"><span data-stu-id="a303c-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="a303c-112">Например, если у вас есть список допустимых кодов частей (в поле с именем Партно), хранящихся в таблице Валидпартс, можно установить связь с таблицей Ордеритем таким образом, что если в таблицу Ордеритем был введен код части, он должен быть уже включен в Валидпартс  приведен.</span><span class="sxs-lookup"><span data-stu-id="a303c-112">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table.</span></span> <span data-ttu-id="a303c-113">Если код части не существовал в таблице Валидпартс и не присвоено свойству **[Attributes](field-attributes-property-dao.md)** объекта **relation** значение **дбрелатиондонтенфорце**, возникнет Перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="a303c-113">If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="a303c-114">В этом случае таблица Валидпартс является основной таблицей, поэтому свойству **Table** объекта **relation** будет присвоено значение валидпартс, а свойству **ForeignTable** объекта **relation** будет присвоено значение ордеритем.</span><span class="sxs-lookup"><span data-stu-id="a303c-114">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="a303c-115">Свойства **Name** и **фореигннаме** объекта **field** в коллекции **Fields** объекта **relation** задаются как партно.</span><span class="sxs-lookup"><span data-stu-id="a303c-115">The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="a303c-116">Пример</span><span class="sxs-lookup"><span data-stu-id="a303c-116">Example</span></span>

<span data-ttu-id="a303c-117">В этом примере показано, как свойства **Table**, **ForeignTable**и **фореигннаме** определяют условия **связи** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="a303c-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
