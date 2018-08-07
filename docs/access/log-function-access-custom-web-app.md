---
title: Функция log (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a897e812-08dc-49c9-954b-e8908a0daab3
description: Возвращает натуральный логарифм или логарифм базовой, указанного выражения.
ms.openlocfilehash: 5004b2b32e89a9d68364d271e8b94d72b012a62c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806931"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="73faa-103">Функция log (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="73faa-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="73faa-104">Возвращает натуральный логарифм или логарифм базовой, указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="73faa-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="73faa-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="73faa-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="73faa-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="73faa-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="73faa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73faa-107">Syntax</span></span>

 <span data-ttu-id="73faa-108">**Журнал** (*NumericExpression* , [ *Base* ])</span><span class="sxs-lookup"><span data-stu-id="73faa-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="73faa-109">Функция **Log** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="73faa-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="73faa-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="73faa-110">**Argument name**</span></span>|<span data-ttu-id="73faa-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73faa-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="73faa-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="73faa-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="73faa-113">Положительное число, для которого вы хотите логарифм.</span><span class="sxs-lookup"><span data-stu-id="73faa-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="73faa-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="73faa-114">*Base*</span></span>  <br/> |<span data-ttu-id="73faa-115">Основание логарифма.</span><span class="sxs-lookup"><span data-stu-id="73faa-115">The base of the logarithm.</span></span> <span data-ttu-id="73faa-116">Если этот параметр опущен, функция **Log** Возвращает натуральный логарифм.</span><span class="sxs-lookup"><span data-stu-id="73faa-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73faa-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="73faa-117">Remarks</span></span>

<span data-ttu-id="73faa-118">Функция **Log10** аналогичен, но всегда возвращает десятичного логарифма, то есть логарифма для основанию 10.</span><span class="sxs-lookup"><span data-stu-id="73faa-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="73faa-119">Натуральный логарифм — это логарифм с основанием e, где e является константой irrational примерно равно 2.718281828.</span><span class="sxs-lookup"><span data-stu-id="73faa-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

