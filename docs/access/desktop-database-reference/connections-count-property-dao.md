---
title: Свойство Connections.Count (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a286bf992116dc4ddfa71a9be8231e70b717aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295760"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="a07e1-102">Свойство Connections.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="a07e1-102">Connections.Count property (DAO)</span></span>


<span data-ttu-id="a07e1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a07e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a07e1-104">Возвращает количество объектов **[Подключения](connection-object-dao.md)** в коллекции **[Connections.](connections-collection-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="a07e1-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a07e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a07e1-105">Syntax</span></span>

<span data-ttu-id="a07e1-106">*выражения* . Count</span><span class="sxs-lookup"><span data-stu-id="a07e1-106">*expression* .Count</span></span>

<span data-ttu-id="a07e1-107">*выражение* Переменная, представляюная объект **Connections.**</span><span class="sxs-lookup"><span data-stu-id="a07e1-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a07e1-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="a07e1-108">Remarks</span></span>

<span data-ttu-id="a07e1-109">Так как члены коллекции начинаются с 0, всегда следует использовать циклы кода, начиная с участника 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="a07e1-109">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="a07e1-110">Если вы хотите пройти цикл через членов коллекции без проверки свойства **Count,** вы можете использовать **для каждого... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="a07e1-110">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="a07e1-111">Параметр **свойства Count** никогда не является Null.</span><span class="sxs-lookup"><span data-stu-id="a07e1-111">The **Count** property setting is never Null.</span></span> <span data-ttu-id="a07e1-112">Если его значение 0, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="a07e1-112">If its value is 0, there are no objects in the collection.</span></span>

