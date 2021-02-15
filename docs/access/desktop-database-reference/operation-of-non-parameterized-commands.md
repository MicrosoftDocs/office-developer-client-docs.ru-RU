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
# <a name="operation-of-non-parameterized-commands"></a><span data-ttu-id="2f792-102">Выполнение непараметризованных команд</span><span class="sxs-lookup"><span data-stu-id="2f792-102">Operation of non-parameterized commands</span></span>


<span data-ttu-id="2f792-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f792-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f792-104">Для команд без параметров выполняются все команды поставщика,  а во время выполнения команды создаются записи.</span><span class="sxs-lookup"><span data-stu-id="2f792-104">For non-parameterized commands, all of the provider commands are executed and the **Recordsets** are created during command execution.</span></span> <span data-ttu-id="2f792-105">Если команда выполняется синхронно, все  записи будут полностью заполнены.</span><span class="sxs-lookup"><span data-stu-id="2f792-105">If the command is executed synchronously, all of the **Recordsets** will be fully populated.</span></span> <span data-ttu-id="2f792-106">Если выбран асинхронный режим заполнения, заполнение  записей будет зависеть от режима заполнения и размера **записей.**</span><span class="sxs-lookup"><span data-stu-id="2f792-106">If an asynchronous population mode was selected, the populated state of the **Recordsets** will depend on the population mode and the size of the **Recordsets**.</span></span>

<span data-ttu-id="2f792-107">Например, *родительская* команда может  вернуть набор записей клиентов для компании из  таблицы Customers, а потомок может вернуть набор заказов **recordset** для всех клиентов из таблицы "Заказы".</span><span class="sxs-lookup"><span data-stu-id="2f792-107">For example, the *parent-command* could return a **Recordset** of customers for a company from a Customers table, and the *child-command* could return a **Recordset** of orders for all customers from an Orders table.</span></span>

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

<span data-ttu-id="2f792-108">Для непараметровизированных отношений родительский-потомок каждый родительский и потомок объекта **Recordset** должен иметь общий столбец, чтобы связать их.</span><span class="sxs-lookup"><span data-stu-id="2f792-108">For non-parameterized parent-child relationships, each parent and child **Recordset** object must have a column in common to associate them.</span></span> <span data-ttu-id="2f792-109">Столбцы именуются в предложении RELATE, *сначала в родительском* столбце, а затем *в столбце child-column.*</span><span class="sxs-lookup"><span data-stu-id="2f792-109">The columns are named in the RELATE clause, *parent-column* first and then *child-column*.</span></span> <span data-ttu-id="2f792-110">У столбцов могут быть разные имена в соответствующих объектах **Recordset,** но они должны ссылаться на те же сведения, чтобы указать осмысленное отношение.</span><span class="sxs-lookup"><span data-stu-id="2f792-110">The columns may have different names in their respective **Recordset** objects but must refer to the same information in order to specify a meaningful relation.</span></span> <span data-ttu-id="2f792-111">Например, **объекты Customers** и **Orders** **Recordset** могут иметь поле customerID.</span><span class="sxs-lookup"><span data-stu-id="2f792-111">For example, the **Customers** and **Orders** **Recordset** objects could both have a customerID field.</span></span> <span data-ttu-id="2f792-112">Поскольку членство в  этом наборе записей определяется командой поставщика, он может содержать потерянные строки. </span><span class="sxs-lookup"><span data-stu-id="2f792-112">Because the membership of the child **Recordset** is determined by the provider command, it is possible for the child **Recordset** to contain orphaned rows.</span></span> <span data-ttu-id="2f792-113">Эти потерянные строки недоступны без дальнейшего изменения их области.</span><span class="sxs-lookup"><span data-stu-id="2f792-113">These orphaned rows are inaccessible without further reshaping.</span></span>

<span data-ttu-id="2f792-114">Формирование данных привносим столбец главы в родительский **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="2f792-114">Data shaping appends a chapter column to the parent **Recordset**.</span></span> <span data-ttu-id="2f792-115">Значения в столбце главы являются ссылками на строки в наборе записей, которые удовлетворяют предложению RELATE.</span><span class="sxs-lookup"><span data-stu-id="2f792-115">The values in the chapter column are references to rows in the child **Recordset**, which satisfy the RELATE clause.</span></span> <span data-ttu-id="2f792-116">То есть в родительском  столбце заданной родительской строки находится то же значение, что и в столбце *child* всех строк в родительской главе.</span><span class="sxs-lookup"><span data-stu-id="2f792-116">That is, the same value is in the *parent-column* of a given parent row as is in the *child-column* of all the rows of the chapter child.</span></span> <span data-ttu-id="2f792-117">Если в одном предложении RELATE используется несколько предложений TO, они неявно объединяются с помощью оператора AND.</span><span class="sxs-lookup"><span data-stu-id="2f792-117">When multiple TO clauses are used in the same RELATE clause, they are implicitly combined using an AND operator.</span></span> <span data-ttu-id="2f792-118">Если родительские столбцы в предложении relate не составляют ключ к родительскому набору записей, одна родительская строка может иметь несколько родительских строк.</span><span class="sxs-lookup"><span data-stu-id="2f792-118">If the parent columns in the relate clause do not constitute a key to the parent **Recordset**, a single child row may have multiple parent rows.</span></span>

<span data-ttu-id="2f792-119">При доступе к ссылке в столбце главы ADO автоматически получает набор **записей,** представленный ссылкой.</span><span class="sxs-lookup"><span data-stu-id="2f792-119">When you access the reference in the chapter column, ADO automatically retrieves the **Recordset** represented by the reference.</span></span> <span data-ttu-id="2f792-120">Обратите внимание, что в команде без параметров, хотя был извлечен весь набор записей, в главе представлено только подмножество строк. </span><span class="sxs-lookup"><span data-stu-id="2f792-120">Note that in a non-parameterized command, although the entire child **Recordset** has been retrieved, the chapter only presents a subset of rows.</span></span>

<span data-ttu-id="2f792-121">Если в столбце с приложением нет псевдонима *главы,* для него автоматически создается имя.</span><span class="sxs-lookup"><span data-stu-id="2f792-121">If the appended column has no *chapter-alias*, a name will be generated for it automatically.</span></span> <span data-ttu-id="2f792-122">Объект [Field](field-object-ado.md) для столбца будет примещаться к коллекции [Fields](fields-collection-ado.md) объекта **Recordset,** а его типом данных будет **adChapter.**</span><span class="sxs-lookup"><span data-stu-id="2f792-122">A [Field](field-object-ado.md) object for the column will be appended to the **Recordset** object's [Fields](fields-collection-ado.md) collection, and its data type will be **adChapter**.</span></span>

<span data-ttu-id="2f792-123">Сведения о навигации по иерархическому набору **записей** см. в подсети "Доступ к [строкам в иерархическом наборе записей".](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="2f792-123">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

