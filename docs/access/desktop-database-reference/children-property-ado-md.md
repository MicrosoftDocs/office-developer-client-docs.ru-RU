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
# <a name="children-property-ado-md"></a><span data-ttu-id="391c9-102">Свойство Children (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="391c9-102">Children property (ADO MD)</span></span>


<span data-ttu-id="391c9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="391c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="391c9-104">Возвращает коллекцию [Members,](members-collection-ado-md.md) для которой [текущий](member-object-ado-md.md) член является родительским в иерархии.</span><span class="sxs-lookup"><span data-stu-id="391c9-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="391c9-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="391c9-105">Return values</span></span>

<span data-ttu-id="391c9-106">Возвращает коллекцию **Members** и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="391c9-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="391c9-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="391c9-107">Remarks</span></span>

<span data-ttu-id="391c9-108">Свойство **Children** содержит коллекцию **Members,** для которой текущий **член** является иерархическим родительским объектом.</span><span class="sxs-lookup"><span data-stu-id="391c9-108">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent.</span></span> <span data-ttu-id="391c9-109">У объектов Leaf level **Member** нет членов-членов в коллекции **Members.**</span><span class="sxs-lookup"><span data-stu-id="391c9-109">Leaf level **Member** objects have no child members in the **Members** collection.</span></span> <span data-ttu-id="391c9-110">Это свойство поддерживается только для объектов **Member,** принадлежащих [объекту Level.](level-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="391c9-110">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="391c9-111">Ошибка возникает, когда на это свойство ссылается объект **Member,** принадлежащий [объекту Position.](position-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="391c9-111">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

