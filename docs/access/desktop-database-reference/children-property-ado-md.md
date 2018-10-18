---
title: Children Property (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbbae74ce8ce22255e97403fc3906dd50f36b38b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605053"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="20449-102">Children Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="20449-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="20449-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="20449-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="20449-104">Возвращает коллекцию [членов](members-collection-ado-md.md) , для которого текущий [элемент](member-object-ado-md.md) является родительской в иерархии.</span><span class="sxs-lookup"><span data-stu-id="20449-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

<span data-ttu-id="20449-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="20449-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="20449-106">Return Values</span><span class="sxs-lookup"><span data-stu-id="20449-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="20449-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="20449-107">Return values</span></span>
>>>>>>> <span data-ttu-id="20449-108">master</span><span class="sxs-lookup"><span data-stu-id="20449-108">master</span></span>

<span data-ttu-id="20449-109">Возвращает коллекцию **элементов** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="20449-109">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="20449-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="20449-110">Remarks</span></span>

<span data-ttu-id="20449-111">**В свойстве** содержит коллекцию **Members** , для которого текущий **член** является иерархической родительского.</span><span class="sxs-lookup"><span data-stu-id="20449-111">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent.</span></span> <span data-ttu-id="20449-112">Конечные объекты уровень **член** не содержат дочерние членов в коллекции **элементов** .</span><span class="sxs-lookup"><span data-stu-id="20449-112">Leaf level **Member** objects have no child members in the **Members** collection.</span></span> <span data-ttu-id="20449-113">Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="20449-113">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="20449-114">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="20449-114">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

