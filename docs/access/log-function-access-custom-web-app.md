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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419298"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="3fa66-103">Функция log (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="3fa66-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="3fa66-104">Возвращает натуральный логарифм или логарифм заданной базы данных Base указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="3fa66-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3fa66-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3fa66-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="3fa66-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="3fa66-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3fa66-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fa66-107">Syntax</span></span>

 <span data-ttu-id="3fa66-108">**Журнал** (*Нумерицекспрессион* , [ *base* ])</span><span class="sxs-lookup"><span data-stu-id="3fa66-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="3fa66-109">Функция **log** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="3fa66-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="3fa66-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="3fa66-110">**Argument name**</span></span>|<span data-ttu-id="3fa66-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3fa66-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3fa66-112">*нумерицекспрессион*</span><span class="sxs-lookup"><span data-stu-id="3fa66-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="3fa66-113">Положительное число, для которого вычисляется логарифм.</span><span class="sxs-lookup"><span data-stu-id="3fa66-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="3fa66-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="3fa66-114">*Base*</span></span>  <br/> |<span data-ttu-id="3fa66-115">Основание логарифма.</span><span class="sxs-lookup"><span data-stu-id="3fa66-115">The base of the logarithm.</span></span> <span data-ttu-id="3fa66-116">Если этот параметр опущен, функция **log** Возвращает натуральный логарифм.</span><span class="sxs-lookup"><span data-stu-id="3fa66-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fa66-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="3fa66-117">Remarks</span></span>

<span data-ttu-id="3fa66-118">Функция **LOG10** похожа, но всегда возвращает общий логарифм, то есть логарифм для базового 10.</span><span class="sxs-lookup"><span data-stu-id="3fa66-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="3fa66-119">Натуральный логарифм — это логарифм базового e, где e — константа ирратионал приблизительно равной 2,718281828.</span><span class="sxs-lookup"><span data-stu-id="3fa66-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

