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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414762"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="be63b-104">ИЛИ (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="be63b-104">OR (Access custom web app)</span></span>

<span data-ttu-id="be63b-105">Объединяет два условия.</span><span class="sxs-lookup"><span data-stu-id="be63b-105">Combines two conditions.</span></span> <span data-ttu-id="be63b-106">Возвращает значение TRUE, если любое из двух условий имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="be63b-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="be63b-107">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="be63b-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="be63b-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="be63b-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="be63b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be63b-109">Syntax</span></span>

 <span data-ttu-id="be63b-110">*Булеанекспрессион* **или** *булеанекспрессион*</span><span class="sxs-lookup"><span data-stu-id="be63b-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="be63b-111">Оператор **or** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="be63b-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="be63b-112">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="be63b-112">**Argument name**</span></span>|<span data-ttu-id="be63b-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be63b-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="be63b-114">*булеанекспрессион*</span><span class="sxs-lookup"><span data-stu-id="be63b-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="be63b-115">Любое допустимое выражение, возвращающее значение TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="be63b-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be63b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="be63b-116">Remarks</span></span>

<span data-ttu-id="be63b-117">Если в операторе используется несколько логических операторов, операторы **or** оцениваются после операторов **and** .</span><span class="sxs-lookup"><span data-stu-id="be63b-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="be63b-118">Однако порядок оценки можно изменить с помощью круглых скобок.</span><span class="sxs-lookup"><span data-stu-id="be63b-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="be63b-119">В приведенной ниже таблице показан результат выполнения оператора **or** .</span><span class="sxs-lookup"><span data-stu-id="be63b-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="be63b-120">**ОТНОСИТСЯ**</span><span class="sxs-lookup"><span data-stu-id="be63b-120">**TRUE**</span></span>|<span data-ttu-id="be63b-121">**ЗНАЧЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="be63b-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="be63b-122">**ОТНОСИТСЯ**</span><span class="sxs-lookup"><span data-stu-id="be63b-122">**TRUE**</span></span> <br/> |<span data-ttu-id="be63b-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="be63b-123">TRUE</span></span>  <br/> |<span data-ttu-id="be63b-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="be63b-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="be63b-125">**ЗНАЧЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="be63b-125">**FALSE**</span></span> <br/> |<span data-ttu-id="be63b-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="be63b-126">TRUE</span></span>  <br/> |<span data-ttu-id="be63b-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="be63b-127">FALSE</span></span>  <br/> |
   

