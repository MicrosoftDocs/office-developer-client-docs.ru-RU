---
title: Функция ВЕЛИЧИНЫ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Возвращает модуль, развитием — A, а чьи запуск — B, умноженное на соответствующие константы constantA и constantB.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814189"
---
# <a name="magnitude-function"></a><span data-ttu-id="466d7-103">Функция ВЕЛИЧИНЫ</span><span class="sxs-lookup"><span data-stu-id="466d7-103">MAGNITUDE Function</span></span>

<span data-ttu-id="466d7-104">Возвращает модуль, развитием — _A_ , а чьи запуск — _B_, умноженное на соответствующие константы _constantA_ и _constantB_.</span><span class="sxs-lookup"><span data-stu-id="466d7-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="466d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="466d7-105">Syntax</span></span>

<span data-ttu-id="466d7-106">ВЕЛИЧИНА (** *constantA* **, ** *A* **, ** *constantB* **, ** *B* **)</span><span class="sxs-lookup"><span data-stu-id="466d7-106">MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="466d7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="466d7-107">Parameters</span></span>

|<span data-ttu-id="466d7-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="466d7-108">**Name**</span></span>|<span data-ttu-id="466d7-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="466d7-109">**Required/Optional**</span></span>|<span data-ttu-id="466d7-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="466d7-110">**Data Type**</span></span>|<span data-ttu-id="466d7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="466d7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="466d7-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="466d7-112">_constantA_</span></span> <br/> |<span data-ttu-id="466d7-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="466d7-113">Required</span></span>  <br/> |<span data-ttu-id="466d7-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="466d7-114">**Number**</span></span> <br/> |<span data-ttu-id="466d7-115">Константа, на который умножается увеличение.</span><span class="sxs-lookup"><span data-stu-id="466d7-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="466d7-116">_A_</span><span class="sxs-lookup"><span data-stu-id="466d7-116">_A_</span></span> <br/> |<span data-ttu-id="466d7-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="466d7-117">Required</span></span>  <br/> |<span data-ttu-id="466d7-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="466d7-118">**Number**</span></span> <br/> |<span data-ttu-id="466d7-119">Увеличение.</span><span class="sxs-lookup"><span data-stu-id="466d7-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="466d7-120">_constantB_</span><span class="sxs-lookup"><span data-stu-id="466d7-120">_constantB_</span></span> <br/> |<span data-ttu-id="466d7-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="466d7-121">Required</span></span>  <br/> |<span data-ttu-id="466d7-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="466d7-122">**Number**</span></span> <br/> |<span data-ttu-id="466d7-123">Константа, на который умножается запустить.</span><span class="sxs-lookup"><span data-stu-id="466d7-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="466d7-124">_B_</span><span class="sxs-lookup"><span data-stu-id="466d7-124">_B_</span></span> <br/> |<span data-ttu-id="466d7-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="466d7-125">Required</span></span>  <br/> |<span data-ttu-id="466d7-126">**Число**</span><span class="sxs-lookup"><span data-stu-id="466d7-126">**Number**</span></span> <br/> |<span data-ttu-id="466d7-127">Запустить.</span><span class="sxs-lookup"><span data-stu-id="466d7-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="466d7-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="466d7-128">Remarks</span></span>

<span data-ttu-id="466d7-129">ВЕЛИЧИНА рассчитывается по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="466d7-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="466d7-130">КОРЕНЬ ((constantA \* A) ^ 2 + (constantB \* Б) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="466d7-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="466d7-131">Пример</span><span class="sxs-lookup"><span data-stu-id="466d7-131">Example</span></span>

<span data-ttu-id="466d7-132">ВЕЛИЧИНА (1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="466d7-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="466d7-133">Возвращает 5.</span><span class="sxs-lookup"><span data-stu-id="466d7-133">Returns 5.</span></span> 
  

