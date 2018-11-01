---
title: Databases.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1860f1719b4e26ab192450c66d610517f0ca9a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868646"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="2010f-102">Databases.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="2010f-102">Databases.Count Property (DAO)</span></span>


<span data-ttu-id="2010f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2010f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2010f-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="2010f-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="2010f-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2010f-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2010f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2010f-106">Syntax</span></span>

<span data-ttu-id="2010f-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="2010f-107">*expression* .Count</span></span>

<span data-ttu-id="2010f-108">*выражение* Переменная, которая представляет собой объект- **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="2010f-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2010f-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="2010f-109">Remarks</span></span>

<span data-ttu-id="2010f-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="2010f-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="2010f-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="2010f-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="2010f-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="2010f-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="2010f-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2010f-113">If its value is 0, there are no objects in the collection.</span></span>

