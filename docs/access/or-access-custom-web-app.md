---
title: ИЛИ (доступа настраиваемых веб-приложения)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Объединение двух условий. Возвращает TRUE, если справедливо одно из двух условий.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807084"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="fea0c-104">ИЛИ (доступа настраиваемых веб-приложения)</span><span class="sxs-lookup"><span data-stu-id="fea0c-104">OR (Access custom web app)</span></span>

<span data-ttu-id="fea0c-105">Объединение двух условий.</span><span class="sxs-lookup"><span data-stu-id="fea0c-105">Combines two conditions.</span></span> <span data-ttu-id="fea0c-106">Возвращает TRUE, если справедливо одно из двух условий.</span><span class="sxs-lookup"><span data-stu-id="fea0c-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="fea0c-107">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fea0c-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="fea0c-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="fea0c-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fea0c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fea0c-109">Syntax</span></span>

 <span data-ttu-id="fea0c-110">*BooleanExpression* **Или** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="fea0c-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="fea0c-111">Оператор **Or** используется следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="fea0c-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="fea0c-112">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="fea0c-112">**Argument name**</span></span>|<span data-ttu-id="fea0c-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fea0c-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fea0c-114">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="fea0c-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="fea0c-115">Любое допустимое выражение, возвращающее значение TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="fea0c-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fea0c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="fea0c-116">Remarks</span></span>

<span data-ttu-id="fea0c-117">Если более одного логический оператор, который используется в операторе, **или** операторы вычисляются после операторов **и** .</span><span class="sxs-lookup"><span data-stu-id="fea0c-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="fea0c-118">Тем не менее можно изменить порядок вычисления с помощью скобок.</span><span class="sxs-lookup"><span data-stu-id="fea0c-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="fea0c-119">В следующей таблице показаны в результате оператор **Or** .</span><span class="sxs-lookup"><span data-stu-id="fea0c-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="fea0c-120">**ЗНАЧЕНИЕ TRUE**</span><span class="sxs-lookup"><span data-stu-id="fea0c-120">**TRUE**</span></span>|<span data-ttu-id="fea0c-121">**ЗНАЧЕНИЕ FALSE**</span><span class="sxs-lookup"><span data-stu-id="fea0c-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fea0c-122">**ЗНАЧЕНИЕ TRUE**</span><span class="sxs-lookup"><span data-stu-id="fea0c-122">**TRUE**</span></span> <br/> |<span data-ttu-id="fea0c-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="fea0c-123">TRUE</span></span>  <br/> |<span data-ttu-id="fea0c-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="fea0c-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="fea0c-125">**ЗНАЧЕНИЕ FALSE**</span><span class="sxs-lookup"><span data-stu-id="fea0c-125">**FALSE**</span></span> <br/> |<span data-ttu-id="fea0c-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="fea0c-126">TRUE</span></span>  <br/> |<span data-ttu-id="fea0c-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="fea0c-127">FALSE</span></span>  <br/> |
   

