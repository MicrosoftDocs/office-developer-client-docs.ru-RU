---
title: Свойство Errors.Count (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2cbbed2c7061b225d969dbd7554191e8db4a28a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293401"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="10364-102">Свойство Errors.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="10364-102">Errors.Count property (DAO)</span></span>


<span data-ttu-id="10364-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10364-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10364-104">Возвращает количество объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="10364-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="10364-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="10364-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10364-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10364-106">Syntax</span></span>

<span data-ttu-id="10364-107">*выражение .* Count</span><span class="sxs-lookup"><span data-stu-id="10364-107">*expression* .Count</span></span>

<span data-ttu-id="10364-108">*выражение* Переменная, представляюная объект **Errors.**</span><span class="sxs-lookup"><span data-stu-id="10364-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="10364-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="10364-109">Remarks</span></span>

<span data-ttu-id="10364-110">Так как члены коллекции начинаются с 0, необходимо всегда кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="10364-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="10364-111">Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="10364-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="10364-112">Параметр **свойства Count** никогда не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="10364-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="10364-113">Если его значение 0, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="10364-113">If its value is 0, there are no objects in the collection.</span></span>

