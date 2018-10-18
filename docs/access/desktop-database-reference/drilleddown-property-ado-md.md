---
title: DrilledDown Property (ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96edfa035937a201891f0dca2aeaf036a5061cfe
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605494"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="73e10-102">DrilledDown Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="73e10-102">DrilledDown Property (ADO MD)</span></span>


<span data-ttu-id="73e10-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="73e10-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="73e10-104">Указывает, будет ли дочерних элементов следовать непосредственно после элемента на оси.</span><span class="sxs-lookup"><span data-stu-id="73e10-104">Indicates whether no children immediately follow the member on the axis.</span></span>

<span data-ttu-id="73e10-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="73e10-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="73e10-106">Return Values</span><span class="sxs-lookup"><span data-stu-id="73e10-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="73e10-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="73e10-107">Return values</span></span>
>>>>>>> <span data-ttu-id="73e10-108">master</span><span class="sxs-lookup"><span data-stu-id="73e10-108">master</span></span>

<span data-ttu-id="73e10-109">Возвращает **логическое** значение и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="73e10-109">Returns a **Boolean** value and is read-only.</span></span> <span data-ttu-id="73e10-110">**DrilledDown** возвращает **значение True** , если нет дочерних членов текущего элемента на оси.</span><span class="sxs-lookup"><span data-stu-id="73e10-110">**DrilledDown** returns **True** if there are no child members of the current member on the axis.</span></span> <span data-ttu-id="73e10-111">**DrilledDown** возвращает **значение False** , если один или несколько дочерних элементов текущего элемента на оси.</span><span class="sxs-lookup"><span data-stu-id="73e10-111">**DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="73e10-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="73e10-112">Remarks</span></span>

<span data-ttu-id="73e10-113">Свойство **DrilledDown** используется для определения, существует ли хотя бы один дочерний этого элемента на оси сразу после этого элемента.</span><span class="sxs-lookup"><span data-stu-id="73e10-113">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member.</span></span> <span data-ttu-id="73e10-114">Эта информация может быть полезна при отображении элемента.</span><span class="sxs-lookup"><span data-stu-id="73e10-114">This information is useful when displaying the member.</span></span>

<span data-ttu-id="73e10-115">Это свойство поддерживается только для объектов [члена](member-object-ado-md.md) , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="73e10-115">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object.</span></span> <span data-ttu-id="73e10-116">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="73e10-116">An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

