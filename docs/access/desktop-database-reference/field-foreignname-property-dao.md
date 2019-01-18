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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708468"
---
# <a name="fieldforeignname-property-dao"></a><span data-ttu-id="2ad84-102">Свойство Field.ForeignName (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ad84-102">Field.ForeignName property (DAO)</span></span>


<span data-ttu-id="2ad84-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ad84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ad84-104">Задает или возвращает значение, указывающее имя объекта **[поля](field-object-dao.md)** внешней таблицы, соответствующее поле в основной таблицы для связи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2ad84-104">Sets or returns a value that specifies the name of the **[Field](field-object-dao.md)** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ad84-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ad84-105">Syntax</span></span>

<span data-ttu-id="2ad84-106">*выражение* . ForeignName</span><span class="sxs-lookup"><span data-stu-id="2ad84-106">*expression* .ForeignName</span></span>

<span data-ttu-id="2ad84-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="2ad84-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ad84-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="2ad84-108">Remarks</span></span>

<span data-ttu-id="2ad84-109">Если объект **[связи](relation-object-dao.md)** не добавлено в **[базе данных](database-object-dao.md)**, но **поля** добавляется к объекту **отношения** , свойство **ForeignName** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="2ad84-109">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field** is appended to the **Relation** object, the **ForeignName** property is read/write.</span></span> <span data-ttu-id="2ad84-110">Если объект **отношения** добавляется к базе данных, свойство **ForeignName** доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2ad84-110">Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="2ad84-111">Только объект **поля** , к которому относится к коллекции **полей** объект **связи** может поддерживать свойство **ForeignName** .</span><span class="sxs-lookup"><span data-stu-id="2ad84-111">Only a **Field** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="2ad84-112">**[Имя](connection-name-property-dao.md)** и **ForeignName** параметры свойства для объекта **поля** укажите имена соответствующие поля в таблице первичного и внешнего отношения.</span><span class="sxs-lookup"><span data-stu-id="2ad84-112">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field** object specify the names of the corresponding fields in the primary and foreign tables of a relationship.</span></span> <span data-ttu-id="2ad84-113">Значения свойств **[в таблице](relation-table-property-dao.md)** и **[таблицавнешнегоключа](relation-foreigntable-property-dao.md)** для **связи** объекта определение таблицы основного и внешнего отношения.</span><span class="sxs-lookup"><span data-stu-id="2ad84-113">The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="2ad84-114">Например, если у вас есть список кодов допустимый части (в поле с именем PartNo) хранятся в таблице ValidParts удалось установить связь с таблицей OrderItem таким образом, если часть кода были введены в таблицу OrderItem, его придется уже существует в ValidPa Таблица RTS.</span><span class="sxs-lookup"><span data-stu-id="2ad84-114">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table.</span></span> <span data-ttu-id="2ad84-115">Если часть кода не был найден в таблице ValidParts и не было задано свойство **[атрибуты](field-attributes-property-dao.md)** объекта **отношения** к **dbRelationDontEnforce**, возникнет перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="2ad84-115">If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="2ad84-116">В этом случае в таблице ValidParts является таблицей внешнего, поэтому свойство **таблицавнешнегоключа** объекта **связь** устанавливается в ValidParts и свойство **таблицы** объект **связи** будет иметь значение OrderItem.</span><span class="sxs-lookup"><span data-stu-id="2ad84-116">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="2ad84-117">Свойства **Name** и **ForeignName** объекта **поля** в коллекции **полей** объект **связи** будет иметь значение PartNo.</span><span class="sxs-lookup"><span data-stu-id="2ad84-117">The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="2ad84-118">Пример</span><span class="sxs-lookup"><span data-stu-id="2ad84-118">Example</span></span>

<span data-ttu-id="2ad84-119">В этом примере показано, как определить свойства **в таблице**, **таблицавнешнегоключа**и **ForeignName** условия **отношения** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="2ad84-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
