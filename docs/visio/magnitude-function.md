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
description: Возвращает величину вектора, рост которого — A, а запуск — B, умноженный на соответствующие константы constantA и constantB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420460"
---
# <a name="magnitude-function"></a><span data-ttu-id="24971-103">Функция MAGNITUDE</span><span class="sxs-lookup"><span data-stu-id="24971-103">MAGNITUDE Function</span></span>

<span data-ttu-id="24971-104">Возвращает величину вектора, рост которого является _A_ и запуск которого _B,_ умножен на соответствующие константы _constantA_ и _constantB._</span><span class="sxs-lookup"><span data-stu-id="24971-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="24971-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24971-105">Syntax</span></span>

<span data-ttu-id="24971-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span><span class="sxs-lookup"><span data-stu-id="24971-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="24971-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24971-107">Parameters</span></span>

|<span data-ttu-id="24971-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="24971-108">**Name**</span></span>|<span data-ttu-id="24971-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="24971-109">**Required/Optional**</span></span>|<span data-ttu-id="24971-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="24971-110">**Data Type**</span></span>|<span data-ttu-id="24971-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="24971-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="24971-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="24971-112">_constantA_</span></span> <br/> |<span data-ttu-id="24971-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="24971-113">Required</span></span>  <br/> |<span data-ttu-id="24971-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="24971-114">**Number**</span></span> <br/> |<span data-ttu-id="24971-115">Константа, с помощью которой можно умножить рост.</span><span class="sxs-lookup"><span data-stu-id="24971-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="24971-116">_A_</span><span class="sxs-lookup"><span data-stu-id="24971-116">_A_</span></span> <br/> |<span data-ttu-id="24971-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="24971-117">Required</span></span>  <br/> |<span data-ttu-id="24971-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="24971-118">**Number**</span></span> <br/> |<span data-ttu-id="24971-119">Подъем.</span><span class="sxs-lookup"><span data-stu-id="24971-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="24971-120">_constantB_</span><span class="sxs-lookup"><span data-stu-id="24971-120">_constantB_</span></span> <br/> |<span data-ttu-id="24971-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="24971-121">Required</span></span>  <br/> |<span data-ttu-id="24971-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="24971-122">**Number**</span></span> <br/> |<span data-ttu-id="24971-123">Константа, с помощью которой можно умножить запуск.</span><span class="sxs-lookup"><span data-stu-id="24971-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="24971-124">_B_</span><span class="sxs-lookup"><span data-stu-id="24971-124">_B_</span></span> <br/> |<span data-ttu-id="24971-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="24971-125">Required</span></span>  <br/> |<span data-ttu-id="24971-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="24971-126">**Number**</span></span> <br/> |<span data-ttu-id="24971-127">Запуск.</span><span class="sxs-lookup"><span data-stu-id="24971-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24971-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="24971-128">Remarks</span></span>

<span data-ttu-id="24971-129">ВЕЛИЧИНА вычисляется по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="24971-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="24971-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span><span class="sxs-lookup"><span data-stu-id="24971-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="24971-131">Пример</span><span class="sxs-lookup"><span data-stu-id="24971-131">Example</span></span>

<span data-ttu-id="24971-132">MAGNITUDE (1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="24971-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="24971-133">Возвращает 5.</span><span class="sxs-lookup"><span data-stu-id="24971-133">Returns 5.</span></span> 
  

