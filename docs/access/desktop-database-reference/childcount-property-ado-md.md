---
title: Свойство ChildCount (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f8e0fc98d7868eb5462bd7d8714e1a8eda1cfcf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296383"
---
# <a name="childcount-property-ado-md"></a><span data-ttu-id="55097-102">Свойство ChildCount (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="55097-102">ChildCount property (ADO MD)</span></span>


<span data-ttu-id="55097-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55097-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55097-104">Указывает количество элементов, для которых текущий объект [member](member-object-ado-md.md) является родительским в иерархии.</span><span class="sxs-lookup"><span data-stu-id="55097-104">Indicates the number of members for which the current [Member](member-object-ado-md.md) object is the parent in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="55097-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="55097-105">Return values</span></span>

<span data-ttu-id="55097-106">Возвращает целое значение **типа Long** и доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="55097-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="55097-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="55097-107">Remarks</span></span>

<span data-ttu-id="55097-108">Используйте свойство **ChildCount** для возврата оценки количества дочерних элементов, которые содержит **элемент** .</span><span class="sxs-lookup"><span data-stu-id="55097-108">Use the **ChildCount** property to return an estimate of how many children a **Member** has.</span></span> <span data-ttu-id="55097-109">Фактические дочерние элементы **элемента** могут быть возвращены свойством [Children](children-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="55097-109">The actual children of a **Member** can be returned by the [Children](children-property-ado-md.md) property.</span></span>

<span data-ttu-id="55097-110">Для объектов **member** из объекта [position](position-object-ado-md.md) максимальное возвращаемое значение равно 65536.</span><span class="sxs-lookup"><span data-stu-id="55097-110">For **Member** objects from a [Position](position-object-ado-md.md) object, the maximum number returned is 65536.</span></span> <span data-ttu-id="55097-111">Если фактическое число потомков превышает 65536, возвращаемое значение по-прежнему будет 65536.</span><span class="sxs-lookup"><span data-stu-id="55097-111">If the actual number of children exceeds 65536, the value returned will still be 65536.</span></span> <span data-ttu-id="55097-112">Таким образом, приложение должно интерпретировать **ChildCount** из 65536 как равное или более 65536 потомков.</span><span class="sxs-lookup"><span data-stu-id="55097-112">Therefore, the application should interpret a **ChildCount** of 65536 as equal to or greater than 65536 children.</span></span>

<span data-ttu-id="55097-113">Для объектов **member** из объекта [Level](level-object-ado-md.md) используйте свойство [Count](count-property-ado.md) Collections коллекции ADO для коллекции **Children** , чтобы определить точное количество дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="55097-113">For **Member** objects from a [Level](level-object-ado-md.md) object, use the ADO collection [Count](count-property-ado.md) property on the **Children** collection to determine the exact number of children.</span></span> <span data-ttu-id="55097-114">Определение точного числа дочерних элементов может быть медленным, если количество дочерних элементов в коллекции велико.</span><span class="sxs-lookup"><span data-stu-id="55097-114">Determining the exact number of children may be slow if the number of children in the collection is large.</span></span>

