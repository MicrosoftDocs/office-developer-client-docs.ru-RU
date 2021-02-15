---
title: Коллекция Recordsets (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b935e05264497c7ad09ada4a8c50c775845857b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309305"
---
# <a name="recordsets-collection-dao"></a><span data-ttu-id="678e1-102">Коллекция Recordsets (DAO)</span><span class="sxs-lookup"><span data-stu-id="678e1-102">Recordsets collection (DAO)</span></span>

<span data-ttu-id="678e1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="678e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="678e1-104">Коллекция **Recordsets содержит** все открытые объекты **Recordset** в **объекте Connection** или **Database.**</span><span class="sxs-lookup"><span data-stu-id="678e1-104">A **Recordsets** collection contains all open **Recordset** objects in a **Connection** or **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="678e1-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="678e1-105">Remarks</span></span>

<span data-ttu-id="678e1-106">Если вы используете интерфейс DAO, вы можете управлять данными практически полностью с помощью объектов **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="678e1-106">When you use DAO objects, you manipulate data almost entirely using **Recordset** objects.</span></span>

<span data-ttu-id="678e1-107">Новый объект **Recordset** автоматически добавляется в коллекцию **Recordsets** при открываемом объекте **Recordset** и автоматически удаляется при его закрытии.</span><span class="sxs-lookup"><span data-stu-id="678e1-107">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the **Recordset** object, and is automatically removed when you close it.</span></span>

<span data-ttu-id="678e1-108">Вы можете создать любое количество переменных объекта **Recordset** при необходимости.</span><span class="sxs-lookup"><span data-stu-id="678e1-108">You can create as many **Recordset** object variables as needed.</span></span> <span data-ttu-id="678e1-109">Различные объекты **Recordset** могут получать доступ к одним таблицам, запросам и полям без возникновения конфликта.</span><span class="sxs-lookup"><span data-stu-id="678e1-109">Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="678e1-110">Чтобы сослаться на объект **Recordset** в коллекции по его порядковому номеру или по его свойству **Name**, используйте любую из следующих синтаксических форм:</span><span class="sxs-lookup"><span data-stu-id="678e1-110">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="678e1-111">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="678e1-111">**Recordsets**(0)</span></span>

- <span data-ttu-id="678e1-112">**Recordsets**("name")</span><span class="sxs-lookup"><span data-stu-id="678e1-112">**Recordsets**("name")</span></span>

- <span data-ttu-id="678e1-113">**Recordsets**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="678e1-113">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="678e1-114">Вы можете открыть объект **Recordset** из одного источника данных или базы данных несколько раз, создавая дублирующие имена в коллекции **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="678e1-114">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection.</span></span> <span data-ttu-id="678e1-115">Вы должны назначить объекты **Recordsets** для переменных объекта и ссылаться на них по имени переменной.</span><span class="sxs-lookup"><span data-stu-id="678e1-115">You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="678e1-116">Пример</span><span class="sxs-lookup"><span data-stu-id="678e1-116">Example</span></span>

<span data-ttu-id="678e1-117">В этом примере показаны объекты **Recordset** и коллекция **Recordset** с помощью открытия четырех разных типов **Recordsets**, перечисления коллекции Recordsets для текущего объекта **Database** и перечисления коллекции **Properties** для каждого объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="678e1-117">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
