---
title: DrilledDown Property (ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8d203513ce88998143d3043e76ce6ffb6a64741
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479800"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="377ac-102">DrilledDown Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="377ac-102">DrilledDown Property (ADO MD)</span></span>


<span data-ttu-id="377ac-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="377ac-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="377ac-104">Указывает, будет ли дочерних элементов следовать непосредственно после элемента на оси.</span><span class="sxs-lookup"><span data-stu-id="377ac-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="377ac-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="377ac-105">Return Values</span></span>

<span data-ttu-id="377ac-106">Возвращает **логическое** значение и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="377ac-106">Returns a **Boolean** value and is read-only.</span></span> <span data-ttu-id="377ac-107">**DrilledDown** возвращает **значение True** , если нет дочерних членов текущего элемента на оси.</span><span class="sxs-lookup"><span data-stu-id="377ac-107">**DrilledDown** returns **True** if there are no child members of the current member on the axis.</span></span> <span data-ttu-id="377ac-108">**DrilledDown** возвращает **значение False** , если один или несколько дочерних элементов текущего элемента на оси.</span><span class="sxs-lookup"><span data-stu-id="377ac-108">**DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="377ac-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="377ac-109">Remarks</span></span>

<span data-ttu-id="377ac-110">Свойство **DrilledDown** используется для определения, существует ли хотя бы один дочерний этого элемента на оси сразу после этого элемента.</span><span class="sxs-lookup"><span data-stu-id="377ac-110">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member.</span></span> <span data-ttu-id="377ac-111">Эта информация может быть полезна при отображении элемента.</span><span class="sxs-lookup"><span data-stu-id="377ac-111">This information is useful when displaying the member.</span></span>

<span data-ttu-id="377ac-112">Это свойство поддерживается только для объектов [члена](member-object-ado-md.md) , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="377ac-112">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object.</span></span> <span data-ttu-id="377ac-113">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="377ac-113">An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

