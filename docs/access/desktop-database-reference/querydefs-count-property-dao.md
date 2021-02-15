---
title: Свойство QueryDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95624c82ee9ab322eec5455759cf4ec2e9708dba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300961"
---
# <a name="querydefscount-property-dao"></a><span data-ttu-id="ccf05-102">Свойство QueryDefs.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="ccf05-102">QueryDefs.Count property (DAO)</span></span>


<span data-ttu-id="ccf05-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ccf05-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ccf05-104">Возвращает количество объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="ccf05-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="ccf05-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ccf05-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf05-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccf05-106">Syntax</span></span>

<span data-ttu-id="ccf05-107">*выражение .* Count</span><span class="sxs-lookup"><span data-stu-id="ccf05-107">*expression* .Count</span></span>

<span data-ttu-id="ccf05-108">*выражение* Переменная, представляюная объект **QueryDefs.**</span><span class="sxs-lookup"><span data-stu-id="ccf05-108">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf05-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="ccf05-109">Remarks</span></span>

<span data-ttu-id="ccf05-110">Так как члены коллекции начинаются с 0, всегда следует кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="ccf05-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="ccf05-111">Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="ccf05-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="ccf05-112">Параметр **свойства Count** никогда не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="ccf05-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="ccf05-113">Если его значение 0, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="ccf05-113">If its value is 0, there are no objects in the collection.</span></span>

