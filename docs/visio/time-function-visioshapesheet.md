---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Возвращает время, представляемые часом, минутой и секундой.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414475"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="aff2d-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="aff2d-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="aff2d-104">Возвращает время, представляемые _часом,_ _минутой_ и _секундой._</span><span class="sxs-lookup"><span data-stu-id="aff2d-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="aff2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aff2d-105">Syntax</span></span>

<span data-ttu-id="aff2d-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span><span class="sxs-lookup"><span data-stu-id="aff2d-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aff2d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aff2d-107">Parameters</span></span>

|<span data-ttu-id="aff2d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="aff2d-108">**Name**</span></span>|<span data-ttu-id="aff2d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="aff2d-109">**Required/Optional**</span></span>|<span data-ttu-id="aff2d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="aff2d-110">**Data Type**</span></span>|<span data-ttu-id="aff2d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aff2d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aff2d-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="aff2d-112">_hour_</span></span> <br/> |<span data-ttu-id="aff2d-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="aff2d-113">Required</span></span>  <br/> |<span data-ttu-id="aff2d-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="aff2d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="aff2d-115">Компонент "час".</span><span class="sxs-lookup"><span data-stu-id="aff2d-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="aff2d-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="aff2d-116">_minute_</span></span> <br/> |<span data-ttu-id="aff2d-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="aff2d-117">Required</span></span>  <br/> |<span data-ttu-id="aff2d-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="aff2d-118">**Numeric**</span></span> <br/> |<span data-ttu-id="aff2d-119">Минутный comonent.</span><span class="sxs-lookup"><span data-stu-id="aff2d-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="aff2d-120">_second_</span><span class="sxs-lookup"><span data-stu-id="aff2d-120">_second_</span></span> <br/> |<span data-ttu-id="aff2d-121">Обязательна</span><span class="sxs-lookup"><span data-stu-id="aff2d-121">Required</span></span>  <br/> |<span data-ttu-id="aff2d-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="aff2d-122">**Numeric**</span></span> <br/> |<span data-ttu-id="aff2d-123">Второй компонент.</span><span class="sxs-lookup"><span data-stu-id="aff2d-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aff2d-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aff2d-124">Return value</span></span>

<span data-ttu-id="aff2d-125">Числовой</span><span class="sxs-lookup"><span data-stu-id="aff2d-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="aff2d-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aff2d-126">Example 1</span></span>

<span data-ttu-id="aff2d-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="aff2d-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="aff2d-128">Возвращает значение, представляющее 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="aff2d-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="aff2d-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aff2d-129">Example 2</span></span>

<span data-ttu-id="aff2d-130">FORMAT(TIME(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="aff2d-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="aff2d-131">Возвращает значение, представляющее 15:30.</span><span class="sxs-lookup"><span data-stu-id="aff2d-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="aff2d-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="aff2d-132">Example 3</span></span>

<span data-ttu-id="aff2d-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="aff2d-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="aff2d-134">Возвращает значение, представляющее 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="aff2d-134">Returns the value representing 23:30:30.</span></span>
  

