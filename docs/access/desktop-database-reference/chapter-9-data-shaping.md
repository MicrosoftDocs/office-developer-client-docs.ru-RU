---
title: Глава 9. Формирование данных
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296425"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="9e187-102">Глава 9. Формирование данных</span><span class="sxs-lookup"><span data-stu-id="9e187-102">Chapter 9: Data shaping</span></span>

<span data-ttu-id="9e187-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e187-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e187-104">*Формирование данных позволяет* запрашивать источник данных и возвращать [набор записей,](recordset-object-ado.md) представляюющий связь между двумя или более логическими сущностями (иерархией).</span><span class="sxs-lookup"><span data-stu-id="9e187-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> 

<span data-ttu-id="9e187-105">Классическим примером иерархических отношений являются клиенты и заказы.</span><span class="sxs-lookup"><span data-stu-id="9e187-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="9e187-106">Для каждого клиента в базе данных может быть ноль или больше заказов.</span><span class="sxs-lookup"><span data-stu-id="9e187-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="9e187-107">Регулярные SQL предоставляют средства для сбора данных с помощью синтаксиса JOIN, но это может быть неэффективным и громоздким, так как избыточные родительские данные повторяются в каждой записи, возвращаемой для данного отношения между родителем и ребенком.</span><span class="sxs-lookup"><span data-stu-id="9e187-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="9e187-108">Формирование данных может связать запись одного  родителя в родительском наборе записей с несколькими записями ребенка в детском наборе записей, избегая избыточности JOIN.</span><span class="sxs-lookup"><span data-stu-id="9e187-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="9e187-109">Большинство людей считают модель программирования с несколькими **записями** родительского ребенка более естественной и простой в работе, чем с одной моделью **Join Recordset.**</span><span class="sxs-lookup"><span data-stu-id="9e187-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="9e187-110">Синтаксис формирования данных также предоставляет другие возможности.</span><span class="sxs-lookup"><span data-stu-id="9e187-110">The data shaping syntax also provides other capabilities.</span></span> <span data-ttu-id="9e187-111">Разработчики могут создавать новые объекты **Recordset** без источника данных, используя ключевое слово NEW для описания полей родительских и детских **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="9e187-111">Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**.</span></span> <span data-ttu-id="9e187-112">Новый объект **Recordset** может быть заполнен данными и постоянно храниться.</span><span class="sxs-lookup"><span data-stu-id="9e187-112">The new **Recordset** object can be populated with data and persistently stored.</span></span> <span data-ttu-id="9e187-113">Разработчики также могут выполнять различные вычисления или агрегации (например, SUM, AVG и MAX) на детских полях.</span><span class="sxs-lookup"><span data-stu-id="9e187-113">Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields.</span></span> <span data-ttu-id="9e187-114">Формирование данных также может создать родительский набор записей из детского **recordset** путем группировки записей в ребенке и размещения одной строки в родительской группе для каждой группы в ребенке. </span><span class="sxs-lookup"><span data-stu-id="9e187-114">Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="9e187-115">Дополнительные сведения о формировании данных см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="9e187-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="9e187-116">Необходимые поставщики для формирования данных</span><span class="sxs-lookup"><span data-stu-id="9e187-116">Required providers for data shaping</span></span>](required-providers-for-data-shaping.md)
- [<span data-ttu-id="9e187-117">Предложение Compute команды Shape</span><span class="sxs-lookup"><span data-stu-id="9e187-117">Shape Compute clause</span></span>](shape-compute-clause.md)
- [<span data-ttu-id="9e187-118">Создание иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="9e187-118">Fabricating hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)
- [<span data-ttu-id="9e187-119">Доступ к строкам в иерархическом наборе записей</span><span class="sxs-lookup"><span data-stu-id="9e187-119">Accessing rows in a hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)
- [<span data-ttu-id="9e187-120">Формальная грамматика фигур</span><span class="sxs-lookup"><span data-stu-id="9e187-120">Formal shape grammar</span></span>](formal-shape-grammar.md)
- [<span data-ttu-id="9e187-121">Visual Basic for Applications functions</span><span class="sxs-lookup"><span data-stu-id="9e187-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)
- [<span data-ttu-id="9e187-122">Положение "Форма приложения" (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e187-122">Shape Append clause (ADO)</span></span>](shape-append-clause.md)
- [<span data-ttu-id="9e187-123">Формирование данных (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e187-123">Data shaping (ADO)</span></span>](data-shaping.md)
- [<span data-ttu-id="9e187-124">Команды фигуры в целом (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e187-124">Shape commands in general (ADO)</span></span>](shape-commands-in-general.md)

