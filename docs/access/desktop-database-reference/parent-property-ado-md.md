---
title: Свойство Parent (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1da5b763d85fc9975a42e357860d87ce64cf618
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930590"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="997b6-102">Свойство Parent (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="997b6-102">Parent property (ADO MD)</span></span>


<span data-ttu-id="997b6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="997b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="997b6-104">Указывает элемент, являющийся родительским для текущего элемента в иерархии.</span><span class="sxs-lookup"><span data-stu-id="997b6-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="997b6-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="997b6-105">Return values</span></span>

<span data-ttu-id="997b6-106">Возвращает объект, [член](member-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="997b6-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="997b6-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="997b6-107">Remarks</span></span>

<span data-ttu-id="997b6-108">Элемент, который находится на верхнем уровне иерархии (корень) не имеет родительского узла.</span><span class="sxs-lookup"><span data-stu-id="997b6-108">A member that is at the top level of a hierarchy (the root) has no parent.</span></span> <span data-ttu-id="997b6-109">Это свойство поддерживается только для объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="997b6-109">This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="997b6-110">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="997b6-110">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

