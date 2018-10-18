---
title: ChildCount Property (ADO MD)
TOCTitle: ChildCount Property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84e2e9873e076128c42e9fa7ae46d902f47865c7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606027"
---
# <a name="childcount-property-ado-md"></a><span data-ttu-id="f3fe9-102">ChildCount Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f3fe9-102">ChildCount Property (ADO MD)</span></span>


<span data-ttu-id="f3fe9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3fe9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f3fe9-104">Указывает число участников, для которых текущего объекта [член](member-object-ado-md.md) является родительской в иерархии.</span><span class="sxs-lookup"><span data-stu-id="f3fe9-104">Indicates the number of members for which the current [Member](member-object-ado-md.md) object is the parent in a hierarchy.</span></span>

<span data-ttu-id="f3fe9-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f3fe9-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="f3fe9-106">Return Values</span><span class="sxs-lookup"><span data-stu-id="f3fe9-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="f3fe9-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f3fe9-107">Return values</span></span>
>>>>>>> <span data-ttu-id="f3fe9-108">master</span><span class="sxs-lookup"><span data-stu-id="f3fe9-108">master</span></span>

<span data-ttu-id="f3fe9-109">Возвращает значение типа **Long** integer и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f3fe9-109">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3fe9-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3fe9-110">Remarks</span></span>

<span data-ttu-id="f3fe9-111">Свойство **ChildCount** Возвращает оценку сколько потомки **члена** имеет.</span><span class="sxs-lookup"><span data-stu-id="f3fe9-111">Use the **ChildCount** property to return an estimate of how many children a **Member** has.</span></span> <span data-ttu-id="f3fe9-112">Фактические потомки **члена** можно возвращается свойством [дочерних элементов](children-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="f3fe9-112">The actual children of a **Member** can be returned by the [Children](children-property-ado-md.md) property.</span></span>

<span data-ttu-id="f3fe9-113">Для объектов **члена** из [положение](position-object-ado-md.md) объекта возвращается не более 65536.</span><span class="sxs-lookup"><span data-stu-id="f3fe9-113">For **Member** objects from a [Position](position-object-ado-md.md) object, the maximum number returned is 65536.</span></span> <span data-ttu-id="f3fe9-114">Если фактическое число дочерних элементов превышает 65536, возвращаемое значение будет по-прежнему 65536.</span><span class="sxs-lookup"><span data-stu-id="f3fe9-114">If the actual number of children exceeds 65536, the value returned will still be 65536.</span></span> <span data-ttu-id="f3fe9-115">Таким образом приложение следует воспринимать **ChildCount** из 65536 как равно или больше, чем 65536 дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="f3fe9-115">Therefore, the application should interpret a **ChildCount** of 65536 as equal to or greater than 65536 children.</span></span>

<span data-ttu-id="f3fe9-116">Для объектов **члена** из объекта [уровень](level-object-ado-md.md) используйте свойство [Count](count-property-ado.md) коллекции ADO на коллекцию **дочерних элементов** , чтобы определить точное количество дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="f3fe9-116">For **Member** objects from a [Level](level-object-ado-md.md) object, use the ADO collection [Count](count-property-ado.md) property on the **Children** collection to determine the exact number of children.</span></span> <span data-ttu-id="f3fe9-117">Определение точное количество дочерних элементов может быть медленным, если большое число дочерних объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="f3fe9-117">Determining the exact number of children may be slow if the number of children in the collection is large.</span></span>

