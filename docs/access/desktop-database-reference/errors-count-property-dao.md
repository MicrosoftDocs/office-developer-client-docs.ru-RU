---
title: Errors.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c49a0f73c759bc901a091bb78bcbd4158e7a1d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867666"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="0ba08-102">Errors.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0ba08-102">Errors.Count Property (DAO)</span></span>


<span data-ttu-id="0ba08-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ba08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ba08-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="0ba08-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="0ba08-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0ba08-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba08-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ba08-106">Syntax</span></span>

<span data-ttu-id="0ba08-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="0ba08-107">*expression* .Count</span></span>

<span data-ttu-id="0ba08-108">*выражение* Переменная, которая представляет объект **ошибки** .</span><span class="sxs-lookup"><span data-stu-id="0ba08-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ba08-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="0ba08-109">Remarks</span></span>

<span data-ttu-id="0ba08-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="0ba08-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="0ba08-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="0ba08-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="0ba08-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="0ba08-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="0ba08-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0ba08-113">If its value is 0, there are no objects in the collection.</span></span>

