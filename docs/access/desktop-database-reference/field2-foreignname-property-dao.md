---
title: Field2.ForeignName Property (DAO)
TOCTitle: ForeignName Property
ms:assetid: 76da233a-efb4-63cd-a2a2-d18d9e2fb2fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196027(v=office.15)
ms:contentKeyID: 48545708
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052932
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eff81bf8d2e7f7f040611ffc1aafdedff1e35ddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874050"
---
# <a name="field2foreignname-property-dao"></a><span data-ttu-id="4159e-102">Field2.ForeignName Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="4159e-102">Field2.ForeignName Property (DAO)</span></span>


<span data-ttu-id="4159e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4159e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4159e-104">Задает или возвращает значение, указывающее имя объекта **поле2** внешней таблицы, соответствующее поле в основной таблицы для связи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4159e-104">Sets or returns a value that specifies the name of the **Field2** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4159e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4159e-105">Syntax</span></span>

<span data-ttu-id="4159e-106">*выражение* . ForeignName</span><span class="sxs-lookup"><span data-stu-id="4159e-106">*expression* .ForeignName</span></span>

<span data-ttu-id="4159e-107">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="4159e-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4159e-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="4159e-108">Remarks</span></span>

<span data-ttu-id="4159e-109">Если объект **[связи](relation-object-dao.md)** не добавлено в **[базе данных](database-object-dao.md)**, но **поле2** добавляется к объекту **отношения** , свойство **ForeignName** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4159e-109">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field2** is appended to the **Relation** object, the **ForeignName** property is read/write.</span></span> <span data-ttu-id="4159e-110">Если объект **отношения** добавляется к базе данных, свойство **ForeignName** доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4159e-110">Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="4159e-111">Только **поле2** объекта, к которому относится к коллекции **полей** объект **связи** может поддерживать свойство **ForeignName** .</span><span class="sxs-lookup"><span data-stu-id="4159e-111">Only a **Field2** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="4159e-112">**[Имя](connection-name-property-dao.md)** и **ForeignName** параметры свойств для объекта **поле2** укажите имена соответствующие поля в таблице первичного и внешнего отношения.</span><span class="sxs-lookup"><span data-stu-id="4159e-112">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field2** object specify the names of the corresponding fields in the primary and foreign tables of a relationship.</span></span> <span data-ttu-id="4159e-113">Значения свойств **[в таблице](relation-table-property-dao.md)** и **[таблицавнешнегоключа](relation-foreigntable-property-dao.md)** для **связи** объекта определение таблицы основного и внешнего отношения.</span><span class="sxs-lookup"><span data-stu-id="4159e-113">The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="4159e-114">Например, если у вас есть список кодов допустимый части (в поле с именем PartNo) хранятся в таблице ValidParts удалось установить связь с таблицей OrderItem таким образом, если часть кода были введены в таблицу OrderItem, его придется уже существует в ValidPa Таблица RTS.</span><span class="sxs-lookup"><span data-stu-id="4159e-114">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table.</span></span> <span data-ttu-id="4159e-115">Если часть кода не был найден в таблице ValidParts и не было задано свойство **[атрибуты](field-attributes-property-dao.md)** объекта **отношения** к **dbRelationDontEnforce**, возникнет перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="4159e-115">If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="4159e-116">В этом случае в таблице ValidParts является таблицей внешнего, поэтому свойство **таблицавнешнегоключа** объекта **связь** устанавливается в ValidParts и свойство **таблицы** объект **связи** будет иметь значение OrderItem.</span><span class="sxs-lookup"><span data-stu-id="4159e-116">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="4159e-117">Свойства **Name** и **ForeignName** объекта **поле2** в коллекции **полей** объект **связи** будет иметь значение PartNo.</span><span class="sxs-lookup"><span data-stu-id="4159e-117">The **Name** and **ForeignName** properties of the **Field2** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="4159e-118">Пример</span><span class="sxs-lookup"><span data-stu-id="4159e-118">Example</span></span>

<span data-ttu-id="4159e-119">В этом примере показано, как определить свойства **в таблице**, **таблицавнешнегоключа**и **ForeignName** условия **отношения** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="4159e-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
