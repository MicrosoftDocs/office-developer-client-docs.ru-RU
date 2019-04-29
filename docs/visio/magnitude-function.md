---
title: Функция MAGNITUDE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Возвращает величину вектора, для которого выводится значение "," С прозначением "от" до "Б", умноженное на соответствующие константы константа и Константб.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420460"
---
# <a name="magnitude-function"></a><span data-ttu-id="f0a66-103">Функция MAGNITUDE</span><span class="sxs-lookup"><span data-stu-id="f0a66-103">MAGNITUDE Function</span></span>

<span data-ttu-id="f0a66-104">Возвращает величину вектора, для которого выводится значение "," _с_ прозначением "от" до " _б_", умноженное на соответствующие константы _константа_ и _константб_.</span><span class="sxs-lookup"><span data-stu-id="f0a66-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f0a66-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0a66-105">Syntax</span></span>

<span data-ttu-id="f0a66-106">ВЕЛИЧИНа (\* \*\* константа\* \* \* \* \* \* \* \* \* \* \* \*\* \* \* \* \* \* \* \* \* \* \* \*]) \*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="f0a66-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f0a66-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0a66-107">Parameters</span></span>

|<span data-ttu-id="f0a66-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f0a66-108">**Name**</span></span>|<span data-ttu-id="f0a66-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="f0a66-109">**Required/Optional**</span></span>|<span data-ttu-id="f0a66-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f0a66-110">**Data Type**</span></span>|<span data-ttu-id="f0a66-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f0a66-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f0a66-112">_Константа_</span><span class="sxs-lookup"><span data-stu-id="f0a66-112">_constantA_</span></span> <br/> |<span data-ttu-id="f0a66-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f0a66-113">Required</span></span>  <br/> |<span data-ttu-id="f0a66-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="f0a66-114">**Number**</span></span> <br/> |<span data-ttu-id="f0a66-115">Константа, на которой умножается подъем.</span><span class="sxs-lookup"><span data-stu-id="f0a66-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="f0a66-116">_A_</span><span class="sxs-lookup"><span data-stu-id="f0a66-116">_A_</span></span> <br/> |<span data-ttu-id="f0a66-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f0a66-117">Required</span></span>  <br/> |<span data-ttu-id="f0a66-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="f0a66-118">**Number**</span></span> <br/> |<span data-ttu-id="f0a66-119">Подъем.</span><span class="sxs-lookup"><span data-stu-id="f0a66-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="f0a66-120">_Константб_</span><span class="sxs-lookup"><span data-stu-id="f0a66-120">_constantB_</span></span> <br/> |<span data-ttu-id="f0a66-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f0a66-121">Required</span></span>  <br/> |<span data-ttu-id="f0a66-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="f0a66-122">**Number**</span></span> <br/> |<span data-ttu-id="f0a66-123">Константа, на которую умножается выполнение.</span><span class="sxs-lookup"><span data-stu-id="f0a66-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="f0a66-124">_З_</span><span class="sxs-lookup"><span data-stu-id="f0a66-124">_B_</span></span> <br/> |<span data-ttu-id="f0a66-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f0a66-125">Required</span></span>  <br/> |<span data-ttu-id="f0a66-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="f0a66-126">**Number**</span></span> <br/> |<span data-ttu-id="f0a66-127">Запуск.</span><span class="sxs-lookup"><span data-stu-id="f0a66-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0a66-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="f0a66-128">Remarks</span></span>

<span data-ttu-id="f0a66-129">ВЕЛИЧИНа рассчитывается в соответствии со следующей формулой:</span><span class="sxs-lookup"><span data-stu-id="f0a66-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="f0a66-130">SQRT ((константа \* A) ^ 2 + (константб \* б) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="f0a66-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="f0a66-131">Пример</span><span class="sxs-lookup"><span data-stu-id="f0a66-131">Example</span></span>

<span data-ttu-id="f0a66-132">ВЕЛИЧИНА (1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="f0a66-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="f0a66-133">Возвращает 5.</span><span class="sxs-lookup"><span data-stu-id="f0a66-133">Returns 5.</span></span> 
  

