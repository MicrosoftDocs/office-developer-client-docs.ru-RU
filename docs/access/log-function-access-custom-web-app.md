---
title: Log Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a897e812-08dc-49c9-954b-e8908a0daab3
description: Возвращает естественный логарифм или логарифм указанного выражения.
ms.openlocfilehash: e2cfd1cf4ad3c1bf44778737faa0f697333f5234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419298"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="a36f8-103">Log Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="a36f8-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="a36f8-104">Возвращает естественный логарифм или логарифм указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="a36f8-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a36f8-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a36f8-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="a36f8-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="a36f8-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a36f8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a36f8-107">Syntax</span></span>

 <span data-ttu-id="a36f8-108">**Log** (*NumericExpression*  , [  *Base*  ])</span><span class="sxs-lookup"><span data-stu-id="a36f8-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="a36f8-109">Функция **Log** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a36f8-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a36f8-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="a36f8-110">**Argument name**</span></span>|<span data-ttu-id="a36f8-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a36f8-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a36f8-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="a36f8-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="a36f8-113">Положительное число, для которого нужно логарифм.</span><span class="sxs-lookup"><span data-stu-id="a36f8-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="a36f8-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="a36f8-114">*Base*</span></span>  <br/> |<span data-ttu-id="a36f8-115">Основа логарифма.</span><span class="sxs-lookup"><span data-stu-id="a36f8-115">The base of the logarithm.</span></span> <span data-ttu-id="a36f8-116">Если этот опущен, функция **Log** возвращает естественный логарифм.</span><span class="sxs-lookup"><span data-stu-id="a36f8-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a36f8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="a36f8-117">Remarks</span></span>

<span data-ttu-id="a36f8-118">Функция **Log10** аналогична, но всегда возвращает общий логарифм, то есть логарифм для базовой 10.</span><span class="sxs-lookup"><span data-stu-id="a36f8-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="a36f8-119">Естественный логарифм — это логарифм в базовой e, где e — это константа-заметь, приблизительно равная 2,718281828.</span><span class="sxs-lookup"><span data-stu-id="a36f8-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

