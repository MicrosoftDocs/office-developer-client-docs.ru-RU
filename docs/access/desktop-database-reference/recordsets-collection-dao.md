---
title: Коллекция наборов записей (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b935e05264497c7ad09ada4a8c50c775845857b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718765"
---
# <a name="recordsets-collection-dao"></a><span data-ttu-id="39e44-102">Коллекция наборов записей (DAO)</span><span class="sxs-lookup"><span data-stu-id="39e44-102">Recordsets collection (DAO)</span></span>

<span data-ttu-id="39e44-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39e44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39e44-104">Коллекция **наборов записей** содержит все открытые объекты **набора записей** в объекте **подключения** или **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="39e44-104">A **Recordsets** collection contains all open **Recordset** objects in a **Connection** or **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e44-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="39e44-105">Remarks</span></span>

<span data-ttu-id="39e44-106">При использовании объектов DAO работы с данным почти полностью с помощью объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="39e44-106">When you use DAO objects, you manipulate data almost entirely using **Recordset** objects.</span></span>

<span data-ttu-id="39e44-107">Новый объект **набора записей** автоматически добавляется в коллекцию **наборов записей** при открытии объекта **набора записей** и автоматически удаляются при закрытии.</span><span class="sxs-lookup"><span data-stu-id="39e44-107">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the **Recordset** object, and is automatically removed when you close it.</span></span>

<span data-ttu-id="39e44-108">Можно создать любое количество переменных объекта **набора записей** при необходимости.</span><span class="sxs-lookup"><span data-stu-id="39e44-108">You can create as many **Recordset** object variables as needed.</span></span> <span data-ttu-id="39e44-109">Объекты различных **наборов записей** можно получить доступ к таблиц, запросов и полей без конфликтов.</span><span class="sxs-lookup"><span data-stu-id="39e44-109">Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="39e44-110">Для ссылки на объект **набора записей** в коллекции по его порядковый номер или по **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="39e44-110">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="39e44-111">**Наборы записей** (0)</span><span class="sxs-lookup"><span data-stu-id="39e44-111">**Recordsets**(0)</span></span>

- <span data-ttu-id="39e44-112">**Наборы записей** («имя»)</span><span class="sxs-lookup"><span data-stu-id="39e44-112">**Recordsets**("name")</span></span>

- <span data-ttu-id="39e44-113">**Наборы записей**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="39e44-113">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="39e44-114">Объект **набора записей** можно открыть из одного источника данных или базы данных более одного раза, Создание повторяющихся имен в коллекции **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="39e44-114">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection.</span></span> <span data-ttu-id="39e44-115">Следует назначить объектов **наборов записей** объектных переменных и обращаться к ним с именем переменной.</span><span class="sxs-lookup"><span data-stu-id="39e44-115">You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="39e44-116">Пример</span><span class="sxs-lookup"><span data-stu-id="39e44-116">Example</span></span>

<span data-ttu-id="39e44-117">В этом примере демонстрируется **набора записей** объекты и коллекции **наборов записей** , открыв четыре различных типов **наборов записей**, перечисления коллекции наборов записей текущей **базы данных**и перечисление \*\* Свойства\*\* коллекцию каждого **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="39e44-117">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

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
