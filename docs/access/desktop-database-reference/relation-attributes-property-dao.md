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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309116"
---
# <a name="relationattributes-property-dao"></a><span data-ttu-id="66124-102">Свойство Relation.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="66124-102">Relation.Attributes property (DAO)</span></span>


<span data-ttu-id="66124-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66124-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66124-104">Задает или возвращает значение, которое указывает одну или несколько характеристик объекта **Relation.**</span><span class="sxs-lookup"><span data-stu-id="66124-104">Sets or returns a value that indicates one or more characteristics of a **Relation** object.</span></span> <span data-ttu-id="66124-105">Для чтения и записи, **Long**.</span><span class="sxs-lookup"><span data-stu-id="66124-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="66124-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66124-106">Syntax</span></span>

<span data-ttu-id="66124-107">*expression* .Attributes</span><span class="sxs-lookup"><span data-stu-id="66124-107">*expression* .Attributes</span></span>

<span data-ttu-id="66124-108">*выражение* Переменная, представляюная объект **Relation.**</span><span class="sxs-lookup"><span data-stu-id="66124-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="66124-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="66124-109">Remarks</span></span>

<span data-ttu-id="66124-110">Для объекта, который еще не добавлен в коллекцию, это свойство предназначено для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="66124-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="66124-111">Пример</span><span class="sxs-lookup"><span data-stu-id="66124-111">Example</span></span>

<span data-ttu-id="66124-112">Этот пример отображает свойство **Attributes** для объектов **Field**, **Relation** и **TableDef** в базе данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="66124-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

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

