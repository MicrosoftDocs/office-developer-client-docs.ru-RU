---
title: Функция log (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a897e812-08dc-49c9-954b-e8908a0daab3
description: Возвращает натуральный логарифм или логарифм заданной базы данных Base указанного выражения.
ms.openlocfilehash: e2cfd1cf4ad3c1bf44778737faa0f697333f5234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311090"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="6e3d6-103">Функция log (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="6e3d6-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="6e3d6-104">Возвращает натуральный логарифм или логарифм заданной базы данных Base указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6e3d6-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="6e3d6-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6e3d6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e3d6-107">Syntax</span></span>

 <span data-ttu-id="6e3d6-108">**Log** (*Нумерицекспрессион* , [ *base* ])</span><span class="sxs-lookup"><span data-stu-id="6e3d6-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="6e3d6-109">Функция **log** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="6e3d6-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="6e3d6-110">**Argument name**</span></span>|<span data-ttu-id="6e3d6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e3d6-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6e3d6-112">*Нумерицекспрессион*</span><span class="sxs-lookup"><span data-stu-id="6e3d6-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="6e3d6-113">Положительное число, для которого вычисляется логарифм.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="6e3d6-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="6e3d6-114">*Base*</span></span>  <br/> |<span data-ttu-id="6e3d6-115">Основание логарифма.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-115">The base of the logarithm.</span></span> <span data-ttu-id="6e3d6-116">Если этот параметр опущен, функция **log** Возвращает натуральный логарифм.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e3d6-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e3d6-117">Remarks</span></span>

<span data-ttu-id="6e3d6-118">Функция **LOG10** похожа, но всегда возвращает общий логарифм, то есть логарифм для базового 10.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="6e3d6-119">Натуральный логарифм — это логарифм базового e, где e — константа ирратионал приблизительно равной 2,718281828.</span><span class="sxs-lookup"><span data-stu-id="6e3d6-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

