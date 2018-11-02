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
ms.openlocfilehash: dcd454bc1c570e119cc8948acb8077a54649db84
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921714"
---
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="62e78-102">Свойство Relation.ForeignTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="62e78-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="62e78-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62e78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62e78-104">Возвращает или задает имя таблицы внешнего в отношении (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="62e78-104">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="62e78-105">.</span><span class="sxs-lookup"><span data-stu-id="62e78-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="62e78-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62e78-106">Syntax</span></span>

<span data-ttu-id="62e78-107">*выражение* . Таблицавнешнегоключа</span><span class="sxs-lookup"><span data-stu-id="62e78-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="62e78-108">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="62e78-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="62e78-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="62e78-109">Remarks</span></span>

<span data-ttu-id="62e78-110">Это свойство является чтение и запись для нового объекта **[отношения](relation-object-dao.md)** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **отношения** в коллекции **[отношений](relations-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="62e78-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="62e78-111">Установка свойства **таблицавнешнегоключа** объект **связи** является **[свойства Name **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** объект, представляющий внешнего таблицы или запроса;](connection-name-property-dao.md)** значение свойства **[в таблице](relation-table-property-dao.md)** — **свойства Name объекта **TableDef** или **QueryDef** , представляющий основной таблицы или запроса** .</span><span class="sxs-lookup"><span data-stu-id="62e78-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="62e78-112">Например, если у вас есть список кодов допустимый части (в поле с именем PartNo) хранятся в таблице ValidParts удалось установить связь с таблицей OrderItem таким образом, если часть кода были введены в таблицу OrderItem, необходимо быть ValidParts  в таблице.</span><span class="sxs-lookup"><span data-stu-id="62e78-112">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table.</span></span> <span data-ttu-id="62e78-113">Если часть кода не был найден в таблице ValidParts и не было задано свойство **[атрибуты](field-attributes-property-dao.md)** объекта **отношения** к **dbRelationDontEnforce**, возникнет перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="62e78-113">If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="62e78-114">В этом случае в таблице ValidParts представляет основной таблицы, поэтому устанавливается свойство **таблицы** объект **отношения** в ValidParts и свойство **таблицавнешнегоключа** объект **связи** будет иметь значение OrderItem.</span><span class="sxs-lookup"><span data-stu-id="62e78-114">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="62e78-115">Свойства **Name** и **ForeignName** объекта **поля** в коллекции **полей** объект **связи** будет иметь значение PartNo.</span><span class="sxs-lookup"><span data-stu-id="62e78-115">The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="62e78-116">Пример</span><span class="sxs-lookup"><span data-stu-id="62e78-116">Example</span></span>

<span data-ttu-id="62e78-117">В этом примере показано, как определить свойства **в таблице**, **таблицавнешнегоключа**и **ForeignName** условия **отношения** между двумя таблицами.</span><span class="sxs-lookup"><span data-stu-id="62e78-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
