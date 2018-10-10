---
title: Children Property (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e126b203e2282f96070f1f3eb14a9b926c04f432
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480345"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="7036e-102">Children Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7036e-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="7036e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7036e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7036e-104">Возвращает коллекцию [членов](members-collection-ado-md.md) , для которого текущий [элемент](member-object-ado-md.md) является родительской в иерархии.</span><span class="sxs-lookup"><span data-stu-id="7036e-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="7036e-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="7036e-105">Return Values</span></span>

<span data-ttu-id="7036e-106">Возвращает коллекцию **элементов** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7036e-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="7036e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="7036e-107">Remarks</span></span>

<span data-ttu-id="7036e-108">**В свойстве** содержит коллекцию **Members** , для которого текущий **член** является иерархической родительского.</span><span class="sxs-lookup"><span data-stu-id="7036e-108">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent.</span></span> <span data-ttu-id="7036e-109">Конечные объекты уровень **член** не содержат дочерние членов в коллекции **элементов** .</span><span class="sxs-lookup"><span data-stu-id="7036e-109">Leaf level **Member** objects have no child members in the **Members** collection.</span></span> <span data-ttu-id="7036e-110">Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="7036e-110">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="7036e-111">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="7036e-111">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

