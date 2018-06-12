---
title: ИЛИ функция
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Возвращает значение TRUE (1), если какие-либо логических выражений, переданных в качестве параметров имеют значение TRUE.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814325"
---
# <a name="or-function"></a><span data-ttu-id="c2f55-103">ИЛИ функция</span><span class="sxs-lookup"><span data-stu-id="c2f55-103">OR Function</span></span>

<span data-ttu-id="c2f55-104">Возвращает значение TRUE (1), если какие-либо логических выражений, переданных в качестве параметров имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c2f55-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c2f55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2f55-105">Syntax</span></span>

<span data-ttu-id="c2f55-106">ИЛИ (** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* **)</span><span class="sxs-lookup"><span data-stu-id="c2f55-106">OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c2f55-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2f55-107">Parameters</span></span>

|<span data-ttu-id="c2f55-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c2f55-108">**Name**</span></span>|<span data-ttu-id="c2f55-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="c2f55-109">**Required/Optional**</span></span>|<span data-ttu-id="c2f55-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c2f55-110">**Data Type**</span></span>|<span data-ttu-id="c2f55-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c2f55-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c2f55-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="c2f55-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="c2f55-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c2f55-113">Required</span></span>  <br/> |<span data-ttu-id="c2f55-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c2f55-114">**String**</span></span> <br/> |<span data-ttu-id="c2f55-115">Первое выражение, чтобы оценить достоверность.</span><span class="sxs-lookup"><span data-stu-id="c2f55-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="c2f55-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="c2f55-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="c2f55-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c2f55-117">Required</span></span>  <br/> |<span data-ttu-id="c2f55-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c2f55-118">**String**</span></span> <br/> |<span data-ttu-id="c2f55-119">Второе выражение, чтобы оценить достоверность.</span><span class="sxs-lookup"><span data-stu-id="c2f55-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="c2f55-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="c2f55-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="c2f55-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c2f55-121">Required</span></span>  <br/> |<span data-ttu-id="c2f55-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c2f55-122">**String**</span></span> <br/> |<span data-ttu-id="c2f55-123">N-е выражение, чтобы оценить достоверность.</span><span class="sxs-lookup"><span data-stu-id="c2f55-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c2f55-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c2f55-124">Return value</span></span>

<span data-ttu-id="c2f55-125">Логический</span><span class="sxs-lookup"><span data-stu-id="c2f55-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2f55-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="c2f55-126">Remarks</span></span>

<span data-ttu-id="c2f55-127">Любое выражение, которое оценивается как ненулевое значение считается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c2f55-127">Any expression that evaluates to a non-zero value is considered TRUE.</span></span> <span data-ttu-id="c2f55-128">Если все логические выражения имеют значение FALSE или равно 0, эта функция возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="c2f55-128">If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c2f55-129">Пример</span><span class="sxs-lookup"><span data-stu-id="c2f55-129">Example</span></span>

<span data-ttu-id="c2f55-130">ИЛИ (высота \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="c2f55-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="c2f55-131">Возвращает значение TRUE (1), если одно из выражений имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c2f55-131">Returns TRUE (1) if either expression is TRUE.</span></span> <span data-ttu-id="c2f55-132">Возвращает значение FALSE (0) только в том случае, если оба выражения имеют значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="c2f55-132">Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

