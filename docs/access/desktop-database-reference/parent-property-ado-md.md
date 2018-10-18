---
title: Parent Property (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c183c997a3c0b49c74e08f7ef29fbe8c274516
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603338"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="9b292-102">Parent Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="9b292-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="9b292-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b292-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9b292-104">Указывает элемент, являющийся родительским для текущего элемента в иерархии.</span><span class="sxs-lookup"><span data-stu-id="9b292-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

<span data-ttu-id="9b292-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="9b292-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="9b292-106">Return Values</span><span class="sxs-lookup"><span data-stu-id="9b292-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="9b292-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9b292-107">Return values</span></span>
>>>>>>> <span data-ttu-id="9b292-108">master</span><span class="sxs-lookup"><span data-stu-id="9b292-108">master</span></span>

<span data-ttu-id="9b292-109">Возвращает объект, [член](member-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9b292-109">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b292-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="9b292-110">Remarks</span></span>

<span data-ttu-id="9b292-111">Элемент, который находится на верхнем уровне иерархии (корень) не имеет родительского узла.</span><span class="sxs-lookup"><span data-stu-id="9b292-111">A member that is at the top level of a hierarchy (the root) has no parent.</span></span> <span data-ttu-id="9b292-112">Это свойство поддерживается только для объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="9b292-112">This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="9b292-113">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="9b292-113">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

