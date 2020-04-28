---
title: Свойство Fields. Count (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99eb21ba4f4ef13c902fc0d029dba59c30066853
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292547"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="0b18b-102">Свойство Fields. Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="0b18b-102">Fields.Count property (DAO)</span></span>


<span data-ttu-id="0b18b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b18b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b18b-104">Возвращает число объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="0b18b-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="0b18b-105">Только для чтения, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="0b18b-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b18b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b18b-106">Syntax</span></span>

<span data-ttu-id="0b18b-107">*Expression* . Отсчет</span><span class="sxs-lookup"><span data-stu-id="0b18b-107">*expression* .Count</span></span>

<span data-ttu-id="0b18b-108">*выражение*: переменная, представляющая объект **Fields**.</span><span class="sxs-lookup"><span data-stu-id="0b18b-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b18b-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b18b-109">Remarks</span></span>

<span data-ttu-id="0b18b-110">Так как члены коллекции начинаются с 0, всегда следует всегда кодировать циклы, начиная с элемента 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="0b18b-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="0b18b-111">Если требуется перебрать элементы коллекции, не проверяя свойство **Count** , можно использовать оператор **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="0b18b-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="0b18b-112">Значение свойства **Count** не может быть равно null.</span><span class="sxs-lookup"><span data-stu-id="0b18b-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="0b18b-113">Если его значение равно 0, в коллекции отсутствуют объекты.</span><span class="sxs-lookup"><span data-stu-id="0b18b-113">If its value is 0, there are no objects in the collection.</span></span>

