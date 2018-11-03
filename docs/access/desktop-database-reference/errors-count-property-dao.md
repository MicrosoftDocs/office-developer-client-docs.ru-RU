---
title: Свойство Errors.Count (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc30a8a88e8d5c91c1900b756f6c041655cb848a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923737"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="19d12-102">Свойство Errors.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="19d12-102">Errors.Count property (DAO)</span></span>


<span data-ttu-id="19d12-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19d12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19d12-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="19d12-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="19d12-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="19d12-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d12-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19d12-106">Syntax</span></span>

<span data-ttu-id="19d12-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="19d12-107">*expression* .Count</span></span>

<span data-ttu-id="19d12-108">*выражение* Переменная, которая представляет объект **ошибки** .</span><span class="sxs-lookup"><span data-stu-id="19d12-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="19d12-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="19d12-109">Remarks</span></span>

<span data-ttu-id="19d12-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="19d12-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="19d12-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="19d12-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="19d12-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="19d12-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="19d12-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="19d12-113">If its value is 0, there are no objects in the collection.</span></span>

