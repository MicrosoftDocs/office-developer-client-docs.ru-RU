---
title: Свойство Containers.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7553b0e7d64e059dfeed50f158f21f48455976d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295592"
---
# <a name="containerscount-property-dao"></a><span data-ttu-id="2d991-102">Свойство Containers.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d991-102">Containers.Count property (DAO)</span></span>


<span data-ttu-id="2d991-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d991-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d991-104">Возвращает количество объектов **[Connection](connection-object-dao.md)** в коллекции **[Connections.](connections-collection-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="2d991-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d991-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d991-105">Syntax</span></span>

<span data-ttu-id="2d991-106">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="2d991-106">*expression* .Count</span></span>

<span data-ttu-id="2d991-107">*выражение* Переменная, представляюная объект **Connections.**</span><span class="sxs-lookup"><span data-stu-id="2d991-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d991-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="2d991-108">Remarks</span></span>

<span data-ttu-id="2d991-109">Так как члены коллекции начинаются с 0, необходимо всегда кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="2d991-109">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="2d991-110">Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="2d991-110">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="2d991-111">Параметр **свойства Count** никогда не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="2d991-111">The **Count** property setting is never Null.</span></span> <span data-ttu-id="2d991-112">Если его значение 0, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="2d991-112">If its value is 0, there are no objects in the collection.</span></span>

