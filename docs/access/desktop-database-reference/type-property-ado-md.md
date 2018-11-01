---
title: Свойство Type (ADO MD)
TOCTitle: Type Property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f4a06956db9a051a130af0cbaa6f9090daa586b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889366"
---
# <a name="type-property-ado-md"></a><span data-ttu-id="53bb9-102">Свойство Type (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="53bb9-102">Type Property (ADO MD)</span></span>


<span data-ttu-id="53bb9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53bb9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53bb9-104">Указывает тип текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="53bb9-104">Indicates the type of the current member.</span></span>

## <a name="return-values"></a><span data-ttu-id="53bb9-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="53bb9-105">Return values</span></span>

<span data-ttu-id="53bb9-106">Возвращает значение [MemberTypeEnum](membertypeenum.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="53bb9-106">Returns a [MemberTypeEnum](membertypeenum.md) value and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="53bb9-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="53bb9-107">Remarks</span></span>

<span data-ttu-id="53bb9-108">Это свойство поддерживается только для объектов [члена](member-object-ado-md.md) , относящегося к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="53bb9-108">This property is supported only on [Member](member-object-ado-md.md) objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="53bb9-109">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="53bb9-109">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

