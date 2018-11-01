---
title: Fields.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f788b726f5be7cdfd7531d4522b6c653744d1c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886748"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="340ac-102">Fields.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="340ac-102">Fields.Count Property (DAO)</span></span>


<span data-ttu-id="340ac-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="340ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="340ac-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="340ac-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="340ac-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="340ac-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="340ac-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="340ac-106">Syntax</span></span>

<span data-ttu-id="340ac-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="340ac-107">*expression* .Count</span></span>

<span data-ttu-id="340ac-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="340ac-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="340ac-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="340ac-109">Remarks</span></span>

<span data-ttu-id="340ac-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="340ac-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="340ac-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="340ac-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="340ac-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="340ac-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="340ac-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="340ac-113">If its value is 0, there are no objects in the collection.</span></span>

