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
description: Возвращает значение истина (1), если какие-либо из логических выражений, переданных в качестве параметров, имеют значение TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433509"
---
# <a name="or-function"></a><span data-ttu-id="a4074-103">Функция OR</span><span class="sxs-lookup"><span data-stu-id="a4074-103">OR Function</span></span>

<span data-ttu-id="a4074-104">Возвращает значение истина (1), если какие-либо из логических выражений, переданных в качестве параметров, имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="a4074-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a4074-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4074-105">Syntax</span></span>

<span data-ttu-id="a4074-106">OR (\* \* *logicalexpression1* \* \*, \* \* *logicalexpression2* \* \*,..., \* \* *логикалекспрессионн* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a4074-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a4074-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4074-107">Parameters</span></span>

|<span data-ttu-id="a4074-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a4074-108">**Name**</span></span>|<span data-ttu-id="a4074-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a4074-109">**Required/Optional**</span></span>|<span data-ttu-id="a4074-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a4074-110">**Data Type**</span></span>|<span data-ttu-id="a4074-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a4074-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a4074-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="a4074-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="a4074-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a4074-113">Required</span></span>  <br/> |<span data-ttu-id="a4074-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a4074-114">**String**</span></span> <br/> |<span data-ttu-id="a4074-115">Первое выражение, для которого необходимо оценить истинность.</span><span class="sxs-lookup"><span data-stu-id="a4074-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="a4074-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="a4074-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="a4074-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a4074-117">Required</span></span>  <br/> |<span data-ttu-id="a4074-118">**String**</span><span class="sxs-lookup"><span data-stu-id="a4074-118">**String**</span></span> <br/> |<span data-ttu-id="a4074-119">Второе выражение, для которого необходимо оценить истинность.</span><span class="sxs-lookup"><span data-stu-id="a4074-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="a4074-120">_логикалекспрессионн_</span><span class="sxs-lookup"><span data-stu-id="a4074-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="a4074-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a4074-121">Required</span></span>  <br/> |<span data-ttu-id="a4074-122">**String**</span><span class="sxs-lookup"><span data-stu-id="a4074-122">**String**</span></span> <br/> |<span data-ttu-id="a4074-123">Выражение n, для которого нужно вычислить истинность.</span><span class="sxs-lookup"><span data-stu-id="a4074-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a4074-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4074-124">Return value</span></span>

<span data-ttu-id="a4074-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4074-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4074-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="a4074-126">Remarks</span></span>

<span data-ttu-id="a4074-127">Любое выражение, результатом которого является ненулевое значение, считается ИСТИНным.</span><span class="sxs-lookup"><span data-stu-id="a4074-127">Any expression that evaluates to a non-zero value is considered TRUE.</span></span> <span data-ttu-id="a4074-128">Если все логические выражения имеют значение ложь или равно 0, эта функция возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="a4074-128">If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a4074-129">Пример</span><span class="sxs-lookup"><span data-stu-id="a4074-129">Example</span></span>

<span data-ttu-id="a4074-130">ИЛИ (Height \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="a4074-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="a4074-131">Возвращает значение истина (1), если любое из выражений имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="a4074-131">Returns TRUE (1) if either expression is TRUE.</span></span> <span data-ttu-id="a4074-132">Возвращает значение FALSE (0) только в том случае, если оба выражения имеют значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="a4074-132">Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

