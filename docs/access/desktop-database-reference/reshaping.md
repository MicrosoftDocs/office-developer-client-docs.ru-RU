---
title: Reshaping (Access desktop database reference)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314779"
---
# <a name="reshaping"></a><span data-ttu-id="dbca2-102">Изменение формы</span><span class="sxs-lookup"><span data-stu-id="dbca2-102">Reshaping</span></span>

<span data-ttu-id="dbca2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbca2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dbca2-104">Набору **записей,** созданному пунктом команды фигуры, может быть назначено имя псевдонима (как правило, с ключевым словом AS). </span><span class="sxs-lookup"><span data-stu-id="dbca2-104">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword).</span></span> <span data-ttu-id="dbca2-105">Псевдоним фигурного **recordset** можно ссылаться в совершенно другой команде.</span><span class="sxs-lookup"><span data-stu-id="dbca2-105">The alias of a shaped **Recordset** can be referenced in an entirely different command.</span></span> <span data-ttu-id="dbca2-106">То есть можно повторно использовать или переформаировать ранее сформированный **набор записей** в новой команде фигуры.</span><span class="sxs-lookup"><span data-stu-id="dbca2-106">That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command.</span></span> <span data-ttu-id="dbca2-107">Для поддержки этой функции ADO предоставляет свойство [Reshape Name](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dbca2-107">To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="dbca2-108">Переохитовка имеет две основные функции.</span><span class="sxs-lookup"><span data-stu-id="dbca2-108">Reshaping has two main functions.</span></span> <span data-ttu-id="dbca2-109">Во-первых, необходимо связать существующий **набор записей** с новым родительским **набором записей.**</span><span class="sxs-lookup"><span data-stu-id="dbca2-109">The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="dbca2-110">Пример</span><span class="sxs-lookup"><span data-stu-id="dbca2-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="dbca2-111">Вторая функция — включить доступ без глав к существующим объектам **recordset** для детей с помощью синтаксиса. `"SHAPE <recordset reshape name>"`</span><span class="sxs-lookup"><span data-stu-id="dbca2-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="dbca2-112">Нельзя прикрепить столбцы к существующему набору  **Recordset,** изменить параметризованный набор записей или объекты Recordset в любом пересекаемом пункте COMPUTE или выполнить совокупные операции для любого потомка **Recordset** из переостановки **recordset.** </span><span class="sxs-lookup"><span data-stu-id="dbca2-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="dbca2-113">**Переоформленный** набор записей и новая команда фигур должны использовать один и тот же объект \*\*[Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="dbca2-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


