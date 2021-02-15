---
title: Свойство ChildCount (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f8e0fc98d7868eb5462bd7d8714e1a8eda1cfcf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296383"
---
# <a name="childcount-property-ado-md"></a><span data-ttu-id="9e0bf-102">Свойство ChildCount (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="9e0bf-102">ChildCount property (ADO MD)</span></span>


<span data-ttu-id="9e0bf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e0bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e0bf-104">Указывает количество членов, для которых текущий объект [Member](member-object-ado-md.md) является родительским в иерархии.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-104">Indicates the number of members for which the current [Member](member-object-ado-md.md) object is the parent in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="9e0bf-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9e0bf-105">Return values</span></span>

<span data-ttu-id="9e0bf-106">Возвращает **длинное** integer и является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e0bf-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="9e0bf-107">Remarks</span></span>

<span data-ttu-id="9e0bf-108">Используйте свойство **ChildCount,** чтобы получить оценку того, сколько детей у **участника.**</span><span class="sxs-lookup"><span data-stu-id="9e0bf-108">Use the **ChildCount** property to return an estimate of how many children a **Member** has.</span></span> <span data-ttu-id="9e0bf-109">Свойство [Children](children-property-ado-md.md) может  вернуть фактические детей участника.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-109">The actual children of a **Member** can be returned by the [Children](children-property-ado-md.md) property.</span></span>

<span data-ttu-id="9e0bf-110">Для **объектов Member** из объекта [Position](position-object-ado-md.md) возвращается максимальное число 65536.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-110">For **Member** objects from a [Position](position-object-ado-md.md) object, the maximum number returned is 65536.</span></span> <span data-ttu-id="9e0bf-111">Если фактическое число детей превышает 65536, возвращаемая величина будет по-прежнему равно 65536.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-111">If the actual number of children exceeds 65536, the value returned will still be 65536.</span></span> <span data-ttu-id="9e0bf-112">Таким образом, приложение должно интерпретировать **childCount** 65536 как равное или больше 65536 детей.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-112">Therefore, the application should interpret a **ChildCount** of 65536 as equal to or greater than 65536 children.</span></span>

<span data-ttu-id="9e0bf-113">Для **объектов Member** из объекта [Level](level-object-ado-md.md) используйте свойство ADO collection [Count](count-property-ado.md) в коллекции **Children,** чтобы определить точное количество детей.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-113">For **Member** objects from a [Level](level-object-ado-md.md) object, use the ADO collection [Count](count-property-ado.md) property on the **Children** collection to determine the exact number of children.</span></span> <span data-ttu-id="9e0bf-114">Определение точного количества детей может быть медленным, если в коллекции много детей.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-114">Determining the exact number of children may be slow if the number of children in the collection is large.</span></span>

