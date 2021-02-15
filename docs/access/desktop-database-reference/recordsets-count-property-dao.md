---
title: Свойство Recordsets.Count (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a81c1ede8a3afb95e39b2c33fb8112119faf8bd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309292"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="65bb0-102">Свойство Recordsets.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="65bb0-102">Recordsets.Count property (DAO)</span></span>


<span data-ttu-id="65bb0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65bb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65bb0-104">Возвращает количество объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="65bb0-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="65bb0-105">Только для чтения, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="65bb0-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="65bb0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65bb0-106">Syntax</span></span>

<span data-ttu-id="65bb0-107">*выражение .* Count</span><span class="sxs-lookup"><span data-stu-id="65bb0-107">*expression* .Count</span></span>

<span data-ttu-id="65bb0-108">*выражение* Переменная, представляюная объект **Recordsets.**</span><span class="sxs-lookup"><span data-stu-id="65bb0-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="65bb0-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="65bb0-109">Remarks</span></span>

<span data-ttu-id="65bb0-110">Так как члены коллекции начинаются с 0, всегда следует кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="65bb0-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="65bb0-111">Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="65bb0-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="65bb0-112">Параметр **свойства Count** никогда не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="65bb0-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="65bb0-113">Если его значение 0, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="65bb0-113">If its value is 0, there are no objects in the collection.</span></span>

