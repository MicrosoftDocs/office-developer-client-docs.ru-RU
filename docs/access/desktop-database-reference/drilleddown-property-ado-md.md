---
title: Свойство DrilledDown (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40a97c7f755f681169c77c3a2077ee41d9cdc980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293688"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="3b036-102">Свойство DrilledDown (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3b036-102">DrilledDown property (ADO MD)</span></span>


<span data-ttu-id="3b036-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b036-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b036-104">Указывает, должны ли дочерние элементы сразу следовать за элементом на оси.</span><span class="sxs-lookup"><span data-stu-id="3b036-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="3b036-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3b036-105">Return values</span></span>

<span data-ttu-id="3b036-106">Возвращает **логическое** значение и доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b036-106">Returns a **Boolean** value and is read-only.</span></span> <span data-ttu-id="3b036-107">**DrilledDown** возвращает **значение true** , если на оси нет дочерних элементов текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="3b036-107">**DrilledDown** returns **True** if there are no child members of the current member on the axis.</span></span> <span data-ttu-id="3b036-108">**DrilledDown** возвращает **значение false** , если один или несколько дочерних элементов текущего элемента оси.</span><span class="sxs-lookup"><span data-stu-id="3b036-108">**DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b036-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="3b036-109">Remarks</span></span>

<span data-ttu-id="3b036-110">Используйте свойство **DrilledDown** , чтобы определить, есть ли по крайней мере один дочерний элемент этого элемента на оси, которая сразу после этого элемента.</span><span class="sxs-lookup"><span data-stu-id="3b036-110">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member.</span></span> <span data-ttu-id="3b036-111">Эта информация полезна при отображении элемента.</span><span class="sxs-lookup"><span data-stu-id="3b036-111">This information is useful when displaying the member.</span></span>

<span data-ttu-id="3b036-112">Это свойство поддерживается только для объектов [member](member-object-ado-md.md) , принадлежащих объекту [position](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="3b036-112">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object.</span></span> <span data-ttu-id="3b036-113">При обращении к этому свойству из объектов **member** , принадлежащих объекту [уровня](level-object-ado-md.md) , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3b036-113">An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

