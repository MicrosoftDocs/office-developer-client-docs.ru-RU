---
title: Recordsets.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3351c1bb2099072622b7f18d7eba23674b398807
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480748"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="cfadb-102">Recordsets.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="cfadb-102">Recordsets.Count Property (DAO)</span></span>


<span data-ttu-id="cfadb-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfadb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cfadb-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="cfadb-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="cfadb-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="cfadb-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfadb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfadb-106">Syntax</span></span>

<span data-ttu-id="cfadb-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="cfadb-107">*expression* .Count</span></span>

<span data-ttu-id="cfadb-108">*выражение* Переменная, которая представляет собой объект- **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="cfadb-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfadb-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="cfadb-109">Remarks</span></span>

<span data-ttu-id="cfadb-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="cfadb-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="cfadb-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="cfadb-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="cfadb-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="cfadb-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="cfadb-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="cfadb-113">If its value is 0, there are no objects in the collection.</span></span>

