---
title: Свойство Relations.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd9cc00d2dc33263d6226783770fdae5207137f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306960"
---
# <a name="relationscount-property-dao"></a><span data-ttu-id="3a656-102">Свойство Relations.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a656-102">Relations.Count property (DAO)</span></span>


<span data-ttu-id="3a656-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a656-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a656-104">Возвращает количество объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a656-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="3a656-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3a656-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a656-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a656-106">Syntax</span></span>

<span data-ttu-id="3a656-107">*выражение .* Count</span><span class="sxs-lookup"><span data-stu-id="3a656-107">*expression* .Count</span></span>

<span data-ttu-id="3a656-108">*выражение* Переменная, представляюная объект **Relations.**</span><span class="sxs-lookup"><span data-stu-id="3a656-108">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a656-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="3a656-109">Remarks</span></span>

<span data-ttu-id="3a656-110">Так как члены коллекции начинаются с 0, всегда следует кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="3a656-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="3a656-111">Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="3a656-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="3a656-112">Параметр **свойства Count** никогда не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="3a656-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="3a656-113">Если его значение 0, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="3a656-113">If its value is 0, there are no objects in the collection.</span></span>

