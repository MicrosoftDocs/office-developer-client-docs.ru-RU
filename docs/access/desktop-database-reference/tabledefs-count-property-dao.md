---
title: TableDefs.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1158e9a54c5ae835e66d2420926200ff0973a7ec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868569"
---
# <a name="tabledefscount-property-dao"></a><span data-ttu-id="b7e9b-102">TableDefs.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="b7e9b-102">TableDefs.Count Property (DAO)</span></span>


<span data-ttu-id="b7e9b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7e9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7e9b-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="b7e9b-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e9b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7e9b-106">Syntax</span></span>

<span data-ttu-id="b7e9b-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="b7e9b-107">*expression* .Count</span></span>

<span data-ttu-id="b7e9b-108">*выражение* Переменная, которая представляет собой объект- **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="b7e9b-108">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e9b-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b7e9b-109">Remarks</span></span>

<span data-ttu-id="b7e9b-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="b7e9b-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="b7e9b-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="b7e9b-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-113">If its value is 0, there are no objects in the collection.</span></span>

