---
title: Свойство Recordset. restarted Property (DAO)
TOCTitle: Restartable Property
ms:assetid: 00def49d-ea7e-6cd5-2f4a-914a1ddcdd51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844737(v=office.15)
ms:contentKeyID: 48542919
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052926
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5142d0d47be37ca8c2e1c6b89462c05b7d41d302
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307576"
---
# <a name="recordsetrestartable-property-dao"></a><span data-ttu-id="295dd-102">Свойство Recordset. restarted Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="295dd-102">Recordset.Restartable property (DAO)</span></span>


<span data-ttu-id="295dd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="295dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="295dd-104">Возвращает значение, которое указывает на то, поддерживает ли объект **[Recordset](recordset-object-dao.md)** метод **[Requery](recordset-requery-method-dao.md)**, который повторно выполняет запрос, на котором основан объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="295dd-104">Returns a value that indicates whether a **[Recordset](recordset-object-dao.md)** object supports the **[Requery](recordset-requery-method-dao.md)** method, which re-executes the query on which the **Recordset** object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="295dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="295dd-105">Syntax</span></span>

<span data-ttu-id="295dd-106">*Expression* . Перезапускаемой</span><span class="sxs-lookup"><span data-stu-id="295dd-106">*expression* .Restartable</span></span>

<span data-ttu-id="295dd-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="295dd-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="295dd-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="295dd-108">Remarks</span></span>

<span data-ttu-id="295dd-109">Объект **Recordset** табличного типа всегда возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="295dd-109">Table-type **Recordset** objects always return **False**.</span></span>

<span data-ttu-id="295dd-110">Проверьте свойство \*\*\*\* restarted перед использованием метода Restart объекта **Recordset** . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="295dd-110">Check the **Restartable** property before using the **Requery** method on a **Recordset** object.</span></span> <span data-ttu-id="295dd-111">Если свойство restarted объекта имеет значение **false**, используйте метод **[OpenRecordset](connection-openrecordset-method-dao.md)** базового объекта **[QueryDef](querydef-object-dao.md)** , чтобы повторно выполнить запрос. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="295dd-111">If the object's **Restartable** property is set to **False**, use the **[OpenRecordset](connection-openrecordset-method-dao.md)** method on the underlying **[QueryDef](querydef-object-dao.md)** object to re-execute the query.</span></span>

## <a name="example"></a><span data-ttu-id="295dd-112">Пример</span><span class="sxs-lookup"><span data-stu-id="295dd-112">Example</span></span>

<span data-ttu-id="295dd-113">В этом примере показано \*\*\*\* свойство restarted с различными объектами **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="295dd-113">This example demonstrates the **Restartable** property with different **Recordset** objects.</span></span>

```vb
    Sub RestartableX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTemp As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open a table-type Recordset and print its 
     ' Restartable property. 
     Set rstTemp = .OpenRecordset("Employees", dbOpenTable) 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from an SQL statement and print its 
     ' Restartable property. 
     Set rstTemp = _ 
     .OpenRecordset("SELECT * FROM Employees") 
     Debug.Print "Recordset based on SQL statement" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from a saved QueryDef object and 
     ' print its Restartable property. 
     Set rstTemp = .OpenRecordset("Current Product List") 
     Debug.Print _ 
     "Recordset based on permanent QueryDef (" & _ 
     rstTemp.Name & ")" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     .Close 
     End With 
     
    End Sub
```
