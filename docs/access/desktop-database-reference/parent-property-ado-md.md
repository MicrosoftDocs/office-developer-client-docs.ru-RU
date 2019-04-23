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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287792"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="098d5-102">Свойство Parent (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="098d5-102">Parent property (ADO MD)</span></span>


<span data-ttu-id="098d5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="098d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="098d5-104">Указывает члена, который является родительским для текущего элемента в иерархии.</span><span class="sxs-lookup"><span data-stu-id="098d5-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="098d5-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="098d5-105">Return values</span></span>

<span data-ttu-id="098d5-106">Возвращает объект [member](member-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="098d5-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="098d5-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="098d5-107">Remarks</span></span>

<span data-ttu-id="098d5-108">Элемент, расположенный на верхнем уровне иерархии (корень), не имеет родителя.</span><span class="sxs-lookup"><span data-stu-id="098d5-108">A member that is at the top level of a hierarchy (the root) has no parent.</span></span> <span data-ttu-id="098d5-109">Это свойство поддерживается только для объектов **member** , принадлежащих объекту [уровня](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="098d5-109">This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="098d5-110">При обращении к этому свойству из объектов **member** , принадлежащих объекту [position](position-object-ado-md.md) , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="098d5-110">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

