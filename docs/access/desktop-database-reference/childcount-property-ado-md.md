---
title: ChildCount Property (ADO MD)
TOCTitle: ChildCount Property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fb6edf995651241d15b9bc9fc9df1ce507801bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481393"
---
# <a name="childcount-property-ado-md"></a><span data-ttu-id="37419-102">ChildCount Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="37419-102">ChildCount Property (ADO MD)</span></span>


<span data-ttu-id="37419-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37419-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37419-104">Указывает число участников, для которых текущего объекта [член](member-object-ado-md.md) является родительской в иерархии.</span><span class="sxs-lookup"><span data-stu-id="37419-104">Indicates the number of members for which the current [Member](member-object-ado-md.md) object is the parent in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="37419-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="37419-105">Return Values</span></span>

<span data-ttu-id="37419-106">Возвращает значение типа **Long** integer и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="37419-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="37419-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="37419-107">Remarks</span></span>

<span data-ttu-id="37419-108">Свойство **ChildCount** Возвращает оценку сколько потомки **члена** имеет.</span><span class="sxs-lookup"><span data-stu-id="37419-108">Use the **ChildCount** property to return an estimate of how many children a **Member** has.</span></span> <span data-ttu-id="37419-109">Фактические потомки **члена** можно возвращается свойством [дочерних элементов](children-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="37419-109">The actual children of a **Member** can be returned by the [Children](children-property-ado-md.md) property.</span></span>

<span data-ttu-id="37419-110">Для объектов **члена** из [положение](position-object-ado-md.md) объекта возвращается не более 65536.</span><span class="sxs-lookup"><span data-stu-id="37419-110">For **Member** objects from a [Position](position-object-ado-md.md) object, the maximum number returned is 65536.</span></span> <span data-ttu-id="37419-111">Если фактическое число дочерних элементов превышает 65536, возвращаемое значение будет по-прежнему 65536.</span><span class="sxs-lookup"><span data-stu-id="37419-111">If the actual number of children exceeds 65536, the value returned will still be 65536.</span></span> <span data-ttu-id="37419-112">Таким образом приложение следует воспринимать **ChildCount** из 65536 как равно или больше, чем 65536 дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="37419-112">Therefore, the application should interpret a **ChildCount** of 65536 as equal to or greater than 65536 children.</span></span>

<span data-ttu-id="37419-113">Для объектов **члена** из объекта [уровень](level-object-ado-md.md) используйте свойство [Count](count-property-ado.md) коллекции ADO на коллекцию **дочерних элементов** , чтобы определить точное количество дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="37419-113">For **Member** objects from a [Level](level-object-ado-md.md) object, use the ADO collection [Count](count-property-ado.md) property on the **Children** collection to determine the exact number of children.</span></span> <span data-ttu-id="37419-114">Определение точное количество дочерних элементов может быть медленным, если большое число дочерних объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="37419-114">Determining the exact number of children may be slow if the number of children in the collection is large.</span></span>

