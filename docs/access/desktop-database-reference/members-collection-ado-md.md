---
title: Members Collection (ADO MD)
TOCTitle: Members Collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd467335102351fc0412b5c77685d6434b0c20a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481489"
---
# <a name="members-collection-ado-md"></a><span data-ttu-id="238ab-102">Members Collection (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="238ab-102">Members Collection (ADO MD)</span></span>


<span data-ttu-id="238ab-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="238ab-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="238ab-104">Содержит объекты [члена](member-object-ado-md.md) с уровнем или положение оси.</span><span class="sxs-lookup"><span data-stu-id="238ab-104">Contains the [Member](member-object-ado-md.md) objects from a level or a position along an axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="238ab-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="238ab-105">Remarks</span></span>

<span data-ttu-id="238ab-106">**Члены** коллекции используется содержат следующие типы элементов:</span><span class="sxs-lookup"><span data-stu-id="238ab-106">A **Members** collection is used to contain the following types of members:</span></span>

  - <span data-ttu-id="238ab-107">Члены, которые составляют уровень в кубе.</span><span class="sxs-lookup"><span data-stu-id="238ab-107">The members that make up a level in a cube.</span></span> <span data-ttu-id="238ab-108">Эти содержащихся в коллекции **элементы** объекта [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="238ab-108">These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="238ab-109">Например с помощью образца из [Обзор многомерные схемы и данных](overview-of-multidimensional-schemas-and-data.md), четырех элементов уровня странах, Канада, США, Великобритании и Германии.</span><span class="sxs-lookup"><span data-stu-id="238ab-109">For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.</span></span>

  - <span data-ttu-id="238ab-110">Члены, которые являются дочерними конкретный элемент в иерархии.</span><span class="sxs-lookup"><span data-stu-id="238ab-110">The members that are the children of a specific member within a hierarchy.</span></span> <span data-ttu-id="238ab-111">Эти элементы возвращаются свойством [потомки](children-property-ado-md.md) **члена** родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="238ab-111">These members are returned by the [Children](children-property-ado-md.md) property of the parent **Member** object.</span></span> <span data-ttu-id="238ab-112">Например два дочерних элементов элемента Канада еще раз с помощью же пример, Канада-Восток и запад Канада.</span><span class="sxs-lookup"><span data-stu-id="238ab-112">For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</span></span>

  - <span data-ttu-id="238ab-113">Элементы, определяющие определенного положения оси набора [ячеек](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="238ab-113">The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md).</span></span> <span data-ttu-id="238ab-114">Использование ячеек от [работы с многомерные данные](working-with-multidimensional-data.md) в качестве примера, два членов первого положение на оси x являются любимая и Seattle.</span><span class="sxs-lookup"><span data-stu-id="238ab-114">Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle.</span></span> <span data-ttu-id="238ab-115">Эти элементы содержащихся в коллекции **элементы** объекта [положение](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="238ab-115">These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.</span></span>

<span data-ttu-id="238ab-116">**Члены** — это обычная коллекция ADO.</span><span class="sxs-lookup"><span data-stu-id="238ab-116">**Members** is a standard ADO collection.</span></span> <span data-ttu-id="238ab-117">С помощью свойства и методы коллекции сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="238ab-117">With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="238ab-118">Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="238ab-118">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="238ab-119">Возвращает объект из коллекции с помощью свойства [элемента](item-property-ado.md) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="238ab-119">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="238ab-120">Обновление объектов в коллекции от поставщика с помощью метода [обновления](refresh-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="238ab-120">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

