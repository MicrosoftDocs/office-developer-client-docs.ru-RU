---
title: Parent Property (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb1606a745cb8572f54b253bdbbbbbb461cfc74a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481005"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="45dd5-102">Parent Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="45dd5-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="45dd5-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="45dd5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="45dd5-104">Указывает элемент, являющийся родительским для текущего элемента в иерархии.</span><span class="sxs-lookup"><span data-stu-id="45dd5-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="45dd5-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="45dd5-105">Return Values</span></span>

<span data-ttu-id="45dd5-106">Возвращает объект, [член](member-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="45dd5-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="45dd5-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="45dd5-107">Remarks</span></span>

<span data-ttu-id="45dd5-108">Элемент, который находится на верхнем уровне иерархии (корень) не имеет родительского узла.</span><span class="sxs-lookup"><span data-stu-id="45dd5-108">A member that is at the top level of a hierarchy (the root) has no parent.</span></span> <span data-ttu-id="45dd5-109">Это свойство поддерживается только для объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="45dd5-109">This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="45dd5-110">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="45dd5-110">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

