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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296369"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="b6694-102">Свойство Children (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="b6694-102">Children property (ADO MD)</span></span>


<span data-ttu-id="b6694-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6694-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6694-104">Возвращает коллекцию [Members,](members-collection-ado-md.md) для которой текущий [член](member-object-ado-md.md) является родителем в иерархии.</span><span class="sxs-lookup"><span data-stu-id="b6694-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6694-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b6694-105">Return values</span></span>

<span data-ttu-id="b6694-106">Возвращает коллекцию **Членов** и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b6694-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6694-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6694-107">Remarks</span></span>

<span data-ttu-id="b6694-108">Свойство **Children** содержит коллекцию **Членов,** для которой текущий член **является** иерархическим родителем.</span><span class="sxs-lookup"><span data-stu-id="b6694-108">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent.</span></span> <span data-ttu-id="b6694-109">Объекты **уровня Leaf Member** не имеют детских членов в коллекции **Members.**</span><span class="sxs-lookup"><span data-stu-id="b6694-109">Leaf level **Member** objects have no child members in the **Members** collection.</span></span> <span data-ttu-id="b6694-110">Это свойство поддерживается только для **объектов Member,** принадлежащих [объекту Level.](level-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="b6694-110">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="b6694-111">Ошибка возникает, когда это свойство ссылается на **объекты Member,** принадлежащие [объекту Position.](position-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="b6694-111">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

