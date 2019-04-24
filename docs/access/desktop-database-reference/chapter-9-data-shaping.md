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
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="3513f-102">Глава 9. Формирование данных</span><span class="sxs-lookup"><span data-stu-id="3513f-102">Chapter 9: Data shaping</span></span>

<span data-ttu-id="3513f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3513f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3513f-104">Средство *формирования данных* позволяет запрашивать источник данных и возвращать [набор записей](recordset-object-ado.md) , представляющий отношение "родитель-потомок" между двумя или несколькими логическими сущностями (иерархия).</span><span class="sxs-lookup"><span data-stu-id="3513f-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> 

<span data-ttu-id="3513f-105">Классический пример иерархического отношения — Customers and Orders.</span><span class="sxs-lookup"><span data-stu-id="3513f-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="3513f-106">Для каждого клиента в базе данных может быть не более одного заказа.</span><span class="sxs-lookup"><span data-stu-id="3513f-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="3513f-107">Обычный SQL предоставляет средства для получения данных с помощью синтаксиса JOIN, но это может оказаться неэффективным и неудобно, так как избыточные родительские данные повторяются в каждой записи, возвращенной для конкретной связи "родитель-потомок".</span><span class="sxs-lookup"><span data-stu-id="3513f-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="3513f-108">Формирование данных может связать одну родительскую запись в родительском **наборе** записей с несколькими дочерними записями в доЧернем **наборе записей**, избегая избыточности соединения.</span><span class="sxs-lookup"><span data-stu-id="3513f-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="3513f-109">Большинство пользователей находят модель программирования "родители — потомки" с использованием нескольких **наборов записей** , более естественной и удобную для работы, чем единственная модель соединения с **набором записей** .</span><span class="sxs-lookup"><span data-stu-id="3513f-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="3513f-110">Синтаксис формирования данных также предоставляет другие возможности.</span><span class="sxs-lookup"><span data-stu-id="3513f-110">The data shaping syntax also provides other capabilities.</span></span> <span data-ttu-id="3513f-111">Разработчики могут создавать новые объекты **Recordset** без базового источника данных, используя ключевое слово New для описания полей родительских и дочерних **наборов записей**.</span><span class="sxs-lookup"><span data-stu-id="3513f-111">Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**.</span></span> <span data-ttu-id="3513f-112">Новый объект **Recordset** может быть заполнен данными и сохраняемым.</span><span class="sxs-lookup"><span data-stu-id="3513f-112">The new **Recordset** object can be populated with data and persistently stored.</span></span> <span data-ttu-id="3513f-113">Разработчики также могут выполнять различные вычисления и статистические вычисления (например, SUM, AVG и MAX) для дочерних полей.</span><span class="sxs-lookup"><span data-stu-id="3513f-113">Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields.</span></span> <span data-ttu-id="3513f-114">С помощью формирования данных можно также создать родительский **набор** записей из доЧернего **набора** записей, группируя записи в дочернем элементе и размещая одну строку в родительской для каждой группы в дочернем элементе.</span><span class="sxs-lookup"><span data-stu-id="3513f-114">Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="3513f-115">Чтобы узнать больше об изменении данных, ознакомьтесь со следующими разделами:</span><span class="sxs-lookup"><span data-stu-id="3513f-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="3513f-116">Необходимые поставщики для формирования данных</span><span class="sxs-lookup"><span data-stu-id="3513f-116">Required providers for data shaping</span></span>](required-providers-for-data-shaping.md)
- [<span data-ttu-id="3513f-117">Предложение Compute команды Shape</span><span class="sxs-lookup"><span data-stu-id="3513f-117">Shape Compute clause</span></span>](shape-compute-clause.md)
- [<span data-ttu-id="3513f-118">Создание иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="3513f-118">Fabricating hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)
- [<span data-ttu-id="3513f-119">Доступ к строкам в иерархическом наборе записей</span><span class="sxs-lookup"><span data-stu-id="3513f-119">Accessing rows in a hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)
- [<span data-ttu-id="3513f-120">Формальная грамматика фигур</span><span class="sxs-lookup"><span data-stu-id="3513f-120">Formal shape grammar</span></span>](formal-shape-grammar.md)
- [<span data-ttu-id="3513f-121">Visual Basic for Applications functions</span><span class="sxs-lookup"><span data-stu-id="3513f-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)
- [<span data-ttu-id="3513f-122">Предложение Append для фигуры (ADO)</span><span class="sxs-lookup"><span data-stu-id="3513f-122">Shape Append clause (ADO)</span></span>](shape-append-clause.md)
- [<span data-ttu-id="3513f-123">Формирование данных (ADO)</span><span class="sxs-lookup"><span data-stu-id="3513f-123">Data shaping (ADO)</span></span>](data-shaping.md)
- [<span data-ttu-id="3513f-124">Общие команды фигур (ADO)</span><span class="sxs-lookup"><span data-stu-id="3513f-124">Shape commands in general (ADO)</span></span>](shape-commands-in-general.md)

