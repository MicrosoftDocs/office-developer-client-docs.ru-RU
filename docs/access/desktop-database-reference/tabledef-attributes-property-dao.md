---
title: Свойство TableDef.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: d01588c3-e94e-06bd-6568-974873411f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834701(v=office.15)
ms:contentKeyID: 48547828
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6a9047ac95e377863c2f8d0f7024ca3ff199a06
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921021"
---
# <a name="tabledefattributes-property-dao"></a><span data-ttu-id="58563-102">Свойство TableDef.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="58563-102">TableDef.Attributes property (DAO)</span></span>


<span data-ttu-id="58563-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="58563-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="58563-104">Задает или возвращает значение, указывающее, один или несколько характеристик объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="58563-104">Sets or returns a value that indicates one or more characteristics of a **TableDef** object.</span></span> <span data-ttu-id="58563-105">Чтение и запись **времени**.</span><span class="sxs-lookup"><span data-stu-id="58563-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="58563-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58563-106">Syntax</span></span>

<span data-ttu-id="58563-107">*выражение* . Атрибуты</span><span class="sxs-lookup"><span data-stu-id="58563-107">*expression* .Attributes</span></span>

<span data-ttu-id="58563-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="58563-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="58563-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="58563-109">Remarks</span></span>

<span data-ttu-id="58563-110">Для объекта еще не добавляется в конец коллекции это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="58563-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="58563-111">Пример</span><span class="sxs-lookup"><span data-stu-id="58563-111">Example</span></span>

<span data-ttu-id="58563-112">В этом примере отображаются свойства **атрибуты** для **полей**, **связь**и **TableDef** объектов базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="58563-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

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

