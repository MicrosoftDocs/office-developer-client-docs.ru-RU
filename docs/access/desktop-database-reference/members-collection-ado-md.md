---
title: Коллекция Members (ADO MD)
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
# <a name="members-collection-ado-md"></a><span data-ttu-id="ea5c6-102">Коллекция Members (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ea5c6-102">Members collection (ADO MD)</span></span>


<span data-ttu-id="ea5c6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea5c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ea5c6-104">Содержит объекты [member](member-object-ado-md.md) на уровне или позиции вдоль оси.</span><span class="sxs-lookup"><span data-stu-id="ea5c6-104">Contains the [Member](member-object-ado-md.md) objects from a level or a position along an axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea5c6-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea5c6-105">Remarks</span></span>

<span data-ttu-id="ea5c6-106">Коллекция **Members** используется для хранения следующих типов элементов:</span><span class="sxs-lookup"><span data-stu-id="ea5c6-106">A **Members** collection is used to contain the following types of members:</span></span>

  - <span data-ttu-id="ea5c6-107">Элементы, составляющие уровень в Кубе.</span><span class="sxs-lookup"><span data-stu-id="ea5c6-107">The members that make up a level in a cube.</span></span> <span data-ttu-id="ea5c6-108">Они включены в коллекцию **Members** объекта [Level](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="ea5c6-108">These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="ea5c6-109">Например, используя пример из [обзора многомерных схем и данных](overview-of-multidimensional-schemas-and-data.md), четыре члена уровня стран — Канады, США, Великобритании и Германии.</span><span class="sxs-lookup"><span data-stu-id="ea5c6-109">For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.</span></span>

  - <span data-ttu-id="ea5c6-110">Элементы, которые являются дочерними по отношению к определенному члену в иерархии.</span><span class="sxs-lookup"><span data-stu-id="ea5c6-110">The members that are the children of a specific member within a hierarchy.</span></span> <span data-ttu-id="ea5c6-111">Эти элементы возвращаются свойством [Children](children-property-ado-md.md) родительского объекта **member** .</span><span class="sxs-lookup"><span data-stu-id="ea5c6-111">These members are returned by the [Children](children-property-ado-md.md) property of the parent **Member** object.</span></span> <span data-ttu-id="ea5c6-112">Например, при использовании того же примера двумя дочерними элементами члена Канады являются Канада — Канада и Канада (запад).</span><span class="sxs-lookup"><span data-stu-id="ea5c6-112">For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</span></span>

  - <span data-ttu-id="ea5c6-113">Элементы, определяющие определенную позицию вдоль оси набора [ячеек](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ea5c6-113">The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md).</span></span> <span data-ttu-id="ea5c6-114">Используя набор ячеек для [работы с многомерными данными](working-with-multidimensional-data.md) в качестве примера, два элемента первой позиции на оси x — любимая и Сиэтл.</span><span class="sxs-lookup"><span data-stu-id="ea5c6-114">Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle.</span></span> <span data-ttu-id="ea5c6-115">Эти элементы входят в коллекцию **Members** объекта [position](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="ea5c6-115">These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.</span></span>

<span data-ttu-id="ea5c6-116">**Members** — это стандартная коллекция ADO.</span><span class="sxs-lookup"><span data-stu-id="ea5c6-116">**Members** is a standard ADO collection.</span></span> <span data-ttu-id="ea5c6-117">С помощью свойств и методов коллекции можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ea5c6-117">With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="ea5c6-118">Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ea5c6-118">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="ea5c6-119">Возвращает объект из коллекции со свойством [Item](item-property-ado.md) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea5c6-119">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="ea5c6-120">Обновление объектов в коллекции от поставщика с помощью метода [Refresh](refresh-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ea5c6-120">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

