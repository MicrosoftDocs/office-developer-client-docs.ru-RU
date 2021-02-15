---
title: Свойство Documents.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3fc0b1e6-f7be-cd43-711f-5cf5763fe7f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192858(v=office.15)
ms:contentKeyID: 48544407
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053325
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dd9cc563ecc885fca4fa0ef5829d82aa2f8bfef6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293744"
---
# <a name="documentscount-property-dao"></a><span data-ttu-id="3bd23-102">Свойство Documents.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="3bd23-102">Documents.Count property (DAO)</span></span>


<span data-ttu-id="3bd23-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bd23-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bd23-104">Возвращает количество объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="3bd23-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="3bd23-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3bd23-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd23-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bd23-106">Syntax</span></span>

<span data-ttu-id="3bd23-107">*выражение .* Count</span><span class="sxs-lookup"><span data-stu-id="3bd23-107">*expression* .Count</span></span>

<span data-ttu-id="3bd23-108">*выражение* Переменная, представляюная объект **Documents.**</span><span class="sxs-lookup"><span data-stu-id="3bd23-108">*expression* A variable that represents a **Documents** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd23-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="3bd23-109">Remarks</span></span>

<span data-ttu-id="3bd23-110">Так как члены коллекции начинаются с 0, всегда следует кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="3bd23-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="3bd23-111">Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="3bd23-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="3bd23-112">Параметр **свойства Count** никогда не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="3bd23-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="3bd23-113">Если его значение 0, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="3bd23-113">If its value is 0, there are no objects in the collection.</span></span>

