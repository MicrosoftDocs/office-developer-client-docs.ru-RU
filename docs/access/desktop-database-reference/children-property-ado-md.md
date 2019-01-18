---
title: Свойство Children (ADO MD)
TOCTitle: Children property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 27d69e760b65a917270b0851743c108692c601e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717827"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="3a711-102">Свойство Children (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3a711-102">Children property (ADO MD)</span></span>


<span data-ttu-id="3a711-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a711-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a711-104">Возвращает коллекцию [членов](members-collection-ado-md.md) , для которого текущий [элемент](member-object-ado-md.md) является родительской в иерархии.</span><span class="sxs-lookup"><span data-stu-id="3a711-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="3a711-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3a711-105">Return values</span></span>

<span data-ttu-id="3a711-106">Возвращает коллекцию **элементов** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3a711-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a711-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a711-107">Remarks</span></span>

<span data-ttu-id="3a711-108">**В свойстве** содержит коллекцию **Members** , для которого текущий **член** является иерархической родительского.</span><span class="sxs-lookup"><span data-stu-id="3a711-108">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent.</span></span> <span data-ttu-id="3a711-109">Конечные объекты уровень **член** не содержат дочерние членов в коллекции **элементов** .</span><span class="sxs-lookup"><span data-stu-id="3a711-109">Leaf level **Member** objects have no child members in the **Members** collection.</span></span> <span data-ttu-id="3a711-110">Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="3a711-110">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="3a711-111">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="3a711-111">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

