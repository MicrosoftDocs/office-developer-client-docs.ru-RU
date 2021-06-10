---
title: Выполнение непараметризованных команд
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 720cbaf346b64d4d23b1e3314b06ba941e78b700
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288268"
---
# <a name="operation-of-non-parameterized-commands"></a><span data-ttu-id="08e9a-102">Выполнение непараметризованных команд</span><span class="sxs-lookup"><span data-stu-id="08e9a-102">Operation of non-parameterized commands</span></span>


<span data-ttu-id="08e9a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08e9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08e9a-104">Для непараметровизированных команд выполняются все команды поставщика и  создаются записи во время выполнения команд.</span><span class="sxs-lookup"><span data-stu-id="08e9a-104">For non-parameterized commands, all of the provider commands are executed and the **Recordsets** are created during command execution.</span></span> <span data-ttu-id="08e9a-105">Если команда выполняется синхронно, все  записи будут заполнены полностью.</span><span class="sxs-lookup"><span data-stu-id="08e9a-105">If the command is executed synchronously, all of the **Recordsets** will be fully populated.</span></span> <span data-ttu-id="08e9a-106">Если выбран асинхронный режим популяции, то  состояние населенных пунктов записей будет зависеть от режима популяции и размера **записей.**</span><span class="sxs-lookup"><span data-stu-id="08e9a-106">If an asynchronous population mode was selected, the populated state of the **Recordsets** will depend on the population mode and the size of the **Recordsets**.</span></span>

<span data-ttu-id="08e9a-107">Например,   *родительская* команда может возвращать набор записей клиентов для компании из  таблицы Клиенты, а детская команда может возвращать набор заказов для всех клиентов из таблицы Заказов.</span><span class="sxs-lookup"><span data-stu-id="08e9a-107">For example, the *parent-command* could return a **Recordset** of customers for a company from a Customers table, and the *child-command* could return a **Recordset** of orders for all customers from an Orders table.</span></span>

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

<span data-ttu-id="08e9a-108">Для непараметровных отношений родителей и детей каждый объект **recordset** для родителей и детей должен иметь общий столбец, чтобы связать их.</span><span class="sxs-lookup"><span data-stu-id="08e9a-108">For non-parameterized parent-child relationships, each parent and child **Recordset** object must have a column in common to associate them.</span></span> <span data-ttu-id="08e9a-109">Столбцы называются в пункте RELATE, сначала в *родительском* столбце, а затем *в столбце child-column.*</span><span class="sxs-lookup"><span data-stu-id="08e9a-109">The columns are named in the RELATE clause, *parent-column* first and then *child-column*.</span></span> <span data-ttu-id="08e9a-110">Столбцы могут иметь разные имена в соответствующих объектах **Recordset,** но должны ссылаться на ту же информацию, чтобы указать значимое отношение.</span><span class="sxs-lookup"><span data-stu-id="08e9a-110">The columns may have different names in their respective **Recordset** objects but must refer to the same information in order to specify a meaningful relation.</span></span> <span data-ttu-id="08e9a-111">Например, **объекты Recordset Клиентов** и **Заказов**  могут иметь поле customerID.</span><span class="sxs-lookup"><span data-stu-id="08e9a-111">For example, the **Customers** and **Orders** **Recordset** objects could both have a customerID field.</span></span> <span data-ttu-id="08e9a-112">Так как членство  в наборе записей ребенка определяется командой  поставщика, ребенок может содержать осиротевших строк.</span><span class="sxs-lookup"><span data-stu-id="08e9a-112">Because the membership of the child **Recordset** is determined by the provider command, it is possible for the child **Recordset** to contain orphaned rows.</span></span> <span data-ttu-id="08e9a-113">Эти осиротевших строки недоступны без дальнейшего изменения.</span><span class="sxs-lookup"><span data-stu-id="08e9a-113">These orphaned rows are inaccessible without further reshaping.</span></span>

<span data-ttu-id="08e9a-114">Формирование данных придает столбец главы родительскому **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="08e9a-114">Data shaping appends a chapter column to the parent **Recordset**.</span></span> <span data-ttu-id="08e9a-115">Значения в столбце главы — это ссылки на строки в наборе записей **ребенка,** удовлетворяющие пункту RELATE.</span><span class="sxs-lookup"><span data-stu-id="08e9a-115">The values in the chapter column are references to rows in the child **Recordset**, which satisfy the RELATE clause.</span></span> <span data-ttu-id="08e9a-116">То есть в родительском  столбце родительской строки то же  значение, что и в детской колонке всех строк ребенка главы.</span><span class="sxs-lookup"><span data-stu-id="08e9a-116">That is, the same value is in the *parent-column* of a given parent row as is in the *child-column* of all the rows of the chapter child.</span></span> <span data-ttu-id="08e9a-117">При использовании нескольких пунктов TO в одном и том же пункте RELATE они неявно объединяются с помощью оператора AND.</span><span class="sxs-lookup"><span data-stu-id="08e9a-117">When multiple TO clauses are used in the same RELATE clause, they are implicitly combined using an AND operator.</span></span> <span data-ttu-id="08e9a-118">Если родительские столбцы в статье relate не являются ключом к родительскому набору **записей,** одна детская строка может иметь несколько родительских строк.</span><span class="sxs-lookup"><span data-stu-id="08e9a-118">If the parent columns in the relate clause do not constitute a key to the parent **Recordset**, a single child row may have multiple parent rows.</span></span>

<span data-ttu-id="08e9a-119">При доступе к ссылке в столбце главы ADO автоматически получает **набор записей,** представленный ссылкой.</span><span class="sxs-lookup"><span data-stu-id="08e9a-119">When you access the reference in the chapter column, ADO automatically retrieves the **Recordset** represented by the reference.</span></span> <span data-ttu-id="08e9a-120">Обратите внимание, что в непараметровной команде, хотя весь набор записей ребенка был извлечен, в главе представлен только подмножество строк. </span><span class="sxs-lookup"><span data-stu-id="08e9a-120">Note that in a non-parameterized command, although the entire child **Recordset** has been retrieved, the chapter only presents a subset of rows.</span></span>

<span data-ttu-id="08e9a-121">Если в приложении столбца нет *псевдонима* главы, для него будет автоматически сгенерировано имя.</span><span class="sxs-lookup"><span data-stu-id="08e9a-121">If the appended column has no *chapter-alias*, a name will be generated for it automatically.</span></span> <span data-ttu-id="08e9a-122">Объект [Field](field-object-ado.md) для столбца будет примещаться к [](fields-collection-ado.md) коллекции Полей объекта **Recordset,** а его тип данных **будет adChapter**.</span><span class="sxs-lookup"><span data-stu-id="08e9a-122">A [Field](field-object-ado.md) object for the column will be appended to the **Recordset** object's [Fields](fields-collection-ado.md) collection, and its data type will be **adChapter**.</span></span>

<span data-ttu-id="08e9a-123">Сведения о навигации по иерархическому **набору записей** см. в сайте [Accessing Rows in a Hierarchical Recordset.](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="08e9a-123">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

