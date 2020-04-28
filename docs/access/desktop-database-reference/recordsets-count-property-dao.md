---
title: Свойство recordsets. Count (DAO)
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
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="8bf78-102">Свойство recordsets. Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="8bf78-102">Recordsets.Count property (DAO)</span></span>


<span data-ttu-id="8bf78-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bf78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8bf78-104">Возвращает число объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="8bf78-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="8bf78-105">Только для чтения, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="8bf78-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf78-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bf78-106">Syntax</span></span>

<span data-ttu-id="8bf78-107">*Expression* . Отсчет</span><span class="sxs-lookup"><span data-stu-id="8bf78-107">*expression* .Count</span></span>

<span data-ttu-id="8bf78-108">*Expression (выражение* ) Переменная, представляющая объект **recordsets** .</span><span class="sxs-lookup"><span data-stu-id="8bf78-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bf78-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bf78-109">Remarks</span></span>

<span data-ttu-id="8bf78-110">Так как члены коллекции начинаются с 0, всегда следует всегда кодировать циклы, начиная с элемента 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="8bf78-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="8bf78-111">Если требуется перебрать элементы коллекции, не проверяя свойство **Count** , можно использовать оператор **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="8bf78-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="8bf78-112">Значение свойства **Count** не может быть равно null.</span><span class="sxs-lookup"><span data-stu-id="8bf78-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="8bf78-113">Если его значение равно 0, в коллекции отсутствуют объекты.</span><span class="sxs-lookup"><span data-stu-id="8bf78-113">If its value is 0, there are no objects in the collection.</span></span>

