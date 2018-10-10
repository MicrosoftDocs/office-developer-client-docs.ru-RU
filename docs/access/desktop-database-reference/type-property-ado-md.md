---
title: Type Property (ADO MD)
TOCTitle: Type Property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3ea67b96e24f01e167ca693dff356c595005904
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479783"
---
# <a name="type-property-ado-md"></a><span data-ttu-id="25bb6-102">Type Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="25bb6-102">Type Property (ADO MD)</span></span>


<span data-ttu-id="25bb6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="25bb6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="25bb6-104">Указывает тип текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="25bb6-104">Indicates the type of the current member.</span></span>

## <a name="return-values"></a><span data-ttu-id="25bb6-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="25bb6-105">Return Values</span></span>

<span data-ttu-id="25bb6-106">Возвращает значение [MemberTypeEnum](membertypeenum.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="25bb6-106">Returns a [MemberTypeEnum](membertypeenum.md) value and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="25bb6-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="25bb6-107">Remarks</span></span>

<span data-ttu-id="25bb6-108">Это свойство поддерживается только для объектов [члена](member-object-ado-md.md) , относящегося к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="25bb6-108">This property is supported only on [Member](member-object-ado-md.md) objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="25bb6-109">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="25bb6-109">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

