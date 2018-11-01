---
title: Recordsets.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5697dcb6dbf3eb306ac94041127ee3e5992467
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881666"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="89dab-102">Recordsets.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="89dab-102">Recordsets.Count Property (DAO)</span></span>


<span data-ttu-id="89dab-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89dab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89dab-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="89dab-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="89dab-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="89dab-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="89dab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89dab-106">Syntax</span></span>

<span data-ttu-id="89dab-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="89dab-107">*expression* .Count</span></span>

<span data-ttu-id="89dab-108">*выражение* Переменная, которая представляет собой объект- **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="89dab-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="89dab-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="89dab-109">Remarks</span></span>

<span data-ttu-id="89dab-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="89dab-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="89dab-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="89dab-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="89dab-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="89dab-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="89dab-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="89dab-113">If its value is 0, there are no objects in the collection.</span></span>

