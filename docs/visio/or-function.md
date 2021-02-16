---
title: Функция OR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Возвращает true (1), если любое из логических выражений, переданных в качестве параметров, является TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433509"
---
# <a name="or-function"></a><span data-ttu-id="aff94-103">Функция OR</span><span class="sxs-lookup"><span data-stu-id="aff94-103">OR Function</span></span>

<span data-ttu-id="aff94-104">Возвращает true (1), если любое из логических выражений, переданных в качестве параметров, является TRUE.</span><span class="sxs-lookup"><span data-stu-id="aff94-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="aff94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aff94-105">Syntax</span></span>

<span data-ttu-id="aff94-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="aff94-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aff94-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aff94-107">Parameters</span></span>

|<span data-ttu-id="aff94-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="aff94-108">**Name**</span></span>|<span data-ttu-id="aff94-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="aff94-109">**Required/Optional**</span></span>|<span data-ttu-id="aff94-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="aff94-110">**Data Type**</span></span>|<span data-ttu-id="aff94-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aff94-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aff94-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="aff94-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="aff94-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="aff94-113">Required</span></span>  <br/> |<span data-ttu-id="aff94-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="aff94-114">**String**</span></span> <br/> |<span data-ttu-id="aff94-115">Первое выражение, истина которого вы хотите оценить.</span><span class="sxs-lookup"><span data-stu-id="aff94-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="aff94-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="aff94-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="aff94-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="aff94-117">Required</span></span>  <br/> |<span data-ttu-id="aff94-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="aff94-118">**String**</span></span> <br/> |<span data-ttu-id="aff94-119">Второе выражение, истина которого вы хотите оценить.</span><span class="sxs-lookup"><span data-stu-id="aff94-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="aff94-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="aff94-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="aff94-121">Обязательно</span><span class="sxs-lookup"><span data-stu-id="aff94-121">Required</span></span>  <br/> |<span data-ttu-id="aff94-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="aff94-122">**String**</span></span> <br/> |<span data-ttu-id="aff94-123">N-выражение, истина которого вы хотите оценить.</span><span class="sxs-lookup"><span data-stu-id="aff94-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aff94-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aff94-124">Return value</span></span>

<span data-ttu-id="aff94-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="aff94-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aff94-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="aff94-126">Remarks</span></span>

<span data-ttu-id="aff94-127">Любое выражение, которое оценивается как ненулевой, считается TRUE.</span><span class="sxs-lookup"><span data-stu-id="aff94-127">Any expression that evaluates to a non-zero value is considered TRUE.</span></span> <span data-ttu-id="aff94-128">Если все логические выражения имеют логическое выражение FALSE или равно 0, эта функция возвращает false.</span><span class="sxs-lookup"><span data-stu-id="aff94-128">If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="aff94-129">Пример</span><span class="sxs-lookup"><span data-stu-id="aff94-129">Example</span></span>

<span data-ttu-id="aff94-130">OR(Height \> 1,PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="aff94-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="aff94-131">Возвращает true (1), если для любого из выражений засве-ется TRUE.</span><span class="sxs-lookup"><span data-stu-id="aff94-131">Returns TRUE (1) if either expression is TRUE.</span></span> <span data-ttu-id="aff94-132">Возвращает false (0), только если оба выражения являются FALSE.</span><span class="sxs-lookup"><span data-stu-id="aff94-132">Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

