---
title: Свойство databases. Count (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd8908492721315202c5bdf26109753c88905a07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294626"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="6e372-102">Свойство databases. Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e372-102">Databases.Count property (DAO)</span></span>


<span data-ttu-id="6e372-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e372-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e372-104">Возвращает число объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="6e372-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="6e372-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6e372-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e372-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e372-106">Syntax</span></span>

<span data-ttu-id="6e372-107">*Expression* . Отсчет</span><span class="sxs-lookup"><span data-stu-id="6e372-107">*expression* .Count</span></span>

<span data-ttu-id="6e372-108">*Expression (выражение* ) Переменная, представляющая объект **databases** .</span><span class="sxs-lookup"><span data-stu-id="6e372-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e372-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e372-109">Remarks</span></span>

<span data-ttu-id="6e372-110">Так как члены коллекции начинаются с 0, всегда следует всегда кодировать циклы, начиная с элемента 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="6e372-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="6e372-111">Если требуется перебрать элементы коллекции, не проверяя свойство **Count** , можно использовать оператор **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="6e372-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="6e372-112">Значение свойства **Count** не может быть равно null.</span><span class="sxs-lookup"><span data-stu-id="6e372-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="6e372-113">Если его значение равно 0, в коллекции отсутствуют объекты.</span><span class="sxs-lookup"><span data-stu-id="6e372-113">If its value is 0, there are no objects in the collection.</span></span>

