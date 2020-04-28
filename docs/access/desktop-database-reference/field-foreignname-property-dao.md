---
title: Свойство Field.ForeignName (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7c340eee9972e8247654ec863ba0ef4588ef65f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293107"
---
# <a name="fieldforeignname-property-dao"></a><span data-ttu-id="63433-102">Свойство Field.ForeignName (DAO)</span><span class="sxs-lookup"><span data-stu-id="63433-102">Field.ForeignName property (DAO)</span></span>


<span data-ttu-id="63433-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63433-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63433-104">Задает или возвращает значение, задающее имя объекта **[поля](field-object-dao.md)** в внешней таблице, которое соответствует полю в главной таблице для отношения (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="63433-104">Sets or returns a value that specifies the name of the **[Field](field-object-dao.md)** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="63433-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63433-105">Syntax</span></span>

<span data-ttu-id="63433-106">*Expression* . фореигннаме</span><span class="sxs-lookup"><span data-stu-id="63433-106">*expression* .ForeignName</span></span>

<span data-ttu-id="63433-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="63433-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="63433-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="63433-108">Remarks</span></span>

<span data-ttu-id="63433-109">Если объект **[relation](relation-object-dao.md)** не добавляется в **[базу данных](database-object-dao.md)**, но **поле** добавляется к объекту **relation** , свойство **фореигннаме** доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="63433-109">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field** is appended to the **Relation** object, the **ForeignName** property is read/write.</span></span> <span data-ttu-id="63433-110">Когда объект **relation** добавляется в базу данных, свойство **фореигннаме** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63433-110">Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="63433-111">Только объект **field** , принадлежащий коллекции **Fields** объекта **relation** , может поддерживать свойство **фореигннаме** .</span><span class="sxs-lookup"><span data-stu-id="63433-111">Only a **Field** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="63433-112">Параметры свойств **[Name](connection-name-property-dao.md)** и **Фореигннаме** для объекта **field** задают имена соответствующих полей в основной и внешней таблицах связи.</span><span class="sxs-lookup"><span data-stu-id="63433-112">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field** object specify the names of the corresponding fields in the primary and foreign tables of a relationship.</span></span> <span data-ttu-id="63433-113">Параметры свойств **[Table](relation-table-property-dao.md)** и **[ForeignTable](relation-foreigntable-property-dao.md)** для объекта **relation** определяют первичную и внешнюю таблицы связи.</span><span class="sxs-lookup"><span data-stu-id="63433-113">The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="63433-114">Например, если у вас есть список допустимых кодов частей (в поле с именем Партно), хранящихся в таблице Валидпартс, можно установить связь с таблицей Ордеритем таким образом, что при вводе кода части в таблицу Ордеритем они должны уже существовать в таблице Валидпартс.</span><span class="sxs-lookup"><span data-stu-id="63433-114">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table.</span></span> <span data-ttu-id="63433-115">Если код части не существовал в таблице Валидпартс и не присвоено свойству **[Attributes](field-attributes-property-dao.md)** объекта **relation** значение **дбрелатиондонтенфорце**, возникнет Перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="63433-115">If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="63433-116">В этом случае таблица Валидпартс является внешней таблицей, поэтому свойству **ForeignTable** объекта **relation** будет присвоено значение валидпартс, а свойству **Table** объекта **relation** будет присвоено значение ордеритем.</span><span class="sxs-lookup"><span data-stu-id="63433-116">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="63433-117">Свойства **Name** и **фореигннаме** объекта **field** в коллекции **Fields** объекта **relation** задаются как партно.</span><span class="sxs-lookup"><span data-stu-id="63433-117">The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="63433-118">Пример</span><span class="sxs-lookup"><span data-stu-id="63433-118">Example</span></span>

<span data-ttu-id="63433-119">В этом примере показано, как свойства **Table**, **ForeignTable**и **фореигннаме** определяют условия **связи** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="63433-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
