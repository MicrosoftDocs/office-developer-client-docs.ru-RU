---
title: Коллекция членов (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: adc8ed771bcba6a4b6532b33b27980f8aab695c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289243"
---
# <a name="members-collection-ado-md"></a><span data-ttu-id="7ce82-102">Коллекция членов (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7ce82-102">Members collection (ADO MD)</span></span>


<span data-ttu-id="7ce82-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ce82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ce82-104">Содержит [объекты Member](member-object-ado-md.md) из уровня или положения вдоль оси.</span><span class="sxs-lookup"><span data-stu-id="7ce82-104">Contains the [Member](member-object-ado-md.md) objects from a level or a position along an axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ce82-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ce82-105">Remarks</span></span>

<span data-ttu-id="7ce82-106">Коллекция **Членов** используется для того, чтобы содержать следующие типы участников:</span><span class="sxs-lookup"><span data-stu-id="7ce82-106">A **Members** collection is used to contain the following types of members:</span></span>

  - <span data-ttu-id="7ce82-107">Участники, которые составляют уровень куба.</span><span class="sxs-lookup"><span data-stu-id="7ce82-107">The members that make up a level in a cube.</span></span> <span data-ttu-id="7ce82-108">Они содержатся в коллекции **Members** объекта [Level.](level-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="7ce82-108">These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="7ce82-109">Например, используя пример из [обзоров](overview-of-multidimensional-schemas-and-data.md)многомерных схем и данных, четыре члена уровня стран — Канада, США, Великобритания и Германия.</span><span class="sxs-lookup"><span data-stu-id="7ce82-109">For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.</span></span>

  - <span data-ttu-id="7ce82-110">Члены, которые являются детьми определенного члена в иерархии.</span><span class="sxs-lookup"><span data-stu-id="7ce82-110">The members that are the children of a specific member within a hierarchy.</span></span> <span data-ttu-id="7ce82-111">Эти члены возвращаются [свойством Children](children-property-ado-md.md) объекта **родительского** члена.</span><span class="sxs-lookup"><span data-stu-id="7ce82-111">These members are returned by the [Children](children-property-ado-md.md) property of the parent **Member** object.</span></span> <span data-ttu-id="7ce82-112">Например, опять же с использованием того же примера, два ребенка члена Канады являются Canada-East и Канада-Запад.</span><span class="sxs-lookup"><span data-stu-id="7ce82-112">For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</span></span>

  - <span data-ttu-id="7ce82-113">Участники, которые определяют определенное положение вдоль оси [ячейки.](cellset-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="7ce82-113">The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md).</span></span> <span data-ttu-id="7ce82-114">В качестве примера используется ячейки из ["Работа](working-with-multidimensional-data.md) с многомерными данными", два члена первой позиции на оси x являются Валентина и Сиэтл.</span><span class="sxs-lookup"><span data-stu-id="7ce82-114">Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle.</span></span> <span data-ttu-id="7ce82-115">Эти члены содержатся в коллекции **Members** объекта [Position.](position-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="7ce82-115">These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.</span></span>

<span data-ttu-id="7ce82-116">**Members** — это стандартная коллекция ADO.</span><span class="sxs-lookup"><span data-stu-id="7ce82-116">**Members** is a standard ADO collection.</span></span> <span data-ttu-id="7ce82-117">С помощью свойств и методов коллекции можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="7ce82-117">With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="7ce82-118">Получение количества объектов в коллекции с помощью свойства [Count.](count-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="7ce82-118">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="7ce82-119">Возвращаем объект из коллекции с свойством [Item по](item-property-ado.md) умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ce82-119">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="7ce82-120">Обновление объектов в коллекции от поставщика с помощью метода [Обновления.](refresh-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="7ce82-120">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

