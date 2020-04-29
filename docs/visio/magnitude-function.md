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
description: Возвращает величину вектора, для которого выводится значение "," с прозначением "от" до "б", умноженное на соответствующие константы константа и Константб.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420460"
---
# <a name="magnitude-function"></a><span data-ttu-id="4e578-103">Функция MAGNITUDE</span><span class="sxs-lookup"><span data-stu-id="4e578-103">MAGNITUDE Function</span></span>

<span data-ttu-id="4e578-104">Возвращает величину вектора, для которого выводится значение "," _с_ прозначением "от" до " _б_", умноженное на соответствующие константы _константа_ и _константб_.</span><span class="sxs-lookup"><span data-stu-id="4e578-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4e578-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e578-105">Syntax</span></span>

<span data-ttu-id="4e578-106">ВЕЛИЧИНа (\* \* *константа* \* \* \* \* \*\* \*\* \* \* \*\* \* \*\* \* \* \* \* \* *B* \* \* \* \* \*])</span><span class="sxs-lookup"><span data-stu-id="4e578-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4e578-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e578-107">Parameters</span></span>

|<span data-ttu-id="4e578-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4e578-108">**Name**</span></span>|<span data-ttu-id="4e578-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4e578-109">**Required/Optional**</span></span>|<span data-ttu-id="4e578-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4e578-110">**Data Type**</span></span>|<span data-ttu-id="4e578-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4e578-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4e578-112">_константа_</span><span class="sxs-lookup"><span data-stu-id="4e578-112">_constantA_</span></span> <br/> |<span data-ttu-id="4e578-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="4e578-113">Required</span></span>  <br/> |<span data-ttu-id="4e578-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="4e578-114">**Number**</span></span> <br/> |<span data-ttu-id="4e578-115">Константа, на которой умножается подъем.</span><span class="sxs-lookup"><span data-stu-id="4e578-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="4e578-116">_Определенно_</span><span class="sxs-lookup"><span data-stu-id="4e578-116">_A_</span></span> <br/> |<span data-ttu-id="4e578-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="4e578-117">Required</span></span>  <br/> |<span data-ttu-id="4e578-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="4e578-118">**Number**</span></span> <br/> |<span data-ttu-id="4e578-119">Подъем.</span><span class="sxs-lookup"><span data-stu-id="4e578-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="4e578-120">_константб_</span><span class="sxs-lookup"><span data-stu-id="4e578-120">_constantB_</span></span> <br/> |<span data-ttu-id="4e578-121">Обязательна</span><span class="sxs-lookup"><span data-stu-id="4e578-121">Required</span></span>  <br/> |<span data-ttu-id="4e578-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="4e578-122">**Number**</span></span> <br/> |<span data-ttu-id="4e578-123">Константа, на которую умножается выполнение.</span><span class="sxs-lookup"><span data-stu-id="4e578-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="4e578-124">_З_</span><span class="sxs-lookup"><span data-stu-id="4e578-124">_B_</span></span> <br/> |<span data-ttu-id="4e578-125">Обязательна</span><span class="sxs-lookup"><span data-stu-id="4e578-125">Required</span></span>  <br/> |<span data-ttu-id="4e578-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="4e578-126">**Number**</span></span> <br/> |<span data-ttu-id="4e578-127">Запуск.</span><span class="sxs-lookup"><span data-stu-id="4e578-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e578-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e578-128">Remarks</span></span>

<span data-ttu-id="4e578-129">ВЕЛИЧИНа рассчитывается в соответствии со следующей формулой:</span><span class="sxs-lookup"><span data-stu-id="4e578-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="4e578-130">SQRT ((константа \* A) ^ 2 + (константб \* б) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="4e578-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="4e578-131">Пример</span><span class="sxs-lookup"><span data-stu-id="4e578-131">Example</span></span>

<span data-ttu-id="4e578-132">ВЕЛИЧИНА (1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="4e578-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="4e578-133">Возвращает 5.</span><span class="sxs-lookup"><span data-stu-id="4e578-133">Returns 5.</span></span> 
  

