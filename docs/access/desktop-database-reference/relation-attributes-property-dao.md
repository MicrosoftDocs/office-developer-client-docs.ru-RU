---
title: Свойство Relation.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: db19d2ad-5965-214c-211d-9a8eb9c3c522
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835337(v=office.15)
ms:contentKeyID: 48548098
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc6bd5ccc607854ab59de51bdb96d9ceebe1acf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708888"
---
# <a name="relationattributes-property-dao"></a><span data-ttu-id="0d310-102">Свойство Relation.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="0d310-102">Relation.Attributes property (DAO)</span></span>


<span data-ttu-id="0d310-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d310-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d310-104">Задает или возвращает значение, указывающее, один или несколько характеристик объект **связи** .</span><span class="sxs-lookup"><span data-stu-id="0d310-104">Sets or returns a value that indicates one or more characteristics of a **Relation** object.</span></span> <span data-ttu-id="0d310-105">Чтение и запись **времени**.</span><span class="sxs-lookup"><span data-stu-id="0d310-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d310-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d310-106">Syntax</span></span>

<span data-ttu-id="0d310-107">*выражение* . Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0d310-107">*expression* .Attributes</span></span>

<span data-ttu-id="0d310-108">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="0d310-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d310-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="0d310-109">Remarks</span></span>

<span data-ttu-id="0d310-110">Для объекта еще не добавляется в конец коллекции это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0d310-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="0d310-111">Пример</span><span class="sxs-lookup"><span data-stu-id="0d310-111">Example</span></span>

<span data-ttu-id="0d310-112">В этом примере отображаются свойства **атрибуты** для **полей**, **связь**и **TableDef** объектов базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="0d310-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

