---
title: Свойство Indexes.Count (DAO)
TOCTitle: Count Property
ms:assetid: 195ede10-f91e-50c6-6af4-b318c476b9ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845647(v=office.15)
ms:contentKeyID: 48543499
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae6a8098e51f271080924a8569d31e5bc268dc1f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927020"
---
# <a name="indexescount-property-dao"></a><span data-ttu-id="2b46f-102">Свойство Indexes.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b46f-102">Indexes.Count property (DAO)</span></span>


<span data-ttu-id="2b46f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b46f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b46f-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="2b46f-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="2b46f-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2b46f-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b46f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b46f-106">Syntax</span></span>

<span data-ttu-id="2b46f-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="2b46f-107">*expression* .Count</span></span>

<span data-ttu-id="2b46f-108">*выражение* Переменная, которая представляет объект **индексов** .</span><span class="sxs-lookup"><span data-stu-id="2b46f-108">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b46f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b46f-109">Remarks</span></span>

<span data-ttu-id="2b46f-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="2b46f-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="2b46f-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="2b46f-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="2b46f-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="2b46f-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="2b46f-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2b46f-113">If its value is 0, there are no objects in the collection.</span></span>

