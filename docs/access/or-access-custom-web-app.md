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
# <a name="or-access-custom-web-app"></a><span data-ttu-id="60aad-104">ИЛИ (доступа настраиваемых веб-приложения)</span><span class="sxs-lookup"><span data-stu-id="60aad-104">OR (Access custom web app)</span></span>

<span data-ttu-id="60aad-105">Объединение двух условий.</span><span class="sxs-lookup"><span data-stu-id="60aad-105">Combines two conditions.</span></span> <span data-ttu-id="60aad-106">Возвращает TRUE, если справедливо одно из двух условий.</span><span class="sxs-lookup"><span data-stu-id="60aad-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="60aad-107">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="60aad-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="60aad-108">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="60aad-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="60aad-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60aad-109">Syntax</span></span>

 <span data-ttu-id="60aad-110">*BooleanExpression* **Или** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="60aad-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="60aad-111">Оператор **Or** используется следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="60aad-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="60aad-112">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="60aad-112">**Argument name**</span></span>|<span data-ttu-id="60aad-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="60aad-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="60aad-114">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="60aad-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="60aad-115">Любое допустимое выражение, возвращающее значение TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="60aad-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60aad-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="60aad-116">Remarks</span></span>

<span data-ttu-id="60aad-117">Если более одного логический оператор, который используется в операторе, **или** операторы вычисляются после операторов **и** .</span><span class="sxs-lookup"><span data-stu-id="60aad-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="60aad-118">Тем не менее можно изменить порядок вычисления с помощью скобок.</span><span class="sxs-lookup"><span data-stu-id="60aad-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="60aad-119">В следующей таблице показаны в результате оператор **Or** .</span><span class="sxs-lookup"><span data-stu-id="60aad-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="60aad-120">**ЗНАЧЕНИЕ TRUE**</span><span class="sxs-lookup"><span data-stu-id="60aad-120">**TRUE**</span></span>|<span data-ttu-id="60aad-121">**ЗНАЧЕНИЕ FALSE**</span><span class="sxs-lookup"><span data-stu-id="60aad-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="60aad-122">**ЗНАЧЕНИЕ TRUE**</span><span class="sxs-lookup"><span data-stu-id="60aad-122">**TRUE**</span></span> <br/> |<span data-ttu-id="60aad-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="60aad-123">TRUE</span></span>  <br/> |<span data-ttu-id="60aad-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="60aad-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="60aad-125">**ЗНАЧЕНИЕ FALSE**</span><span class="sxs-lookup"><span data-stu-id="60aad-125">**FALSE**</span></span> <br/> |<span data-ttu-id="60aad-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="60aad-126">TRUE</span></span>  <br/> |<span data-ttu-id="60aad-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="60aad-127">FALSE</span></span>  <br/> |
   

