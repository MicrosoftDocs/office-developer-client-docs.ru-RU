---
title: Свойство Parent (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700003"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="f8534-102">Свойство Parent (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f8534-102">Parent property (ADO MD)</span></span>


<span data-ttu-id="f8534-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8534-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8534-104">Указывает элемент, являющийся родительским для текущего элемента в иерархии.</span><span class="sxs-lookup"><span data-stu-id="f8534-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8534-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f8534-105">Return values</span></span>

<span data-ttu-id="f8534-106">Возвращает объект, [член](member-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f8534-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8534-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="f8534-107">Remarks</span></span>

<span data-ttu-id="f8534-108">Элемент, который находится на верхнем уровне иерархии (корень) не имеет родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f8534-108">A member that is at the top level of a hierarchy (the root) has no parent.</span></span> <span data-ttu-id="f8534-109">Это свойство поддерживается только для объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="f8534-109">This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="f8534-110">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="f8534-110">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

