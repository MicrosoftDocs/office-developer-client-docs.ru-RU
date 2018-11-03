---
title: Свойство QueryDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5efc7479f69d379f406a9a7cda5d4c522df6325
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930898"
---
# <a name="querydefscount-property-dao"></a><span data-ttu-id="6a007-102">Свойство QueryDefs.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="6a007-102">QueryDefs.Count property (DAO)</span></span>


<span data-ttu-id="6a007-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a007-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a007-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="6a007-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="6a007-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6a007-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a007-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a007-106">Syntax</span></span>

<span data-ttu-id="6a007-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="6a007-107">*expression* .Count</span></span>

<span data-ttu-id="6a007-108">*выражение* Переменная, которая представляет собой объект- **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="6a007-108">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a007-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a007-109">Remarks</span></span>

<span data-ttu-id="6a007-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="6a007-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="6a007-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="6a007-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="6a007-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="6a007-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="6a007-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6a007-113">If its value is 0, there are no objects in the collection.</span></span>

