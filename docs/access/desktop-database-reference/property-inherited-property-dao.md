---
title: Свойство Property.Inherited (DAO)
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
# <a name="propertyinherited-property-dao"></a><span data-ttu-id="293ff-102">Свойство Property.Inherited (DAO)</span><span class="sxs-lookup"><span data-stu-id="293ff-102">Property.Inherited property (DAO)</span></span>


<span data-ttu-id="293ff-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="293ff-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="293ff-104">Возвращает значение, которое указывает, наследуется ли объект **[Property](property-object-dao.md)** от одного из его объектов.</span><span class="sxs-lookup"><span data-stu-id="293ff-104">Returns a value that indicates whether a **[Property](property-object-dao.md)** object is inherited from an underlying object.</span></span>

## <a name="syntax"></a><span data-ttu-id="293ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="293ff-105">Syntax</span></span>

<span data-ttu-id="293ff-106">*выражение .* Унаследовано</span><span class="sxs-lookup"><span data-stu-id="293ff-106">*expression* .Inherited</span></span>

<span data-ttu-id="293ff-107">*выражение* Переменная, представляюная объект **Property.**</span><span class="sxs-lookup"><span data-stu-id="293ff-107">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="293ff-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="293ff-108">Remarks</span></span>

<span data-ttu-id="293ff-109">Для встроенных **объектов Property,** которые представляют предопределенные свойства, единственным возможным возвращаемым значением является **False.**</span><span class="sxs-lookup"><span data-stu-id="293ff-109">For built-in **Property** objects that represent predefined properties, the only possible return value is **False**.</span></span>

<span data-ttu-id="293ff-110">Свойство **Inherited** можно использовать, чтобы определить, было  ли пользовательское свойство создано для объекта,  к который оно применяется, или было ли свойство унаследовано от другого объекта.</span><span class="sxs-lookup"><span data-stu-id="293ff-110">You can use the **Inherited** property to determine whether a user-defined **Property** was created for the object it applies to, or whether the **Property** was inherited from another object.</span></span> <span data-ttu-id="293ff-111">Например, предположим, что  вы создаете новое свойство для объекта **[QueryDef,](querydef-object-dao.md)** а затем открываете объект **[Recordset](recordset-object-dao.md)** из объекта **QueryDef.**</span><span class="sxs-lookup"><span data-stu-id="293ff-111">For example, suppose you create a new **Property** for a **[QueryDef](querydef-object-dao.md)** object and then open a **[Recordset](recordset-object-dao.md)** object from the **QueryDef** object.</span></span> <span data-ttu-id="293ff-112">Это новое **свойство** будет частью коллекции **[](properties-collection-dao.md)** свойств объекта **Recordset,** а его унаследованный свойство будет иметь свойство **True,** так как свойство было создано для объекта **QueryDef,** а не **объекта Recordset.** </span><span class="sxs-lookup"><span data-stu-id="293ff-112">This new **Property** will be part of the **Recordset** object's **[Properties](properties-collection-dao.md)** collection, and its **Inherited** property will be set to **True** because the property was created for the **QueryDef** object, not the **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="293ff-113">Пример</span><span class="sxs-lookup"><span data-stu-id="293ff-113">Example</span></span>

<span data-ttu-id="293ff-114">В этом примере свойство **Inherited** используется для определения, был ли создан пользовательский объект **Property** для объекта **Recordset** или для определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="293ff-114">This example use the **Inherited** property to determine if a user-defined **Property** object was created for a **Recordset** object or for some underlying object.</span></span>

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

