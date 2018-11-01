---
title: Connections.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec8ff4d610ef9a9b88f379ff8cc72d1b647f9bb2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871908"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="0e103-102">Connections.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0e103-102">Connections.Count Property (DAO)</span></span>


<span data-ttu-id="0e103-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e103-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e103-104">Возвращает количество объектов **[подключения](connection-object-dao.md)** в коллекции **[подключений](connections-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="0e103-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e103-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e103-105">Syntax</span></span>

<span data-ttu-id="0e103-106">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="0e103-106">*expression* .Count</span></span>

<span data-ttu-id="0e103-107">*выражение* Переменная, которая представляет собой объект- **подключений** .</span><span class="sxs-lookup"><span data-stu-id="0e103-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e103-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e103-108">Remarks</span></span>

<span data-ttu-id="0e103-109">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="0e103-109">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="0e103-110">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="0e103-110">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="0e103-111">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="0e103-111">The **Count** property setting is never Null.</span></span> <span data-ttu-id="0e103-112">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0e103-112">If its value is 0, there are no objects in the collection.</span></span>

