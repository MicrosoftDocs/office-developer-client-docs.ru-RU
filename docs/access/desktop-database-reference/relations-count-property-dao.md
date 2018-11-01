---
title: Relations.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1be0766c1f1a2057e5cb7137d2e9131a2505f75
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876010"
---
# <a name="relationscount-property-dao"></a><span data-ttu-id="978f1-102">Relations.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="978f1-102">Relations.Count Property (DAO)</span></span>


<span data-ttu-id="978f1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="978f1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="978f1-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="978f1-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="978f1-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="978f1-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="978f1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="978f1-106">Syntax</span></span>

<span data-ttu-id="978f1-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="978f1-107">*expression* .Count</span></span>

<span data-ttu-id="978f1-108">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="978f1-108">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="978f1-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="978f1-109">Remarks</span></span>

<span data-ttu-id="978f1-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="978f1-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="978f1-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="978f1-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="978f1-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="978f1-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="978f1-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="978f1-113">If its value is 0, there are no objects in the collection.</span></span>

