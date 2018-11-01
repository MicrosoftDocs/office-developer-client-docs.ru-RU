---
title: Глава 9. Формирование данных
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 988766f71fd57505693683d54a15b13409ae6960
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875877"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="fb5fe-102">Глава 9. Формирование данных</span><span class="sxs-lookup"><span data-stu-id="fb5fe-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="fb5fe-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb5fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb5fe-104">*Формирование данных* предоставляет способ для запроса источника данных и возврата [набора записей](recordset-object-ado.md) , представляющий отношение родитель потомок между двумя или более логические сущности (иерархии).</span><span class="sxs-lookup"><span data-stu-id="fb5fe-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> <span data-ttu-id="fb5fe-105">Классический пример иерархической связи — клиентов и заказы.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="fb5fe-106">Для каждого клиента в базе данных может быть ноль или больше заказов.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="fb5fe-107">Регулярные SQL предоставляет средства извлечения данных, с помощью синтаксиса, но это может быть неэффективны и громоздким, так как избыточных родительских данных повторяется в каждой записи возвращаются для связь с заданным родитель потомок.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="fb5fe-108">Формирование данных можно связать один родительской записи в родительском **записей** несколько дочерних записей в дочерних **записей**, избегая избыточность соединения.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="fb5fe-109">Большинство пользователей поиск родитель потомок нескольких **записей** модель программирования более естественный и более удобен для работы с более одной модели ОБЪЕДИНЕНИЯ **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="fb5fe-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="fb5fe-110">Также формирования синтаксис данных предоставляет другие возможности.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-110">The data shaping syntax also provides other capabilities.</span></span> <span data-ttu-id="fb5fe-111">Разработчики могут создавать новые объекты **набора записей** без источника данных с помощью ключевого слова NEW для описания полей родительских и дочерних **наборов записей**.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-111">Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**.</span></span> <span data-ttu-id="fb5fe-112">Новый объект **набора записей** можно заполненный данными и постоянно хранятся.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-112">The new **Recordset** object can be populated with data and persistently stored.</span></span> <span data-ttu-id="fb5fe-113">Разработчики также можно выполнить различные вычисления или aggregations (например, сумм, AVG и максимальное число) на подчиненные поля.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-113">Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields.</span></span> <span data-ttu-id="fb5fe-114">Формирование данных также можно создавать родительского **набора записей** из дочерних **записей** группировки записей в дочернем и поместить одну строку в родительской для каждой группы в дочернем.</span><span class="sxs-lookup"><span data-stu-id="fb5fe-114">Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="fb5fe-115">В следующих разделах для получения дополнительных сведений о формирования данных:</span><span class="sxs-lookup"><span data-stu-id="fb5fe-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="fb5fe-116">Необходимые поставщики для формирования данных</span><span class="sxs-lookup"><span data-stu-id="fb5fe-116">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

- [<span data-ttu-id="fb5fe-117">Предложение вычисления фигур</span><span class="sxs-lookup"><span data-stu-id="fb5fe-117">Shape Compute Clause</span></span>](shape-compute-clause.md)

- [<span data-ttu-id="fb5fe-118">Создание иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="fb5fe-118">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

- [<span data-ttu-id="fb5fe-119">Доступ к строкам в иерархическом наборе записей</span><span class="sxs-lookup"><span data-stu-id="fb5fe-119">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

- [<span data-ttu-id="fb5fe-120">Формальная грамматика фигур</span><span class="sxs-lookup"><span data-stu-id="fb5fe-120">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

- [<span data-ttu-id="fb5fe-121">Функции Visual Basic для приложений</span><span class="sxs-lookup"><span data-stu-id="fb5fe-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)

- [<span data-ttu-id="fb5fe-122">Shape Append Clause (ADO)</span><span class="sxs-lookup"><span data-stu-id="fb5fe-122">Shape Append Clause (ADO)</span></span>](shape-append-clause.md)

- [<span data-ttu-id="fb5fe-123">Формирования (ADO) данных</span><span class="sxs-lookup"><span data-stu-id="fb5fe-123">Data Shaping (ADO)</span></span>](data-shaping.md)

- [<span data-ttu-id="fb5fe-124">Shape Commands in General (ADO)</span><span class="sxs-lookup"><span data-stu-id="fb5fe-124">Shape Commands in General (ADO)</span></span>](shape-commands-in-general.md)

