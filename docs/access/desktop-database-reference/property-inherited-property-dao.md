---
title: Property.Inherited Property (DAO)
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
ms.openlocfilehash: 7768ec3048c14962154fa8ba54f391a9a8a10e66
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887980"
---
# <a name="propertyinherited-property-dao"></a><span data-ttu-id="7cd77-102">Property.Inherited Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="7cd77-102">Property.Inherited Property (DAO)</span></span>


<span data-ttu-id="7cd77-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cd77-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="7cd77-104">Возвращает значение, указывающее, является ли объект **[Свойства](property-object-dao.md)** наследуется из базового объекта.</span><span class="sxs-lookup"><span data-stu-id="7cd77-104">Returns a value that indicates whether a **[Property](property-object-dao.md)** object is inherited from an underlying object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd77-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cd77-105">Syntax</span></span>

<span data-ttu-id="7cd77-106">*выражение* . Унаследованные</span><span class="sxs-lookup"><span data-stu-id="7cd77-106">*expression* .Inherited</span></span>

<span data-ttu-id="7cd77-107">*выражение* Переменная, которая представляет собой объект- **свойство** .</span><span class="sxs-lookup"><span data-stu-id="7cd77-107">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd77-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="7cd77-108">Remarks</span></span>

<span data-ttu-id="7cd77-109">Для встроенных **свойств** объектов, которые представляют предварительно определенные свойства единственными возможными возвращаемое значение — **значение False**.</span><span class="sxs-lookup"><span data-stu-id="7cd77-109">For built-in **Property** objects that represent predefined properties, the only possible return value is **False**.</span></span>

<span data-ttu-id="7cd77-110">Чтобы определить, был ли создан пользовательских **свойств** для объекта, его можно применить, можно использовать свойство **Inherited** или ли **свойство** наследующего от другого объекта.</span><span class="sxs-lookup"><span data-stu-id="7cd77-110">You can use the **Inherited** property to determine whether a user-defined **Property** was created for the object it applies to, or whether the **Property** was inherited from another object.</span></span> <span data-ttu-id="7cd77-111">Предположим, например, создание нового **Свойства** для объекта **[QueryDef](querydef-object-dao.md)** и откройте объект **[набора записей](recordset-object-dao.md)** из объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="7cd77-111">For example, suppose you create a new **Property** for a **[QueryDef](querydef-object-dao.md)** object and then open a **[Recordset](recordset-object-dao.md)** object from the **QueryDef** object.</span></span> <span data-ttu-id="7cd77-112">Это новое **свойство** будет частью коллекции **[свойств](properties-collection-dao.md)** объекта **набора записей** и его свойство **Inherited** будет присвоено **значение True,** так как свойство был создан для объекта **QueryDef** не \*\* Набор записей\*\* объекта.</span><span class="sxs-lookup"><span data-stu-id="7cd77-112">This new **Property** will be part of the **Recordset** object's **[Properties](properties-collection-dao.md)** collection, and its **Inherited** property will be set to **True** because the property was created for the **QueryDef** object, not the **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="7cd77-113">Пример</span><span class="sxs-lookup"><span data-stu-id="7cd77-113">Example</span></span>

<span data-ttu-id="7cd77-114">В этом примере свойство **Inherited** используется для определения, был ли создан объект пользовательские **Свойства** для объекта **набора записей** или для некоторых базового объекта.</span><span class="sxs-lookup"><span data-stu-id="7cd77-114">This example use the **Inherited** property to determine if a user-defined **Property** object was created for a **Recordset** object or for some underlying object.</span></span>

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

