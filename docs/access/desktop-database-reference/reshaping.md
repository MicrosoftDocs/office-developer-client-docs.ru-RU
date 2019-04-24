---
title: Изменение формы (Справочник по базам данных Access на компьютере)
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
# <a name="reshaping"></a><span data-ttu-id="6fda6-102">Изменение формы</span><span class="sxs-lookup"><span data-stu-id="6fda6-102">Reshaping</span></span>

<span data-ttu-id="6fda6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fda6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fda6-104">Для объекта **Recordset** , созданного с помощью предложения команды Shape, может быть назначен *псевдоним* (как правило, с помощью ключевого слова as).</span><span class="sxs-lookup"><span data-stu-id="6fda6-104">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword).</span></span> <span data-ttu-id="6fda6-105">Псевдоним для объекта **Recordset** в форме может быть указан в полностью другой команде.</span><span class="sxs-lookup"><span data-stu-id="6fda6-105">The alias of a shaped **Recordset** can be referenced in an entirely different command.</span></span> <span data-ttu-id="6fda6-106">То есть вы можете повторно использовать или *изменить форму*ранее созданного **набора записей** в новой команде Shape.</span><span class="sxs-lookup"><span data-stu-id="6fda6-106">That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command.</span></span> <span data-ttu-id="6fda6-107">Чтобы обеспечить поддержку этой функции, ADO предоставляет свойство, а также перерисовку [имени](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6fda6-107">To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="6fda6-108">Изменение формы состоит из двух основных функций.</span><span class="sxs-lookup"><span data-stu-id="6fda6-108">Reshaping has two main functions.</span></span> <span data-ttu-id="6fda6-109">Первый — связать существующий **набор записей** с новым родительским набором **записей**.</span><span class="sxs-lookup"><span data-stu-id="6fda6-109">The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="6fda6-110">Пример</span><span class="sxs-lookup"><span data-stu-id="6fda6-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="6fda6-111">Вторая функция заключается в включении доступа, не разбитого на разделы, \*\*\*\* в существующие дочерние объекты `"SHAPE <recordset reshape name>"`Recordset с помощью синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="6fda6-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="6fda6-112">Невозможно добавить столбцы к существующему **набору записей**, изменить форму параметризованного **набора записей** или объектов **Recordset** в любом промежуточном предложении COMPUTE или выполнить операции агрегированИя для любого потомка объекта **Recordset** из \*\* \*\*Перерисовка объекта Recordset.</span><span class="sxs-lookup"><span data-stu-id="6fda6-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="6fda6-113">Объект **Recordset** , для которого выполняется изменение формы, и команда Новая фигура должна использовать один и тот же объект[подключения](connection-object-ado.md) \* \*.</span><span class="sxs-lookup"><span data-stu-id="6fda6-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


