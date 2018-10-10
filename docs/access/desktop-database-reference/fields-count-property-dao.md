---
title: Fields.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bc5cbe34378951ea973725132256f278ade11cf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483272"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="21f17-102">Fields.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="21f17-102">Fields.Count Property (DAO)</span></span>


<span data-ttu-id="21f17-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="21f17-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="21f17-104">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="21f17-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="21f17-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="21f17-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f17-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21f17-106">Syntax</span></span>

<span data-ttu-id="21f17-107">*выражение* . Count</span><span class="sxs-lookup"><span data-stu-id="21f17-107">*expression* .Count</span></span>

<span data-ttu-id="21f17-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="21f17-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f17-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="21f17-109">Remarks</span></span>

<span data-ttu-id="21f17-110">Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="21f17-110">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="21f17-111">Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="21f17-111">If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="21f17-112">Значение свойства **Count** никогда не имеет значение Null.</span><span class="sxs-lookup"><span data-stu-id="21f17-112">The **Count** property setting is never Null.</span></span> <span data-ttu-id="21f17-113">Если значение равно 0, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="21f17-113">If its value is 0, there are no objects in the collection.</span></span>

