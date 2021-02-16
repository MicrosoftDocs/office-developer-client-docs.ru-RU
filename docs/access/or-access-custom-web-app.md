---
title: OR (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Объединяет два условия. Возвращает true, если оба условия истинны.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414762"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="d4bc4-104">OR (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="d4bc4-104">OR (Access custom web app)</span></span>

<span data-ttu-id="d4bc4-105">Объединяет два условия.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-105">Combines two conditions.</span></span> <span data-ttu-id="d4bc4-106">Возвращает true, если оба условия истинны.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d4bc4-107">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="d4bc4-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d4bc4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4bc4-109">Syntax</span></span>

 <span data-ttu-id="d4bc4-110">*BooleanExpression* **или** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="d4bc4-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="d4bc4-111">Оператор **Or** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="d4bc4-112">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="d4bc4-112">**Argument name**</span></span>|<span data-ttu-id="d4bc4-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d4bc4-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d4bc4-114">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="d4bc4-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="d4bc4-115">Любое допустимые выражения, возвращая true или FALSE.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4bc4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4bc4-116">Remarks</span></span>

<span data-ttu-id="d4bc4-117">Если в операторе используется несколько логических операторов, операторы **Or** оцениваются после операторов **And.**</span><span class="sxs-lookup"><span data-stu-id="d4bc4-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="d4bc4-118">Однако вы можете изменить порядок оценки с помощью скобок.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="d4bc4-119">В следующей таблице показаны результаты работы оператора **Or.**</span><span class="sxs-lookup"><span data-stu-id="d4bc4-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="d4bc4-120">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="d4bc4-120">**TRUE**</span></span>|<span data-ttu-id="d4bc4-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d4bc4-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4bc4-122">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="d4bc4-122">**TRUE**</span></span> <br/> |<span data-ttu-id="d4bc4-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="d4bc4-123">TRUE</span></span>  <br/> |<span data-ttu-id="d4bc4-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="d4bc4-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="d4bc4-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d4bc4-125">**FALSE**</span></span> <br/> |<span data-ttu-id="d4bc4-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="d4bc4-126">TRUE</span></span>  <br/> |<span data-ttu-id="d4bc4-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="d4bc4-127">FALSE</span></span>  <br/> |
   

