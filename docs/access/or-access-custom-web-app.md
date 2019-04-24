---
title: ИЛИ (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Объединяет два условия. Возвращает значение TRUE, если любое из двух условий имеет значение true.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308073"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="43a23-104">ИЛИ (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="43a23-104">OR (Access custom web app)</span></span>

<span data-ttu-id="43a23-105">Объединяет два условия.</span><span class="sxs-lookup"><span data-stu-id="43a23-105">Combines two conditions.</span></span> <span data-ttu-id="43a23-106">Возвращает значение TRUE, если любое из двух условий имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="43a23-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="43a23-107">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="43a23-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="43a23-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="43a23-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="43a23-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43a23-109">Syntax</span></span>

 <span data-ttu-id="43a23-110">*Булеанекспрессион* **Или** *Булеанекспрессион*</span><span class="sxs-lookup"><span data-stu-id="43a23-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="43a23-111">Оператор **or** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="43a23-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="43a23-112">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="43a23-112">**Argument name**</span></span>|<span data-ttu-id="43a23-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="43a23-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="43a23-114">*Булеанекспрессион*</span><span class="sxs-lookup"><span data-stu-id="43a23-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="43a23-115">Любое допустимое выражение, возвращающее значение TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="43a23-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43a23-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="43a23-116">Remarks</span></span>

<span data-ttu-id="43a23-117">Если в операторе используется несколько логических операторов, операторы **or** оцениваются после операторов **and** .</span><span class="sxs-lookup"><span data-stu-id="43a23-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="43a23-118">Однако порядок оценки можно изменить с помощью круглых скобок.</span><span class="sxs-lookup"><span data-stu-id="43a23-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="43a23-119">В приведенной ниже таблице показан результат выполнения оператора **or** .</span><span class="sxs-lookup"><span data-stu-id="43a23-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="43a23-120">**ОТНОСИТСЯ**</span><span class="sxs-lookup"><span data-stu-id="43a23-120">**TRUE**</span></span>|<span data-ttu-id="43a23-121">**ЗНАЧЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="43a23-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43a23-122">**ОТНОСИТСЯ**</span><span class="sxs-lookup"><span data-stu-id="43a23-122">**TRUE**</span></span> <br/> |<span data-ttu-id="43a23-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="43a23-123">TRUE</span></span>  <br/> |<span data-ttu-id="43a23-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="43a23-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="43a23-125">**ЗНАЧЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="43a23-125">**FALSE**</span></span> <br/> |<span data-ttu-id="43a23-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="43a23-126">TRUE</span></span>  <br/> |<span data-ttu-id="43a23-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="43a23-127">FALSE</span></span>  <br/> |
   

