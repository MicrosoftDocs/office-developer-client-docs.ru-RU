---
title: Свойство. Inherited (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf3aef6d04c7d7cc573ec1d6efaca7d5238f5125
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302928"
---
# <a name="propertyinherited-property-dao"></a><span data-ttu-id="5243b-102">Свойство. Inherited (DAO)</span><span class="sxs-lookup"><span data-stu-id="5243b-102">Property.Inherited property (DAO)</span></span>


<span data-ttu-id="5243b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5243b-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="5243b-104">Возвращает значение, которое указывает, наследуется ли объект **[Свойства](property-object-dao.md)** из базового объекта.</span><span class="sxs-lookup"><span data-stu-id="5243b-104">Returns a value that indicates whether a **[Property](property-object-dao.md)** object is inherited from an underlying object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5243b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5243b-105">Syntax</span></span>

<span data-ttu-id="5243b-106">*Expression* . Наследуется</span><span class="sxs-lookup"><span data-stu-id="5243b-106">*expression* .Inherited</span></span>

<span data-ttu-id="5243b-107">*Expression (выражение* ) Переменная, представляющая объект **Property** .</span><span class="sxs-lookup"><span data-stu-id="5243b-107">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5243b-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="5243b-108">Remarks</span></span>

<span data-ttu-id="5243b-109">Для встроенных объектов **Property** , представляющих собой предопределенные свойства, единственным возможным возвращаемым значением является **false**.</span><span class="sxs-lookup"><span data-stu-id="5243b-109">For built-in **Property** objects that represent predefined properties, the only possible return value is **False**.</span></span>

<span data-ttu-id="5243b-110">Можно использовать унаследованное \*\*\*\* свойство, чтобы определить, было ли создано пользовательское **свойство** для объекта, к которому он применяется, или же **свойство** было унаследовано от другого объекта.</span><span class="sxs-lookup"><span data-stu-id="5243b-110">You can use the **Inherited** property to determine whether a user-defined **Property** was created for the object it applies to, or whether the **Property** was inherited from another object.</span></span> <span data-ttu-id="5243b-111">Например, предположим, что вы создаете новое **свойство** для объекта **[QueryDef](querydef-object-dao.md)** , а затем открыли объект **[Recordset](recordset-object-dao.md)** из объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="5243b-111">For example, suppose you create a new **Property** for a **[QueryDef](querydef-object-dao.md)** object and then open a **[Recordset](recordset-object-dao.md)** object from the **QueryDef** object.</span></span> <span data-ttu-id="5243b-112">Это новое **свойство** будет частью коллекции **[свойств](properties-collection-dao.md)** объекта **Recordset** , а его унаследованное свойство будет \*\*\*\* иметь значение **true** , так как свойство было создано для объекта **QueryDef** , а не \*\* Объект Recordset\*\* .</span><span class="sxs-lookup"><span data-stu-id="5243b-112">This new **Property** will be part of the **Recordset** object's **[Properties](properties-collection-dao.md)** collection, and its **Inherited** property will be set to **True** because the property was created for the **QueryDef** object, not the **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="5243b-113">Пример</span><span class="sxs-lookup"><span data-stu-id="5243b-113">Example</span></span>

<span data-ttu-id="5243b-114">В этом примере показано \*\*\*\* , как использовать унаследованное свойство, чтобы определить, был ли создан пользовательский объект **свойства** для объекта **Recordset** или для некоторого базового объекта.</span><span class="sxs-lookup"><span data-stu-id="5243b-114">This example use the **Inherited** property to determine if a user-defined **Property** object was created for a **Recordset** object or for some underlying object.</span></span>

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

